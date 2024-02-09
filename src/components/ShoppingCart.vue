<script setup>
export default {
  props: {
    cart: {
      type: Array,
      default: () => [],
    },
  },
};
</script>

<template>
  <div class="shopping-cart">
    <h2 class="section-title">Shopping Cart</h2>
    <div v-if="cart.length === 0">Your cart is empty.</div>
    <div v-else>
      <div class="cart-item" v-for="item in cart" :key="item.id">
        <img :src="item.image" :alt="item.title" class="cart-item-image"/>
        <div class="cart-item-info">
          <h3 class="cart-item-title">{{ item.title }}</h3>
          <p class="cart-item-price">${{ item.price.toFixed(2) }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>

</style>