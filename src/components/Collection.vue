<script setup>
import { computed, ref } from 'vue';

import bedroom1 from '../assets/products/bedroom/bedroom1.png';
import bedroom2 from '../assets/products/bedroom/bedroom2.png';
import bedroom3 from '../assets/products/bedroom/bedroom3.png';
import bedroom4 from '../assets/products/bedroom/bedroom4.png';
import bedroom5 from '../assets/products/bedroom/bedroom5.png';
import bedroom6 from '../assets/products/bedroom/bedroom6.png';
import decor1 from '../assets/products/decor/decor1.png';
import decor2 from '../assets/products/decor/decor2.png';
import decor3 from '../assets/products/decor/decor3.png';
import decor4 from '../assets/products/decor/decor4.png';
import decor5 from '../assets/products/decor/decor5.png';
import decor6 from '../assets/products/decor/decor6.png';
import lightning1 from '../assets/products/lightning/lightning1.png';
import lightning2 from '../assets/products/lightning/lightning2.png';
import lightning3 from '../assets/products/lightning/lightning3.png';
import lightning4 from '../assets/products/lightning/lightning4.png';
import lightning5 from '../assets/products/lightning/lightning5.png';
import lightning6 from '../assets/products/lightning/lightning6.png';
import livingroom1 from '../assets/products/living room/living-room1.png';
import livingroom2 from '../assets/products/living room/living-room2.png';
import livingroom3 from '../assets/products/living room/living-room3.png';
import livingroom4 from '../assets/products/living room/living-room4.png';
import livingroom5 from '../assets/products/living room/living-room5.png';
import livingroom6 from '../assets/products/living room/living-room6.png';

const selectedCategory = ref('Living Room');

const categories = ['Living Room', 'Bedroom', 'Decor', 'Lighting'];

const products = [
  { id: 1, name: 'Rattan Armchair', category: 'Living Room', price: 229, subprice: 'Rp 3.732.700', image: livingroom1, rating: 4.9, reviews: 128 },
  { id: 2, name: 'Wooden Coffee Table', category: 'Living Room', price: 189, subprice: 'Rp 3.080.700', image: livingroom2, rating: 4.8, reviews: 84 },
  { id: 3, name: 'TV Console', category: 'Living Room', price: 349, subprice: 'Rp 5.688.700', image: livingroom3, rating: 4.8, reviews: 76 },
  { id: 4, name: 'Lounge Chair', category: 'Living Room', price: 279, subprice: 'Rp 4.547.700', image: livingroom4, rating: 4.7, reviews: 41 },
  { id: 5, name: 'Teak Side Table', category: 'Living Room', price: 129, subprice: 'Rp 2.102.700', image: livingroom5, rating: 4.8, reviews: 88 },
  { id: 6, name: 'Wooden Bookshelf', category: 'Living Room', price: 259, subprice: 'Rp 4.221.700', image: livingroom6, rating: 4.9, reviews: 52 },

  { id: 7, name: 'Solid Wood Bed Frame', category: 'Bedroom', price: 599, subprice: 'Rp 9.763.700', image: bedroom1, rating: 4.9, reviews: 63 },
  { id: 8, name: 'Wooden Bedside Table', category: 'Bedroom', price: 149, subprice: 'Rp 2.428.700', image: bedroom2, rating: 4.7, reviews: 44 },
  { id: 9, name: 'Linen Bedding Set', category: 'Bedroom', price: 99, subprice: 'Rp 1.613.700', image: bedroom3, rating: 4.8, reviews: 37 },
  { id: 10, name: 'Rattan Headboard', category: 'Bedroom', price: 189, subprice: 'Rp 3.080.700', image: bedroom4, rating: 4.8, reviews: 29 },
  { id: 11, name: 'Wooden Wardrobe', category: 'Bedroom', price: 799, subprice: 'Rp 13.023.700', image: bedroom5, rating: 4.9, reviews: 18 },
  { id: 12, name: 'Bedroom Bench', category: 'Bedroom', price: 179, subprice: 'Rp 2.917.700', image: bedroom6, rating: 4.7, reviews: 21 },

  { id: 13, name: 'Ceramic Vase', category: 'Decor', price: 39, subprice: 'Rp 635.700', image: decor1, rating: 4.8, reviews: 96 },
  { id: 14, name: 'Woven Rattan Basket', category: 'Decor', price: 49, subprice: 'Rp 798.700', image: decor2, rating: 4.7, reviews: 58 },
  { id: 15, name: 'Wooden Sculpture', category: 'Decor', price: 69, subprice: 'Rp 1.124.700', image: decor3, rating: 4.6, reviews: 33 },
  { id: 16, name: 'Macrame Wall Hanging', category: 'Decor', price: 59, subprice: 'Rp 961.700', image: decor4, rating: 4.6, reviews: 27 },
  { id: 17, name: 'Terracotta Planter', category: 'Decor', price: 45, subprice: 'Rp 733.500', image: decor5, rating: 4.8, reviews: 41 },
  { id: 18, name: 'Batik Cushion Cover', category: 'Decor', price: 35, subprice: 'Rp 570.500', image: decor6, rating: 4.5, reviews: 12 },

  { id: 19, name: 'Rattan Pendant Lamp', category: 'Lighting', price: 139, subprice: 'Rp 2.265.700', image: lightning1, rating: 4.8, reviews: 51 },
  { id: 20, name: 'Wooden Table Lamp', category: 'Lighting', price: 89, subprice: 'Rp 1.450.700', image: lightning2, rating: 4.7, reviews: 34 },
  { id: 21, name: 'Bamboo Hanging Lamp', category: 'Lighting', price: 119, subprice: 'Rp 1.939.700', image: lightning3, rating: 4.6, reviews: 28 },
  { id: 22, name: 'Wooden Floor Lamp', category: 'Lighting', price: 199, subprice: 'Rp 3.243.700', image: lightning4, rating: 4.8, reviews: 19 },
  { id: 23, name: 'Bedside Lamp', category: 'Lighting', price: 79, subprice: 'Rp 1.287.700', image: lightning5, rating: 4.6, reviews: 22 },
  { id: 24, name: 'Artisan Ceiling Light', category: 'Lighting', price: 169, subprice: 'Rp 2.754.700', image: lightning6, rating: 4.8, reviews: 14 },
];

