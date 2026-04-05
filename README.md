# 🌾 FarmRise — Smart Farming Platform

A fully client-side, single-file agricultural web application that gives farmers real-time mandi prices, crop advisory, an agri shop, government schemes, and nearby retailer connect — all in one place. No backend required.

---

## 🚀 Features

| Feature | Description |
|---|---|
| 📊 **Mandi Prices** | Live wholesale market prices from mandis across India with price history charts |
| 🛒 **Agri Shop** | Buy seeds, pesticides, fertilizers, and equipment with cart & checkout |
| 🌱 **Crop Advisory** | AI-powered pest alerts, weather advisory, and personalized recommendations |
| 🩺 **Crop Doctor** | Upload a crop photo for AI disease diagnosis and treatment suggestions |
| 🏛️ **Govt Schemes** | Browse PM-KISAN, PMFBY, KCC and 5+ other schemes with apply links |
| 🏪 **Nearby Retailers** | Find agri retailers with call, WhatsApp, and directions buttons |
| 📰 **Agri News** | Latest agriculture news filtered by Market, Weather, Government, Alert |
| ▶ **Farm Videos** | Educational farming videos from Bayer, IFFCO, IMD and others |
| 📱 **Phone Connect** | Register mobile for SMS alerts on prices, weather & pest outbreaks |
| 🏆 **Bayer Coins** | Earn coins for every action — add crops, verify products, place orders |
| 🔍 **Product Verify** | Verify Bayer product authenticity via QR code or 16-digit code |
| 🔔 **Notifications** | In-app notification panel with real-time mandi and weather alerts |

---

## 📁 File Structure

```
FarmRise/
└── index.html    # Complete single-file application
```

> The entire platform is a **single self-contained HTML file** — no build tools, no frameworks, no backend.

---

## 🖥️ Pages & Navigation

| Page | Sidebar / Nav | Description |
|------|--------------|-------------|
| 🏠 Home | Home | Hero banner, quick actions, live market prices, flash sale, price trend chart, latest news |
| ₹ Mandi | Mandi Prices | Crop filter, variety tabs, sort by distance/price/trend, price history charts |
| 🛒 Shop | Shop | Category banners, flash sale countdown, product grid, cart sidebar |
| 🌱 Advisory | Advisory | My crops list, pest alerts, AI recommendations, Crop Doctor |
| ▶ Videos | Videos | Filterable video grid by topic |
| 🏛️ Schemes | Govt Schemes | 8 government schemes with apply + SMS info buttons |
| 🏪 Retailers | Nearby Retailers | Retailer cards with call, WhatsApp, directions |
| 📰 News | Agri News | News grid filtered by category |
| 👤 Profile | Profile/More | Edit profile, settings, coins, language, logout |

Navigation is available via top navbar, left sidebar (desktop), and bottom mobile nav bar.

---

## 🛒 Shop & Cart

- Products across 4 categories: Seeds, Pesticides, Fertilizers, Equipment
- Wishlist toggle per product
- Cart sidebar with quantity controls and live total
- Free delivery above ₹499
- Checkout earns +50 Bayer Coins

---

## 📊 Mandi Price Data

Crops supported: Corn, Tomato, Onion, Wheat, Capsicum, Soybean, Cumin, Rice

Each mandi entry includes:
- Low price, High price (per 100 kg)
- Distance from user location
- Today's price trend (up/down + delta)
- 7-day price history chart

Filters available: crop type, variety, radius (100/300/500 km / All India), "Highest Price Only" toggle, sort by Distance / Price / Trend.

---

## 🏆 Bayer Coins System

| Action | Coins Earned |
|--------|-------------|
| Complete profile | +50 |
| Add crop to advisory | +30 |
| Use Crop Doctor | +20 |
| Verify Bayer product | +25 |
| Refer a friend | +50 |
| Place an order | +10 |
| Connect phone number | +50 |
| Read articles daily | +10/day |

---

## 💾 Data Storage

All user data is stored in `localStorage` — no server calls made.

| Key | Contents |
|-----|----------|
| `fr_profile` | User name, phone, state, district |
| `fr_myCrops` | List of user's crops with sowing dates |
| `fr_cart` | Shopping cart items |
| `fr_wishlist` | Wishlisted product IDs |
| `fr_coins` | Bayer Coins balance |
| `fr_followed` | Followed mandi names |
| `fr_notifs` | Notification history |

---

## 🎨 Design System

- **Fonts:** Plus Jakarta Sans (body) + Syne (headings) via Google Fonts
- **Icons:** Font Awesome 6.5
- **Charts:** Chart.js 4.4.1 (price trend + mandi bar charts)
- **Primary colour:** `#1c8a3c` green with `#1de9b6` teal gradient
- **Background:** `#f3faf5` light green tint
- **Theme:** Light only, with green-dominant UI and glassmorphism navbar

---

## 📱 Responsive Design

| Breakpoint | Layout |
|------------|--------|
| > 1100px | Sidebar (240px) + main content |
| 640–900px | Sidebar hidden, top nav only |
| < 900px | Mobile bottom navigation bar shown |
| < 640px | Single-column product grid, stacked banners |

---

## ⚡ Real-Time Features

- **Flash sale countdown timer** — live timer on Home and Shop pages
- **Price simulation** — mandi prices randomly update every 12 seconds
- **Notification bar** — appears at top with live price alerts
- **Online/Offline detection** — shows connectivity toast messages
- **PWA-ready** — registers service worker on load

---

## 🌐 Browser Compatibility

Works in all modern browsers. Recommended: **Chrome** or **Edge** for best performance.

GPS auto-detect (Location modal) requires user to grant permission when prompted.

---

## 📄 License

This project is for personal/educational use. Built with HTML, CSS, and vanilla JavaScript — no frameworks or backend required.
