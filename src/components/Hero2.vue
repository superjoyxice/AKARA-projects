<script setup>
import rattanbasket from "../assets/featured/rattan-basket.png";
import ceramicvase from "../assets/featured/ceramic-vase.png";
import woodenshelf from "../assets/featured/wooden-shelf.png";
import bedframe from "../assets/featured/bed-frame.png";
import woodentable from "../assets/featured/wooden-table.png";

const products = [
  {
    id: 1,
    img: rattanbasket,
    price: '$ 4.61',
    subprice: 'Rp 82.400',
    name: 'Rattan Basket',
  },
  {
    id: 2,
    img: ceramicvase,
    price: '$ 3.69',
    subprice: 'Rp 65.900',
    name: 'Ceramic Vase',
  },
  {
    id: 3,
    img: woodenshelf,
    price: '$ 97.98',
    subprice: 'Rp 1.750.000',
    name: 'Wooden Shelf',
  },
  {
    id: 4,
    img: bedframe,
    price: '$ 204.36',
    subprice: 'Rp 3.650.000',
    name: 'Bed Frame',
  },
  {
    id: 5,
    img: woodentable,
    price: '$ 14.56',
    subprice: 'Rp 260.000',
    name: 'Wooden Table',
  },
];
</script>

<template>
    <div class="main-container">
        <h1 class="main-text">FEATURED</h1>
        <span class="sub-text">Featured Products</span>

        <div class="products-container">
            <button
              v-for="product in products"
              :key="product.id"
              class="product-card"
            >
                <img
                  :src="product.img"
                  :alt="product.name"
                  class="product-image"
                />
                <div class="product-details">
                    <span class="product-title">{{ product.name }}</span>
                    <span class="product-price">{{ product.price }}</span>
                    <span class="product-subprice">{{ product.subprice }}</span>
                </div>
            </button>
        </div>
    </div>
</template>

<style lang="css" scoped> 
.main-container {
    background-color: #cdb17b;
    min-height: 400px;
    padding: 20px 207px 32px;
}

.main-text {
    color: #f8f5f1;
    font-family: "Cormorant Garamond", serif;
    font-size: 3.5rem;
    letter-spacing: 1.2px;
}

.sub-text {
    display: block;
    color: #f8f5f1;
    font-family: "Inter", sans-serif;
    font-size: 1rem;
    margin-top: 8px;
    margin-bottom: 24px;
}

.products-container {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
}

.product-card {
    width: 212px;
    background: #f0f0f0;
    border-radius: 24px;
    border: none;
    padding: 14px;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 12px;
    box-shadow: 0 16px 32px rgba(0, 0, 0, 0.08);
    cursor: pointer;
    transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.product-card:hover {
    transform: translateY(-4px);
    box-shadow: 0 20px 40px rgba(0, 0, 0, 0.12);
}

.product-image {
    width: 100%;
    height: 148px;
    object-fit: cover;
    border-radius: 18px;
}

.product-details {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 4px;
    text-align: center;
}

.product-title {
    color: #242424;
    font-family: "Inter", sans-serif;
    font-weight: 700;
    font-size: 0.95rem;
}

.product-price {
    color: #4a3428;
    font-family: "Inter", sans-serif;
    font-size: 1rem;
    font-weight: 700;
}

.product-subprice {
    color: #4a3428;
    font-family: "Inter", sans-serif;
    font-size: 0.9rem;
}

</style>