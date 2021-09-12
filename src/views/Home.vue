<template>
  <v-main>
    <v-container fluid="false">
      <carousels />
      <v-layout wrap>
        <v-flex md2>
          <h3>カテゴリー</h3>
          <side-menu />
        </v-flex>
        <v-flex md10>
          <v-row>
            <v-col cols="12">
              <h3 class="mb-3">新着商品</h3>
              <item-list />
            </v-col>
          </v-row>
        </v-flex>
      </v-layout>
    </v-container>
  </v-main>
</template>

<script lang="ts">
  import Vue from 'vue'
  import Carousels from '../components/home/Carousels.vue'
  import ItemList from '../components/items/ItemList.vue'
  import SideMenu from '../components/home/SideMenu.vue'

  export default Vue.extend({
    name: 'Home',

    components: {
      Carousels,
      ItemList,
      SideMenu
    },
  })
</script>
