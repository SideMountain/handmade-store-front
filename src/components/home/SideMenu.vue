<template>
  <div>
    <v-list>
      <v-list-item v-for="category in categories" :key="category.id">
        <v-list-item-title class="py-1">
          <v-btn block text x-large @click="alertCategory(category.id)">
            <v-icon>{{category.icon}}</v-icon>
            {{category.name}}
          </v-btn>
        </v-list-item-title>
      </v-list-item>
    </v-list>
  </div>
</template>

<script lang="ts">
  import { Component, Vue } from 'vue-property-decorator'

  @Component
  export default class SideMenu extends Vue {
    categories = [
      {
        id: '001',
        name: 'category1',
        icon: 'mdi-account'
      },
      {
        id: '002',
        name: 'category2',
        icon: 'mdi-account'
      },
      {
        id: '003',
        name: 'category3',
        icon: 'mdi-account'
      },
      {
        id: '004',
        name: 'category4',
        icon: 'mdi-account'
      },
      {
        id: '005',
        name: 'category5',
        icon: 'mdi-account'
      }
    ];

    alertCategory(id: string): void {
      alert('categoryId is ' + id);
    }
  }
</script>