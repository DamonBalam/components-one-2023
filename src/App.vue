<script setup>
import ButtonCounter from './components/ButtonCounter.vue';
import BlogPost from './components/BlogPost.vue';
</script>

<template>
<div class="container">
  <h1>App</h1>
  <ButtonCounter />
  <BlogPost class="mt-5" title="Post 1"/>
  <BlogPost  title="Post 2"/>
  <BlogPost  title="Post 3"/>
  <BlogPost  title="Post 4"/>
</div>
</template>

<style lang="scss" scoped>

</style>