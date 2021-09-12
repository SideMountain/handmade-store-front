<template>
  <v-row>
    <v-col v-for="item in items" :key="item.id" cols="3">
      <v-card min-height="100px" outlined hover>
        <v-layout justify-center>
          <v-img
            class="shrink mr-2"
            contain
            :src="require('../../assets/origami_logo.png')"
            width="150"
          >
          </v-img>
        </v-layout>
        <v-card-title>
          {{ item.title }}
        </v-card-title>
        <v-card-subtitle class="text-right">
          ¥{{ item.price }}
        </v-card-subtitle>
        <v-divider />
        <v-card-text>
          {{ item.explanation }}
        </v-card-text>
        <v-card-actions>
          <v-spacer />
          <v-btn dark color="primary" @click="alertDetail(item.id)">
            詳細
          </v-btn>

          <v-btn class="mx-2" dark color="teal" @click="alertAddCart(item.id)">
            <v-icon dark> mdi-cart-arrow-down </v-icon>
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-col>
  </v-row>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component
export default class ItemList extends Vue {
  items = [
    {
      id: '001',
      title: '商品1',
      price: '1000',
      explanation:
        '商品説明商品説明商品説明商品説明商品説明商品説明商品説明商品説明商品説明商品説明商品説明',
      src: '../../assets/origami_logo.png',
    },
    {
      id: '002',
      title: '商品2',
      price: '2000',
      explanation:
        '商品説明商品説明商品説明商品説明商品説明商品説明商品説明商品説明商品説明商品説明商品説明',
      src: '../../assets/origami_logo.png',
    },
    {
      id: '003',
      title: '商品3',
      price: '3000',
      explanation:
        '商品説明商品説明商品説明商品説明商品説明商品説明商品説明商品説明商品説明商品説明商品説明',
      src: '../../assets/origami_logo.png',
    },
    {
      id: '004',
      title: '商品4',
      price: '4000',
      explanation:
        '商品説明商品説明商品説明商品説明商品説明商品説明商品説明商品説明商品説明商品説明商品説明',
      src: '../../assets/origami_logo.png',
    },
    {
      id: '005',
      title: '商品5',
      price: '5000',
      explanation:
        '商品説明商品説明商品説明商品説明商品説明商品説明商品説明商品説明商品説明商品説明商品説明',
      src: '../../assets/origami_logo.png',
    },
    {
      id: '006',
      title: '商品6',
      price: '6000',
      explanation:
        '商品説明商品説明商品説明商品説明商品説明商品説明商品説明商品説明商品説明商品説明商品説明',
      src: '../../assets/origami_logo.png',
    },
  ];

  alertDetail(id: string): void {
    alert(id + ' Detail');
  }
  alertAddCart(id: string): void {
    alert('Add ' + id + ' to Cart');
  }
}
</script>
