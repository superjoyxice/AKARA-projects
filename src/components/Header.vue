<script setup>
import logoWhite from "../assets/logoWhite.png";

const gotohome = () => {
  document.getElementById('home')?.scrollIntoView({ behavior: 'smooth' });
};

const gotocollection = () => {
  document.getElementById('collection')?.scrollIntoView({ behavior: 'smooth' });
}

const gotoartisans = () => {
  document.getElementById('artisans')?.scrollIntoView({ behavior: 'smooth' });
}

const gotocontact = () => {
  document.getElementById('contact')?.scrollIntoView({ behavior : 'smooth' })
}
</script>

<template>
  <header class="header">
    <div class="brand">
      <img :src="logoWhite" alt="AKARA Logo" class="logo" />
      <h2 class="main-text">AKARA</h2>
    </div>
    
    <nav class="nav-menu">
      <button class="nav-button" @click="gotohome">Home</button>
      <button class="nav-button" @click="gotoartisans">Aritsans</button>
      <button class="nav-button" @click="gotocontact">Contact</button>
    </nav>

    <button class="explore" @click="gotocollection">Explore</button>
  </header>
</template>

<style scoped>
.header {
  width: 100%;
  min-height: 80px;
  background-color: black;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0 45px;
  box-sizing: border-box;
  position: fixed;
  top: 0;
  z-index: 1000;
  gap: 24px;
}

.brand {
  display: flex;
  align-items: center;
  flex-shrink: 0;
}

.logo {
  height: 45px;
  width: auto;
  margin-left: 0;
}

.main-text {
  margin-left: 11px;
  color: white;
  font-family: "Cormorant Garamond", serif;
  font-size: 28px;
}

.nav-menu {
  display: flex;
  align-items: center;
  justify-content: right;
  flex: 1;
  gap: clamp(24px, 4vw, 67px);
  margin: 0;
  margin-right: 40px;
}

.nav-button {
  background: none;
  border: none;
  color: white;
  font-family: "Inter", sans-serif;
  font-size: 20px;
  cursor: pointer;
  transition: 0.2s ease;
  padding: 0;
}

.nav-button:hover {
  transform: scale(1.1);
}

.explore {
  background: white;
  color: black;
  border: none;
  border-radius: 8px;
  padding: 10px 18px;
  font-family: "Inter", sans-serif;
  font-size: 20px;
  cursor: pointer;
  transition: 0.2s;
  margin-right: 0;
  flex-shrink: 0;
}

.explore:hover {
  background: black;
  color: white;
}
</style>