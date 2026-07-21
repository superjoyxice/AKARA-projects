# AKARA

AKARA merupakan website landing page yang dibuat menggunakan teknologi **Vue.js 3** dan **Vite** untuk memperkenalkan produk dan dekorasi rumah hasil kerajinan tangan pengrajin lokal Indonesia.

---

## Persyaratan Sistem

Pastikan perangkat telah terpasang:

- Node.js v18 atau versi yang lebih baru
- npm

Untuk mengecek versi:

```bash
node -v
npm -v
```

---

## Instalasi

Clone repository.

```bash
git clone https://github.com/USERNAME/AKARA.git
```

Masuk ke folder project.

```bash
cd AKARA-projects
```

Install seluruh dependency.

```bash
npm install
```

---

## Menjalankan Website

Jalankan development server.

```bash
npm run dev
```

Apabila berhasil, terminal akan menampilkan url seperti berikut.

```
Local:   http://localhost:5173/
```

Buka url tersebut melalui browser.

---

## Teknologi yang Digunakan

- Vue.js 3
- Vite
- JavaScript
- HTML5
- CSS3

---

## Struktur Folder

```
AKARA-projects/
├── src/
│   ├── assets/
│   │   ├── artisans/
│   │   ├── featured/
│   │   ├── products/
│   │   ├── logoWhite.png
│   │   └── mainLogo.png
│   │
│   ├── components/
│   │   ├── Header.vue
│   │   ├── Hero.vue
│   │   ├── Collection.vue
│   │   ├── Artisans.vue
│   │   └── Contact.vue
│   │
│   ├── App.vue
│   ├── main.js
│   └── style.css
│
├── .gitignore
├── index.html
├── package.json
├── package-lock.json
├── README.md
└── vite.config.js
```

---

## Catatan

Project ini tidak menggunakan database maupun backend.

Seluruh tampilan website dibuat menggunakan komponen Vue.js dan CSS.

---
