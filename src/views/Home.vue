<template>
  <v-main>
    <v-container fluid="false">
      <Carousels />
      <v-layout wrap>
        <v-flex md2>
          <h3>カテゴリー</h3>
          <SideMenu />
        </v-flex>
        <v-flex md10>
          <v-row>
            <v-col cols="12">
              <h3 class="mb-3">新着商品</h3>
              <ItemList />
            </v-col>
          </v-row>
        </v-flex>
      </v-layout>
    </v-container>
  </v-main>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import Carousels from '../components/home/Carousels.vue';
import ItemList from '../components/items/ItemList.vue';
import SideMenu from '../components/home/SideMenu.vue';

@Component({
  components: {
    Carousels,
    ItemList,
    SideMenu,
  },
})
export default class Home extends Vue {}
</script>
