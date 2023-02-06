<script setup>
import BlogPost from './components/BlogPost.vue';
import { ref } from 'vue';

const posts = ref([
  { id: 1, title: 'Post 1', descripcion: 'Descripción 1' },
  { id: 2, title: 'Post 2', descripcion: 'Descripción 2' },
  { id: 3, title: 'Post 3', descripcion: 'Descripción 3' },
  { id: 4, title: 'Post 4', descripcion: 'Descripción 4' },
])

const favorite = ref("")
const changeFavorite = (post) => { 
  favorite.value = post;
 }
</script>

<template>
  <div class="container">
    <h1>App</h1>
    <h2>Mi post favorito:{{ favorite }}</h2>

    <BlogPost :key="post.id" :id="post.id" :title="post.title" :body="post.descripcion" v-for="post in posts" @click="changeFavorite" />
  </div>
</template>

<style lang="scss" scoped>

</style>