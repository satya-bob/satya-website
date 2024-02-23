<template>
    <div class="home-page-container bg-cover bg-center min-h-screen flex justify-center items-center">
      <div class="text-center text-white">
        <h1 class="text-5xl font-bold mb-4 hover:text-blue-500 transition duration-300">Welcome to Our Website!</h1>
        <p class="text-lg mb-8">This is the home page of our website.</p>
        
        <div class="grid grid-cols-1 gap-4 sm:grid-cols-3">
          <NuxtLink to="/posts" class="text-xl font-semibold mb-2 hover:text-blue-500 transition duration-300">Posts</NuxtLink>
          <NuxtLink to="/weather" class="text-gray-600 hover:text-blue-500 transition duration-300">Weather</NuxtLink>
          <NuxtLink to="/products" class="text-gray-600 hover:text-blue-500 transition duration-300">Products</NuxtLink>
        </div>
      </div>
    </div>
  </template>
  
  <style scoped>
  .home-page-container {
    background-color: rgba(0, 0, 0, 0.5); /* Semi-transparent black overlay for better text readability */
    background-image: url('/path/to/your/background-image.jpg');
  }
  
  /* Styles for hover effects on links */
  .home-page-container a:hover {
    transform: translateY(-2px); /* Move the link slightly upward on hover */
  }
  
  </style>
  
  