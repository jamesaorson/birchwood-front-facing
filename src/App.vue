<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>

    <div class="navbar">
      <RouterLink class="navbar-item" :to="'/'">Home</RouterLink>
      <RouterLink class="navbar-item" :to="'/blog'">Blog</RouterLink>
    </div>
  </header>

  <RouterView />
</template>

<style>
* {
  border: 1px solid red;
}

.navbar {
  color: white;
  display: flex;
  flex-direction: row;
  justify-content: center;
}

.navbar-item {
  padding-left: 5em;
  padding-right: 5em;
}

</style>
