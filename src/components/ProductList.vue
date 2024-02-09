<!-- ProductList.vue -->
<template>
  <div class="product-container">
    <ProductCard v-for="product in products" :key="product.id" :product="product" @add-to-cart="addToCart" />
  </div>
</template>

<script>
import ProductCard from '@/components/ProductCard.vue';
import products from '@/data/products.js';

export default {
  components: {
    ProductCard,
  },
  data() {
    return {
      products: products,
    };
  },
  methods: {
    addToCart(product) {
      this.$emit('add-to-cart', product);
    },
  },
};
</script>

<style scoped>
.product-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  margin-top: 2rem;
}

</style>
