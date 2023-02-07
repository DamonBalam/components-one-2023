<script setup>
import BlogPost from './components/BlogPost.vue';
import { ref } from 'vue';

const posts = ref([])

const favorite = ref("")
const changeFavorite = (post) => {
  favorite.value = post;
}

fetch('https://jsonplaceholder.typicode.com/posts')
  .then(res => res.json())
  .then(data => posts.value = data)

</script>

<template>
  <div class="container">
    <h1>App</h1>
    <h2>Mi post favorito:{{ favorite }}</h2>

    <BlogPost :key="post.id" :id="post.id" :title="post.title" :body="post.descripcion" v-for="post in posts"
      @click="changeFavorite" />
  </div>
</template>

<style lang="scss" scoped>

</style>