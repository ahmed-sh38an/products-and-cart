<template>
  <main class="wrapper">
    <h2>Recommended</h2>
    <div class="recommended">

      <ProductCard
        v-for="(product, index) in inventory.slice(0,3)"
        :key="product.id"
        class="card"
        :index="index"
        :product="product"
        :addToCart="addToCart"
      />
    </div>
  </main>
</template>

<script>
import ProductCard from '@/components/ProductCard.vue'

export default {
  components: {
    ProductCard
  },
  name: 'HomeView',
  props: ['inventory', 'addToCart']
}
</script>
