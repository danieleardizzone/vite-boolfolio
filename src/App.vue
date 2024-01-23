<script setup>
import axios from 'axios';
import { createApp } from 'vue';

createApp({
  data() {
    return {
      posts: [],
      BASE_URL: 'http://127.0.0.1:8000/api'
    }
  }, methods: {
    fetchProjects() {
      axios.get(`${this.BASE_URL}/projects`)
        .then((res) => {
          console.log(res)
        })
    }
  }, created() {
    this.fetchProjects();
  }
})
</script>

<template>
  <div id="app">
    <a href="https://vitejs.dev" target="_blank">
      <img src="/vite.svg" class="logo" alt="Vite logo" />
    </a>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>
  </div>
</template>

<style scoped></style>
