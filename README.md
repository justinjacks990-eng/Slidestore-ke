# SlideStoreKE — Premium E-Commerce Website

> **"Quiet luxury starts from the ground up"**
> Nairobi's premier custom footwear brand — Slides · Clogs · Sandals

---

## 📁 File Structure

```
slidestoreke/
├── index.html          ← Complete single-page e-commerce site
├── images/             ← All product & profile images (local, no CDN)
│   ├── birkenstock-black-clogs.jpg
│   ├── birkenstock-boston-box.jpg
│   ├── birkenstock-embroidered.jpg
│   ├── birkenstock-multicolor.jpg
│   ├── birkenstock-pink-suede.jpg
│   ├── chrome-hearts-black.jpg
│   ├── chrome-hearts-brown.jpg
│   ├── chrome-hearts-tan.jpg
│   ├── custom-clogs-brown-flames.jpg
│   ├── custom-clogs-flames.jpg
│   ├── custom-flames-chrome.jpg
│   ├── instagram-profile.jpg
│   ├── nike-calm-mule.jpg
│   ├── nike-ispa-slides.jpg
│   ├── product1.jpg – product8.jpg
│   └── profile.jpg
└── README.md           ← This file
```

---

## 🌐 External Dependencies (CDN — requires internet)

The site loads two resources from CDN at runtime:

| Resource | URL |
|---|---|
| Tailwind CSS | `https://cdn.tailwindcss.com` |
| Google Fonts | `https://fonts.googleapis.com` (Playfair Display, Inter, Space Grotesk) |

> **Offline use:** If you need the site to work without internet, download Tailwind CSS locally and self-host the fonts. See the "Offline / Self-Hosted" section below.

---

## 🚀 Deployment

### Option 1 — GitHub Pages (Free)

1. Create a new GitHub repository (e.g. `slidestoreke-website`)
2. Upload all files maintaining the folder structure:
   ```
   index.html
   images/
   README.md
   ```
3. Go to **Settings → Pages**
4. Under **Source**, select `main` branch → `/ (root)` → **Save**
5. Your site will be live at:
   `https://<your-username>.github.io/slidestoreke-website/`

**Using Git CLI:**
```bash
git init
git add .
git commit -m "Initial SlideStoreKE website"
git branch -M main
git remote add origin https://github.com/<your-username>/slidestoreke-website.git
git push -u origin main
```
Then enable GitHub Pages in repository Settings.

---

### Option 2 — Netlify (Free, Recommended)

**Drag & Drop (easiest):**
1. Go to [netlify.com](https://netlify.com) and sign up / log in
2. From the dashboard, drag the entire `slidestoreke/` folder onto the deploy area
3. Your site is live instantly with a Netlify URL (e.g. `https://slidestoreke.netlify.app`)
4. Optionally connect a custom domain in **Site Settings → Domain Management**

**Via Netlify CLI:**
```bash
npm install -g netlify-cli
netlify login
netlify deploy --prod --dir .
```

---

### Option 3 — Vercel (Free)

```bash
npm install -g vercel
vercel login
vercel --prod
```

---

### Option 4 — Local Development

Simply open `index.html` in any modern browser. No build step, no server required.

> **Note:** Some browsers block local file access for images. If images don't load locally, use a simple server:
> ```bash
> # Python 3
> python3 -m http.server 8000
> # Then open: http://localhost:8000
> ```

---

## ⚙️ Customisation

### Update WhatsApp Number
In `index.html`, find this line near the top of the `<script>` section:
```javascript
const WHATSAPP_NUMBER = '254702080950';
```
Change to your number in international format (no `+`, no spaces).

### Add / Edit Products
Find the `products` array in the `<script>` section:
```javascript
const products = [
  {
    id: 1,
    name: 'Chrome Hearts Custom Clogs',
    brand: 'Custom',
    price: 8500,
    image: 'images/chrome-hearts-black.jpg',
    category: 'clogs',
    badge: 'HOT',
    rating: 4.9,
    sizes: [36, 37, 38, 39, 40, 41, 42, 43, 44],
    colors: ['Black', 'White', 'Brown'],
    description: '...'
  },
  // Add more products here
];
```

### Update Store Info
Search for these values in `index.html` and replace as needed:
- **Address:** `Odeon, Latema Road, Lois Plaza, Shop A9`
- **Phone:** `0702 080 950`
- **Instagram:** `@_slidestoreke_`
- **Hours:** `Mon–Sat: 9:00 AM – 7:00 PM`

---

## 🛒 Features

| Feature | Status |
|---|---|
| Product grid with filters & sorting | ✅ |
| Product detail modal (bottom-sheet) | ✅ |
| Size & color selection with validation | ✅ |
| Add to cart / remove / quantity control | ✅ |
| Cart drawer with item list | ✅ |
| WhatsApp checkout (formatted order message) | ✅ |
| Wishlist with localStorage persistence | ✅ |
| Real-time search overlay | ✅ |
| Category filter pills | ✅ |
| Fixed bottom navigation | ✅ |
| Toast notifications | ✅ |
| Floating WhatsApp button | ✅ |
| Instagram feed section | ✅ |
| Trust badges section | ✅ |
| Fully responsive (375px – 1440px) | ✅ |
| Dark mode premium aesthetic | ✅ |

---

## 📞 Brand Contact

- **WhatsApp:** [0702 080 950](https://wa.me/254702080950)
- **Instagram:** [@_slidestoreke_](https://instagram.com/_slidestoreke_)
- **Location:** Odeon, Latema Road, Lois Plaza, Shop A9, Nairobi

---

## 📄 Offline / Self-Hosted Fonts & CSS

To make the site work 100% offline:

1. Download Tailwind CSS: https://tailwindcss.com/docs/installation
2. Download fonts from Google Fonts and place in a `fonts/` folder
3. Replace the CDN `<link>` and `<script>` tags in `index.html` with local paths

---

*Built with ❤️ for SlideStoreKE — Nairobi's Quiet Luxury Footwear Brand*
*© 2026 SlideStoreKE. All rights reserved.*
