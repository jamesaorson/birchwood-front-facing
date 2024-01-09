<template>
  <div>${{ props.blog.ingredients }}</div>
</template>

<script setup lang="ts">
import { defineProps } from "vue";
import type { Blog } from "@/assets/types";
const props = defineProps({
  blog: {
    type: Object as () => Blog,
    default: () => {},
  },
});
</script>

<style scoped>

</style>
