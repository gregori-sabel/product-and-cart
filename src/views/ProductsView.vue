<template>
  <main class="wrapper">
    <h1>Products</h1>

    <div class="card-container">
      <ProductCart
        v-for="(product, index) in inventory"
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
import ProductCart from '@/components/ProductCart.vue'

export default {
  name: 'ProductsView',
  props: ['inventory', 'addToCart'],
  components: { ProductCart }
}
</script>
