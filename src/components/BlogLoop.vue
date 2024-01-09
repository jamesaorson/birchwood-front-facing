<template>
  <div v-for="blog in blogs">
    <Blog :blog="blog" />
  </div>
</template>

<script setup lang="ts">
import { defineProps } from "vue";
import type { Blog } from "@/assets/types";

const props: { recipes: string } = defineProps({
  recipes: {
    type: String,
    default: "[]",
  },
});
const blogs: Blog[] = JSON.parse(props.recipes);
</script>

<style scoped></style>
