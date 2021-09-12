<template>
  <v-main>
    <v-container fluid="false">
      <h1 class="mb-5">ショッピングカート一覧</h1>
      <v-divider></v-divider>
      <v-sheet
        class="mt-5 py-5 px-5"
        color="white"
        elevation="1"
        min-height="200px"
        rounded
      >
        <v-alert v-if="!cartItems.length">カート内に商品がありません。</v-alert>
        <v-simple-table v-else fixed-header>
          <template slot:default>
            <thead>
              <tr>
                <th>商品名</th>
                <th>価格</th>
                <th>個数</th>
              </tr>
            </thead>
            <tbody>
              <tr v-for="item in cartItems" :key="item.name">
                <td>{{ item.name }}</td>
                <td>¥{{ item.price }}</td>
                <td>{{ item.count }}</td>
              </tr>
              <tr>
                <td colspan="3" class="text-right">合計：¥{{ totalPrice }}</td>
              </tr>
            </tbody>
          </template>
        </v-simple-table>
        <v-row class="mt-5 justify-end">
          <v-btn text outlined class="ml-3" @click="$router.push('/')">
            <v-icon>mdi-store-outline</v-icon>
            <span class="ml-2">買い物を続ける</span>
          </v-btn>
          <v-btn text outlined class="ml-3" @click="alertCheck()">
            <v-icon>mdi-cart-check</v-icon>
            <span class="ml-2">購入内容を確認する</span>
          </v-btn>
        </v-row>
      </v-sheet>
    </v-container>
  </v-main>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component
export default class Cart extends Vue {
  totalPrice = '21000';
  cartItems = [
    {
      id: '001',
      name: '商品1',
      price: '1000',
      count: '1',
    },
    {
      id: '004',
      name: '商品4',
      price: '4000',
      count: '5',
    },
  ];
  alertCheck() {
    alert(this.totalPrice + '円です。購入確認画面へ遷移します。');
  }
}
</script>
