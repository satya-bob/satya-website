
import type { ProductCard } from '#build/components';

import type { ProductCard } from '#build/components';

import type { ProductCard } from '#build/components';

  
  <template>
    <div class="product-item">
      <img :src="product.image" alt="Product Image">
      <NuxtLink :to="`/products/${product.id}`" class="details-link">View Details</NuxtLink>
    </div>
  </template>
  
  <script setup>
  const { product } = defineProps(['product']);
  </script>