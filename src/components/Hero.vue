<script setup>
import { ref, computed, onMounted, onUnmounted } from 'vue';
import basket from '../assets/featured/rattan-basket.png';
import vase from '../assets/featured/ceramic-vase.png';
import table from '../assets/featured/wooden-table.png';
import bedFrame from '../assets/featured/bed-frame.png';
import shelf from '../assets/featured/wooden-shelf.png';

const slides = [
  { image: basket, title: 'Rattan Basket', description: 'Handcrafted basket for home styling' },
  { image: vase, title: 'Ceramic Vase', description: 'Elegant vase for modern decor' },
  { image: table, title: 'Wooden Table', description: 'Solid wood table with natural finish' },
  { image: bedFrame, title: 'Bed Frame', description: 'Comfortable and stylish bedroom piece' },
  { image: shelf, title: 'Wooden Shelf', description: 'Rustic shelf for display and storage' }
];

const activeIndex = ref(0);
const activeSlide = computed(() => slides[activeIndex.value]);

const setSlide = (index) => {
  activeIndex.value = index;
};

let intervalId = null;

const startAutoScroll = () => {
  intervalId = setInterval(() => {
    activeIndex.value = (activeIndex.value + 1) % slides.length;
  }, 3500);
};

const stopAutoScroll = () => {
  if (intervalId) {
    clearInterval(intervalId);
    intervalId = null;
  }
};

onMounted(() => {
  startAutoScroll();
});

onUnmounted(() => {
  stopAutoScroll();
});

const gotocollection = () => {
  document.getElementById('collection')?.scrollIntoView({ behavior: 'smooth' });
}
</script>

<template>
  <section class="hero-section" id="home">
    <div class="hero-content">
      <div class="hero-copy">
        <p class="eyebrow">LOCAL CRAFTSMANSHIP</p>
        <h1>WORLD CLASS COMFORT</h1>
        <p class="hero-description">
          AKARA brings Indonesia's finest handcrafted home decor to the world. Every piece is thoughtfully made by local artisans, blending timeless heritage with contemporary design to create beautiful spaces that tell meaningful stories.
        </p>
        <button class="hero-button" @click="gotocollection">Explore Collection</button>
      </div>

      <div class="carousel">
        <div class="carousel-image-wrapper">
          <transition name="slide" mode="out-in">
            <img
              :key="activeSlide.image"
              :src="activeSlide.image"
              :alt="activeSlide.title"
              class="carousel-image"
            />
          </transition>
        </div>
        <div class="carousel-info">
          <h2>{{ activeSlide.title }}</h2>
          <p>{{ activeSlide.description }}</p>
        </div>
        <div class="carousel-dots">
          <button
            v-for="(_, index) in slides"
            :key="index"
            :class="['dot', { active: index === activeIndex }]"
            @click="setSlide(index)"
            aria-label="Show slide"
          />
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.hero-section {
  background: #f8f5f1;
  padding: 132px 48px 56px;
}

.hero-content {
  max-width: 1240px;
  margin: 0 auto;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 48px;
}

.hero-copy {
  max-width: 540px;
}

.eyebrow {
  color: #4a3428;
  font-size: 0.95rem;
  letter-spacing: 0.24em;
  text-transform: uppercase;
  margin-bottom: 24px;
  font-size: 30px;
}

.hero-copy h1 {
  color: #4a3428;
  font-family: 'Cormorant Garamond', serif;
  font-size: 4.8rem;
  line-height: 1.05;
  margin: 0 0 24px;
}

.hero-description {
  color: #2d2d2d;
  font-family: 'Playfair Display', serif;
  font-size: 1.1rem;
  line-height: 1.75;
  margin-bottom: 36px;
}

.hero-button {
  background: #1e3a5f;
  color: #fff;
  border: none;
  border-radius: 10px;
  padding: 16px 28px;
  font-family: 'Inter', sans-serif;
  font-size: 1rem;
  letter-spacing: 0.03em;
  cursor: pointer;
  transition: transform 0.2s ease, background 0.2s ease;
}

.hero-button:hover {
  background: #162d4c;
}

.carousel {
  width: 540px;
  display: flex;
  flex-direction: column;
  gap: 18px;
}

.carousel-image-wrapper {
  position: relative;
  overflow: hidden;
  border-radius: 28px;
  box-shadow: 0 24px 60px rgba(0, 0, 0, 0.12);
  min-height: 380px;
}

.carousel-image {
  display: block;
  width: 100%;
  height: 380px;
  object-fit: cover;
}

.slide-enter-active,
.slide-leave-active {
  transition: transform 0.5s ease, opacity 0.5s ease;
  position: absolute;
  width: 100%;
}

.slide-enter-from {
  transform: translateX(100%);
  opacity: 0;
}

.slide-enter-to {
  transform: translateX(0);
  opacity: 1;
}

.slide-leave-from {
  transform: translateX(0);
  opacity: 1;
}

.slide-leave-to {
  transform: translateX(-100%);
  opacity: 0;
}

.carousel-info h2 {
  margin: 0;
  color: #1e3a5f;
  font-family: 'Cormorant Garamond', serif;
  font-size: 1.6rem;
}

.carousel-info p {
  margin: 8px 0 0;
  color: #2d2d2d;
  font-family: 'Inter', sans-serif;
  font-size: 0.98rem;
  line-height: 1.6;
}

.carousel-dots {
  display: flex;
  gap: 10px;
  justify-content: center;
}

.dot {
  width: 14px;
  height: 14px;
  border-radius: 50%;
  border: none;
  background: rgba(0, 0, 0, 0.2);
  cursor: pointer;
  transition: background 0.2s ease;
}

.dot.active {
  background: #1e3a5f;
}

@media (max-width: 980px) {
  .hero-content {
    flex-direction: column-reverse;
    text-align: center;
  }

  .hero-copy h1 {
    font-size: 3rem;
  }

  .carousel {
    width: 100%;
  }

  .carousel-image {
    height: 300px;
  }
}
</style>