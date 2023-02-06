<script setup>
import ButtonCounter from './components/ButtonCounter.vue';
import BlogPost from './components/BlogPost.vue';
import { ref } from 'vue';

const posts = ref([
  {id:1, title:'Post 1', descripcion:'Descripción 1'},
  {id:2, title:'Post 2', descripcion:'Descripción 2'},
  {id:3, title:'Post 3', descripcion:'Descripción 3'},
  {id:4, title:'Post 4', descripcion:'Descripción 4'},
])
</script>

<template>
<div class="container">
  <h1>App</h1>
  <!-- <ButtonCounter /> -->
  <BlogPost :key="post.id"  :id="post.id" :title="post.title" :body="post.descripcion" v-for="post in posts"/>
  <!-- <BlogPost  :id="2" title="Post 2" body="descripción 2"/>
  <BlogPost  :id="3" title="Post 3" body="descripción 3"/>
  <BlogPost  :id="4" title="Post 4" body="descripción 4"/> -->
</div>
</template>

<style lang="scss" scoped>
</style>