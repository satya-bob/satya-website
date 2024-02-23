<!-- pages/index.vue -->
<template>
    <div>
      <h1>News Headlines</h1>
      <ul>
        <li v-for="(article, index) in articles" :key="index">
          <h2>{{ article.title }}</h2>
          <p>{{ article.description }}</p>
          <p><a :href="article.url" target="_blank">Read more</a></p>
        </li>
      </ul>
    </div>
  </template>
  
  <script setup>
  import { ref, onMounted } from 'vue';
  
  const articles = ref([]);
  
  onMounted(async () => {
    try {
      const response = await fetch('https://newsapi.org/v2/top-headlines?country=us&apiKey=e5bd758a5c804d6590f92aec18b502c4');
      const data = await response.json();
      articles.value = data.articles;
    } catch (error) {
      console.error('Error fetching news:', error);
    }
  });
  </script>
  