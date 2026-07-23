# ✨ Aroma Noire — Luxury Fragrance Storefront

[![Vercel Deployment](https://img.shields.io/badge/Vercel-Live%20Demo-black?style=for-the-badge&logo=vercel)](https://aroma-noire.vercel.app)
[![Firebase](https://img.shields.io/badge/Firebase-Firestore%20%26%20Auth-orange?style=for-the-badge&logo=firebase)](https://firebase.google.com/)
[![JavaScript](https://img.shields.io/badge/JavaScript-Browser--Native%20ESM-yellow?style=for-the-badge&logo=javascript)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

> **Live Storefront URL:** [https://aroma-noire.vercel.app](https://aroma-noire.vercel.app)

---

## 📖 Overview

**Aroma Noire** is a high-performance, mobile-first e-commerce storefront crafted for luxury perfumes, attars, and bespoke fragrance creations. Built on a lightweight, no-bundler browser-native ESM architecture, the platform connects seamlessly to **Firebase Firestore** for real-time cloud data management and is deployed on **Vercel** serverless infrastructure.

---

## 🚀 Key Features

* **🌐 Standalone Deep-Link Product Pages (`product.html`):** 
  Utilizes clean query-parameter routing (`product.html?id=PRODUCT_ID`) for shareable direct links, featuring a dual-image scroll-snap gallery (bottle photo + scent notes card) and custom 2–3 line luxury fragrance narratives.
* **⚥ Authentic Unisex Collection:** 
  Dedicated homepage slider highlighting authentic, gender-neutral artisanal creations (sourced directly from Racks C3 & C4, including *OMG, Oud Wood, Shadow Accord, Majestic Oud,* and more).
* **🔄 Contextual "You May Also Like" Recommendation Engine:** 
  Dynamic category-matched recommendation carousel at the bottom of product pages with self-exclusion logic.
* **👆 Whole-Card Interaction UX:** 
  Entire product card acts as an interactive link to view details, while keeping size pill toggles (30ml / 60ml) and "Add to Bag" buttons isolated from accidental triggers.
* **🔎 Live Search & Filter Bar:** 
  Instant keyword matching across product titles, notes, and category mappings (*Best Sellers, Our Creation, Recreations, Attars, Bakhour*).
* **📱 Mobile-First Responsive Design:** 
  Optimized layouts, drawer menus, and horizontal scroll tracks tested seamlessly down to `320px` viewports.
* **🛠️ Cloud Migration Suite:** 
  Built-in admin utility (`/admin/migrate.html`) for one-click catalog seeding and database synchronization.

---

## 🛠️ Tech Stack & Architecture

* **Frontend:** Vanilla JavaScript (Browser-Native ESM via hosted `gstatic.com` builds — zero Webpack/Vite bundler required), HTML5, CSS3 (CSS Variables, Flexbox, Grid).
* **Backend / Database:** Firebase (Cloud Firestore, Authentication, Firebase Storage).
* **Hosting & CDN:** Vercel Serverless Platform.
* **Data Sources:** Centralized JavaScript configuration arrays mapped to live Firestore collections.

---

## 📂 Project Structure

```text
aroma-noire/
├── index.html                 # Primary Storefront Landing Page
├── product.html               # Dynamic Standalone Product Detail Page
├── perfumes.html              # Full Recreations Collection View
├── assets/
│   ├── css/
│   │   └── main.css           # Core Design Tokens, Responsive Layouts, Animations
│   └── js/
│       ├── app.js             # Storefront Logic, Search, Navigation & Sliders
│       ├── firebase-config.js # Centralized Firebase SDK Init & Exports (db, auth)
│       ├── product-detail.js  # Parameter Parsing, Data Hydration & Recommendations
│       └── config.js          # Master Catalog Data, Rack Mappings & Theme Specs
└── admin/
    ├── migrate.html           # Cloud Firestore Seeding & Catalog Sync Utility
    └── dashboard.js           # Admin Management Scripts