const filteredProducts = computed(() => {
  return products.filter((product) => product.category === selectedCategory.value);
});
</script>

<template>
    <div id="collection" class="main-container">
      <div class="collection-header">
        <p class="collection-label">OUR COLLECTION</p>
        <h1 class="collection-title">Discover Handcrafted Pieces<br>Inspired by Indonesian Artisans</h1>
        <p class="collection-description">
          Timeless furniture and home decor, thoughtfully crafted using sustainable<br>
          materials and traditional techniques.
        </p>
      </div>

      <div class="filter-buttons">
        <button
          v-for="category in categories"
          :key="category"
          :class="['filter-btn', { active: selectedCategory === category }]"
          @click="selectedCategory = category"
        >
          {{ category }}
        </button>
      </div>

      <div class="products-grid">
        <div v-for="product in filteredProducts" :key="product.id" class="product-card">
          <div class="product-image-wrapper">
            <img :src="product.image" :alt="product.name" class="product-image" />
          </div>
          <div class="product-info">
            <h3 class="product-name">{{ product.name }}</h3>
            <p class="product-category">{{ product.category }}</p>
            <p class="product-price">${{ product.price }}</p>
            <p class="product-subprice">{{ product.subprice }}</p>
            <div class="product-footer">
              <div class="rating">
                <span class="stars">★★★★½</span>
                <span class="review-count">({{ product.reviews }})</span>
              </div>
              <button class="explore-btn">Buy Now →</button>
            </div>
          </div>
        </div>
      </div>
    </div>
</template>

<style lang="css" scoped>
.main-container {
    background-color: #f8f5f1;
    padding: 20px 20px;
    min-height: 850px;
}

.collection-header {
    text-align: center;
    margin-bottom: 40px;
}

.collection-label {
    font-size: 18px;
    letter-spacing: 1.8px;
    color: black;
    margin-bottom: 10px;
    text-transform: uppercase;
    font-family: "Inter", sans-serif;
}

.collection-title {
    font-size: 48px;
    font-weight: 600;
    color: #000000;
    margin: 15px 0;
    line-height: 1.2;
    font-family: "Cormorant Garamond", serif;
    letter-spacing: 0.2px;
}

.collection-description {
    font-size: 14px;
    color: #666;
    max-width: 600px;
    margin: 20px auto;
    line-height: 1.6;
}

.filter-buttons {
    display: flex;
    justify-content: center;
    gap: 12px;
    margin: 40px 0;
    flex-wrap: wrap;
}

.filter-btn {
    padding: 10px 24px;
    border: 1px solid #ddd;
    background: white;
    border-radius: 4px;
    cursor: pointer;
    font-size: 14px;
    transition: all 0.3s ease;
    font-family: "Inter", sans-serif;
    letter-spacing: 0.6px;
}

.filter-btn.active {
    background-color: #1a3a52;
    color: white;
    border-color: #1a3a52;
}

.filter-btn:hover:not(.active) {
    border-color: #999;
}

.products-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 30px;
    max-width: 1200px;
    margin: 50px auto;
    font-family: "Playfair Display", serif;
}

.product-card {
    background: white;
    border-radius: 8px;
    overflow: hidden;
    transition: transform 0.3s ease;
}

.product-card:hover {
    transform: translateY(-5px);
}

.product-image-wrapper {
    position: relative;
    width: 100%;
    height: 300px;
    overflow: hidden;
    background: #f5f5f5;
}

.product-image {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.product-info {
    padding: 20px;
}

.product-name {
    font-size: 18px;
    font-weight: 600;
    color: #1a1a1a;
    margin-bottom: 5px;
}

.product-category {
    font-size: 13px;
    color: #999;
    margin-bottom: 12px;
}

.product-price {
    font-size: 20px;
    font-weight: 600;
    color: #1a1a1a;
    margin-bottom: 4px;
}

.product-subprice {
    font-size: 14px;
    color: #777;
    margin-bottom: 15px;
}

.product-footer {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.rating {
    display: flex;
    align-items: center;
    gap: 6px;
    font-size: 12px;
}

.stars {
    color: #f0ad4e;
    font-size: 14px;
}

.review-count {
    color: #999;
}

.explore-btn {
    background-color: #1a3a52;
    color: white;
    border: none;
    padding: 8px 16px;
    border-radius: 4px;
    cursor: pointer;
    font-size: 12px;
    transition: background-color 0.3s ease;
}

.explore-btn:hover {
    background-color: #142d40;
}

@media (max-width: 768px) {
    .products-grid {
        grid-template-columns: repeat(2, 1fr);
        gap: 20px;
    }

    .collection-title {
        font-size: 32px;
    }
}

@media (max-width: 480px) {
    .products-grid {
        grid-template-columns: 1fr;
    }

    .filter-buttons {
        gap: 8px;
    }

    .filter-btn {
        padding: 8px 16px;
        font-size: 12px;
    }
}
</style>
