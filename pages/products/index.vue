<template>
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4">
      <div v-for="p in products" :key="p.id" class="overflow-hidden rounded-lg shadow-lg hover:shadow-xl transform hover:scale-105 transition-all duration-300">
        <ProductCard :product="p" />
        <div class="absolute inset-0 bg-black bg-opacity-50 opacity-0 hover:opacity-100 transition-opacity duration-300"></div>
        <div class="absolute inset-0 flex items-center justify-center text-white opacity-0 hover:opacity-100 transition-opacity duration-300">
          <h2 class="text-lg font-semibold">{{ p.title }}</h2>
          <p class="text-sm">{{ p.description }}</p>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  const { data: products } = await useFetch('https://fakestoreapi.com/products');
  </script>
  
  <style scoped>
  /* You can also add custom styles here if needed */
  </style>
  