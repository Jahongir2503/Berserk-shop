<template>
  <div class="main-page">
    <div class="main-content">
      <h2 class="section-title">Popular Manga</h2>


      <div class="product-container">

        <div class="product-card">
          <img src="@/assets/manga.jpg" alt="Manga Cover" class="product-image"/>
          <div class="product-info">
            <h3 class="product-title">Manga Title 1</h3>
            <p class="product-description">Description of the manga...</p>
            <p class="product-price">$19.99</p>
            <button class="add-to-cart-button">Add to Cart</button>
          </div>
        </div>


        <div class="product-card">
          <img src="@/assets/manga2.jpg" alt="Manga Cover" class="product-image"/>
          <div class="product-info">
            <h3 class="product-title">Manga Title 2</h3>
            <p class="product-description">Description of the manga...</p>
            <p class="product-price">$24.99</p>
            <button class="add-to-cart-button">Add to Cart</button>
          </div>
        </div>

        <div class="product-card">
          <img src="@/assets/manga3.jpg" alt="Manga Cover" class="product-image"/>
          <div class="product-info">
            <h3 class="product-title">Manga Title 3</h3>
            <p class="product-description">Description of the manga...</p>
            <p class="product-price">$29.99</p>
            <button class="add-to-cart-button">Add to Cart</button>
          </div>
        </div>

        <div class="product-card">
          <img src="@/assets/manga4.jpg" alt="Manga Cover" class="product-image"/>
          <div class="product-info">
            <h3 class="product-title">Manga Title 4</h3>
            <p class="product-description">Description of the manga...</p>
            <p class="product-price">$22.99</p>
            <button class="add-to-cart-button">Add to Cart</button>
          </div>
        </div>

        <div class="product-card">
          <img src="@/assets/manga5.jpg" alt="Manga Cover" class="product-image"/>
          <div class="product-info">
            <h3 class="product-title">Manga Title 5</h3>
            <p class="product-description">Description of the manga...</p>
            <p class="product-price">$34.99</p>
            <button class="add-to-cart-button">Add to Cart</button>
          </div>
        </div>
        <div class="product-card">
          <img src="@/assets/manga6.jpg" alt="Manga Cover" class="product-image"/>
          <div class="product-info">
            <h3 class="product-title">Manga Title 5</h3>
            <p class="product-description">Description of the manga...</p>
            <p class="product-price">$34.99</p>
            <button class="add-to-cart-button">Add to Cart</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

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
