<template>
    <div>
      <h2 class="text-2xl font-bold mb-4">Posts</h2>
      <ul>
        <li v-for="post in posts" :key="post.id" class="mb-4">
          <nuxt-link :to="`/posts/${post.id}`" class="block p-4 rounded-lg shadow-md hover:bg-blue-500 hover:text-white transform transition duration-300 hover:scale-105">
            {{ post.title }}
          </nuxt-link>
        </li>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      posts: {
        type: Array,
        required: true
      }
    }
  }
  </script>
  
  <style scoped>
  /* Set full background color */
  body {
    background-color: #f7fafc; /* You can adjust the color as needed */
  }
  </style>
  