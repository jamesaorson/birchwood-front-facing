<template>
  <div class="blogtile">
    <div class="titlesection">
      <div class="blog title">{{ props.post.title }}</div>
    </div>
    <div class="blog ingredients">{{ props.post.ingredients }}</div>
    <div class="blog instructions">{{  props.post.instructions }}</div>
    <div class="blog notes">{{  props.post.notes }}</div>
  </div>
</template>

<script setup lang="ts">
import type { Blog } from "@/assets/types"; 


const props = defineProps({
  post: {
    type: Object as () => Blog,
    default: () => {},
  },
});
</script>

<style scoped>
    .blogtile {
        color: black;
        background-color: rgb(201, 204, 206);
        margin: 5px 0px;
        padding: 5px;
        display: flex;
        flex-direction: column;
    }

    .title {
      font-size: larger;
      font-weight: 700;
    }

    .titlesection {
      display: flex;
      justify-content: center;
      padding: 5px;
    }
</style>
