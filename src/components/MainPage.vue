<template>
  <div class="main-page">
    <div class="main-content">
      <h2 class="section-title">Popular Manga</h2>
      <ProductList :products="products" @add-to-cart="addToCart"/>
    </div>
  </div>
</template>

<script>
import ProductList from '@/components/ProductList.vue';

export default {
  components: {
    ProductList,
  },
  data() {
    return {
      products: [
        {
          id: 1,
          title: 'Berserk Tom:27',
          description: 'Popular manga by mangaki Kantaro Miura..',
          price: 19.99,
          image: require('@/assets/manga.jpg'),
        },
        // Другие продукты...
      ],
    };
  },
  methods: {
    addToCart(product) {
      console.log('Added to cart:', product);
    },
  },
};
</script>
<style scoped>
.main-page {
  background: url('@/assets/berserk-kleymo.jpg') no-repeat center center fixed;
  background-size: cover;
  color: #fff;
  padding-top: 2rem;
  min-height: 100vh;
}

.main-content {
  width: 80%;
  margin: 0 auto;
}

.product-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}

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

.section-title {
  color: #dd2f2f;
  font-size: 2rem;
  text-align: center;
  margin-bottom: 1rem;
}

.product-title {
  font-size: 1.5rem;
  margin-bottom: 0.5rem;
  color: #fff;
}

.product-description {
  margin-bottom: 0.5rem;
  color: #ddd;
}

.product-price {
  font-size: 1rem;
  margin-bottom: 0.5rem;
  color: #fff;
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
