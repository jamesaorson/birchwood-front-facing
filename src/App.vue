<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>

    <div class="navbar">
      <div class="name">
        Brandon's Recipe Collection
      </div>
      <div class="nav-tabs">
        <RouterLink class="navbar-item" :to="'/'">Home</RouterLink>
        <RouterLink class="navbar-item" :to="'/blog'">Blog</RouterLink>
      </div>
    </div>
  </header>

  <RouterView />
</template>

<style>
* {
  border: 1px solid red;
}

.navbar {
  background-color: #A4BEF3;
  display: flex;
  flex-direction: row;
  justify-content: space-around;
}

.navbar-item {
  padding-left: 5em;
  padding-right: 5em;
  padding-top: 1em;
  padding-bottom: 1em;
}

</style>
