<template>
  <div class="product-card">
    <img :src="require(`@/assets/${product.image}`)" alt="Manga Cover" class="product-image" />
    <div class="product-info">
      <h3 class="product-title">{{ product.title }}</h3>
      <p class="product-description">{{ product.description }}</p>
      <p  class="product-price">${{ product.price | formatCurrency }}</p>
      <button @click="addToCart" class="add-to-cart-button">Add to Cart</button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    product: {
      type: Object,
      required: true,
    },
  },
  methods: {
    addToCart() {
      this.$emit('add-to-cart', this.product);
    },
  },
};
</script>

<style scoped>
.product-card {
  width: 30%;
  border: 1px solid #ddd;
  padding: 1rem;
  margin-bottom: 1rem;
  background-color: #333;
  position: relative;
  overflow: hidden;
  transition: transform 0.3s;
}

.product-card:hover {
  transform: scale(1.05);
}

.product-image {
  width: 100%;
  height: auto;
  margin-bottom: 0.5rem;
}

.product-info {
  color: #fff;
}

.product-title {
  font-size: 1.5rem;
  margin-bottom: 0.5rem;
}

.product-description {
  margin-bottom: 0.5rem;
}

.product-price {
  font-size: 1rem;
  margin-bottom: 0.5rem;
}

.add-to-cart-button {
  background-color: #dd2f2f;
  color: #fff;
  padding: 0.5rem 1rem;
  border: none;
  cursor: pointer;
  font-size: 1rem;
  transition: background-color 0.3s;
}

.add-to-cart-button:hover {
  background-color: #aa1f1f;
}
</style>
