<template>
  <v-app>
    <v-app-bar app color="#FFF9C4">
      <div class="d-flex align-center">
        <v-img
          class="shrink mr-2"
          contain
          :src="require('./assets/origami_logo.png')"
          width="40"
        />

        <h2>HANDMADE STORE</h2>
      </div>

      <v-spacer></v-spacer>
      <v-btn text @click="$router.push('cart')">
        <v-icon>mdi-cart-outline</v-icon>
        <span class="ml-2">Cart</span>
      </v-btn>
      <v-btn text @click="alertLogin()">
        <v-icon>mdi-account</v-icon>
        <span class="ml-2">Login</span>
      </v-btn>
    </v-app-bar>

    <v-main style="padding: 0">
      <router-view />
    </v-main>
  </v-app>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component
export default class App extends Vue {
  alertLogin() {
    alert('login');
  }
}
</script>
