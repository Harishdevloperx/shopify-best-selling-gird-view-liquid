# Best Selling – Mixed Collections (Shopify Section)

A fully custom Shopify section that displays products from multiple collections in a unified, responsive grid with advanced UX features like full-card click, AJAX cart, fake ratings, stock sorting, and load-more pagination.

---

## ✨ Features

- 🔀 Merge products from multiple collections
- 📱 Responsive grid (mobile & desktop limits)
- 🏷️ Sale & Sold-Out badges (auto)
- ⭐ Dynamic rating system (ID-based, consistent)
- 💰 Discount percentage + compare price
- 🛒 AJAX Add to Cart (no page reload)
- 🧭 Full card clickable (safe from button conflict)
- 📦 Sold-out products auto-moved to the end
- 🔄 Load More button with JS pagination
- ⚡ Fast, lightweight, no external libraries

---

## ⚙️ Settings

Inside Shopify Customizer:

- **Products on Desktop**  
  Controls how many items load initially on large screens.
- **Products on Mobile**  
  Controls how many items load initially on mobile.

Each block lets you:
- Select one collection
- Combine unlimited collections into one grid

---

## 🧠 Logic Overview

### 1. Stock Priority
Available products appear first.  
Sold-out items are pushed to the bottom using JavaScript sorting.

### 2. Rating System
Ratings are generated using product ID modulus:
```liquid
rating = (product.id % 11) * 0.1 + 4.0
