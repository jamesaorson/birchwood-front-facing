<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>

    <div class="wrapper">
      <RouterLink :to="'/'">Home</RouterLink>
      <RouterLink :to="'/blog'">Blog</RouterLink>
    </div>
  </header>

  <RouterView />
</template>

<style scoped>
* {
  border: 1px solid red;
}
</style>
