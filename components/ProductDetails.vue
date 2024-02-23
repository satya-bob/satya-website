
import type productCard from './productCard.vue';

import type productCard from './productCard.vue';
<template>
    <div class="product-details">
      <div class="product-image-container">
        <img :src="product.image" alt="Product Image">
      </div>
      <div class="product-info">
        <h2>{{ product.title }}</h2>
        <h3>Price: ${{ product.price }}</h3>
        <h3>ID: {{ product.id }}</h3>
        <p>{{ product.description }}</p>
      </div>
    </div>
  </template>
  
  <script setup>
  const { product } = defineProps(["product"]);
  </script>


