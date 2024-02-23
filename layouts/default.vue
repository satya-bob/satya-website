<template>
    <div>
      <header class="header bg-blue-500 py-4">
        <nav class="nav flex justify-center">
          <NuxtLink to="/" class="nav-link text-white font-bold text-xl hover:text-yellow-400 transition duration-300">Satya Website</NuxtLink>
        </nav>
      </header>
      <div class="content bg-gray-100 px-4 py-8">
        <slot />
      </div>
      <footer class="footer bg-blue-500 py-4">
        <ul class="footer-links flex justify-center">
          <li><NuxtLink to="/" class="footer-link text-white hover:text-yellow-400 transition duration-300">Home</NuxtLink></li>
          <li><NuxtLink to="/about" class="footer-link text-white hover:text-yellow-400 transition duration-300">About</NuxtLink></li>
        </ul>
      </footer>
    </div>
  </template>
  
  <style scoped>
  .header:hover {
    background-color: #3182ce;
  }
  
  .footer:hover {
    background-color: #3182ce;
  }
  
  .nav-link:hover {
    transform: scale(1.05);
  }
  
  .footer-link:hover {
    transform: scale(1.05);
  }
  </style>
  