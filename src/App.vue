<script setup>

import ButtonCounter from "./components/ButtonCounter.vue"
import BlogPost from "./components/BlogPost.vue"
import { ref } from "vue";

const  posts = ref ([
  {title:'Post 1', id: 1, body: 'Descripcion 1'},
  {title:'Post 2', id: 2, body: 'Descripcion 2'},
  {title:'Post 3', id: 3, body: 'Descripcion 3'},
  {title:'Post 4', id: 4 }
])
const favorito = ref('')
const cambiarFavorito = () => {
  favorito.value.post

}


</script>

<template>
  <h1>APP</h1>
  <h2>
    Mi post favorito
  </h2>

    <ButtonCounter></ButtonCounter>
    <br>
    <BlogPost 
    v-for="post in posts"
    :key="post.id"
    :title="post.title" 
    :id="post.id" 
    :body="post.body" 
></BlogPost>
  
</template>
<style>

</style>