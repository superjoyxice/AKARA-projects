<script setup>
import artisan1 from '../assets/artisans/artisan1.png'
import artisan2 from '../assets/artisans/artisan2.png'
import artisan3 from '../assets/artisans/artisan3.png'
import artisan4 from '../assets/artisans/artisan4.png'
import artisan5 from '../assets/artisans/artisan5.png'

const artisansCard = [
    {
        id:1,
        img:artisan2,
        alt: 'artisan 1'
    },
    {
        id:2,
        img:artisan3,
        alt: 'artisan 2'
    },
    {
        id:3,
        img:artisan4,
        alt: 'artisan 3'
    },
    {
        id:4,
        img:artisan5,
        alt: 'artisan 4'
    }
]
</script>

<template>
    <section id="artisans" class="main-container">
        <div class="img-container">
            <img :src="artisan1" alt="artisan1" class="main-img">
            <div class="fade-overlay" aria-hidden="true"></div>
            <div class="text-container">
                <h1 id="main-text">"Every handcrafted piece the soul of its maker."</h1>
            </div>
        </div>

        <div class="profile-container">
            <button class="profile"
            v-for="artisan in artisansCard"
            :key="artisan.id">
        <img class="profile-img"
        :src="artisan.img"
        :alt="artisan.alt">
        </button>
        </div>
    </section>
</template>

<style lang="css" scoped>
.main-container {
    background-color: #cdb17b;
    min-height: 1040px;
}
.img-container {
    background-color: rgb(255, 255, 255);
    width: 100%;
    height: 570px;
    display: flex;
    position: relative;
}
.main-img {
    width: 65%;
    height: 100%;
    object-fit: cover;
    display: block;
}
#main-text {
    position: absolute;
    left: 62%;
    top: 0;
    bottom: 50px;
    width: calc(35% - 32px);
    margin: auto 16px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 70px;
    font-family: "Cormorant Garamond", serif;
    letter-spacing: 1px;
    text-align: center;
    z-index: 4;
}
.text-container {
    z-index: 5;
}

.fade-overlay {
    position: absolute;
    left: 0;
    top: 0;
    bottom: 0;
    width: 65%;
    pointer-events: none;
    z-index: 3;
    background: linear-gradient(90deg, rgba(255,255,255,0) 60%, rgba(255,255,255,1) 90%);
}

.profile-container {

    display: flex;
    justify-content: center;
    gap: 80px;
    padding: 50px 60px;
    flex-wrap: wrap;
}

.profile {
    background: #f6f3f0;
    width: 340px;
    height: 340px;
    border-radius: 22px;
    display: flex;
    align-items: center;
    justify-content: center;
    border: none;
    cursor: pointer;
    padding: 12px;
    box-shadow: 0 4px 6px rgba(0,0,0,0.06);
    transition: transform 180ms cubic-bezier(.2,.9,.2,1), box-shadow 180ms cubic-bezier(.2,.9,.2,1);
}

.profile-img {
    width: 300px;
    height: 300px;
    border-radius: 12px;
    object-fit: cover;
    background: #b0905b;
    display: block;
}

.profile:hover {
    transform: translateY(-10px) scale(1.02);
    box-shadow: 0 18px 40px rgba(0,0,0,0.18);
}

@media (max-width: 600px) {
    .profile-container {
        gap: 20px;
        padding: 24px;
    }
    .profile {
        width: 220px;
        height: 220px;
    }
    .profile-img {
        width: 180px;
        height: 180px;
    }
}
</style>