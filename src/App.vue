<template>
  <v-app>
    <v-main>
      <TheNavbar />
      <router-view />
    </v-main>
  </v-app>
</template>
<script setup>
import TheNavbar from "@/components/TheNavbar.vue";
</script>

<style></style>
