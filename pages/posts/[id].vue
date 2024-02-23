<template>
    <div class="bg-gray-100 p-8 rounded-lg shadow-lg hover:shadow-xl">
      <h2 class="text-2xl font-bold mb-4">{{ post.title }}</h2>
      <p class="text-gray-700">{{ post.content }}</p>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        post: {}
      };
    },
    async mounted() {
      // Fetch post data based on route params
      const postId = this.$route.params.id;
      // You can fetch post data from an API using Axios or fetch here
      // For demonstration purposes, we'll use a dummy post
      this.post = { id: postId, title: 'Dummy Post', content: 'This is a dummy post.' };
    }
  };
  </script>
  
  <style scoped>
  .bg-gray-100 {
    background-color: #f3f4f6;
  }
  
  .rounded-lg {
    border-radius: 0.5rem;
  }
  
  .shadow-lg {
    box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
  }
  
  .hover\:shadow-xl:hover {
    transition: all 0.3s ease;
    box-shadow: 0 8px 12px -4px rgba(0, 0, 0, 0.15), 0 4px 6px -2px rgba(0, 0, 0, 0.1);
  }
  </style>
  