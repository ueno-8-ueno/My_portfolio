<script setup lang="ts">
import { RouterView } from 'vue-router'
import Header from './components/Header.vue';
</script>

<template>
  <v-app>
    <Header class="change-font"></Header>
    <v-main class="change-font top-outline">
      <RouterView></RouterView>
    </v-main>
  </v-app>
</template>

<style>
@import url("https://fonts.googleapis.com/css2?family=Murecho:wght@500;900&display=swap");

.change-font {
  font-family: "Murecho", sans-serif;
}

.top-outline{
  width: 100%;
}
</style>