<template>
  <div v-for="post in blogs" :key="post.id">
    <a :href="`#${post.title}`">{{ post.title }}</a>
  </div>
  <div v-for="post in blogs" :key="post.id">
    <SingleBlog :post="post" />
  </div>
</template>

<script setup lang="ts">
import { defineProps } from "vue";
import SingleBlog from "./SingleBlog.vue";
import type { Blog as BlogType } from "@/assets/types";

const props: { recipes: string } = defineProps({
  recipes: {
    type: String,
    default: "[]",
  },
});
const blogs: BlogType[] = JSON.parse(props.recipes);

</script>

<style scoped>

a {
  color: white;
}

</style>
