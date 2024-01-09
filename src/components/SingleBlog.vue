<template>
  <div>{{ props.post.ingredients }}</div>
</template>

<script setup lang="ts">
import { defineProps } from "vue";
import type { Blog } from "@/assets/types"; 


const props = defineProps({
  post: {
    type: Object as () => Blog,
    default: () => {},
  },
});
</script>

<style scoped>
    div {
        color: black;
        background-color: white;
    }
</style>
