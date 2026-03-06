# 🛒 Spesti — Smart Grocery Comparison · Bulgaria

Compare prices across **Kaufland, Lidl, Billa & Fantastico** in Bulgaria.  
Build your weekly list, see where each item is cheapest, and track your savings.

**Live demo:** `https://YOUR-USERNAME.github.io/spesti`

---

## 🚀 Deploy to GitHub Pages (5 minutes)

### Option A — GitHub Web UI (no git required)

1. Go to [github.com](https://github.com) and sign in
2. Click **New repository** → name it `spesti` → set to **Public** → click **Create repository**
3. On the next page, click **uploading an existing file**
4. Drag and drop `index.html` → click **Commit changes**
5. Go to **Settings → Pages**
6. Under **Source**, select **Deploy from a branch**
7. Branch: **main** | Folder: **/ (root)** → click **Save**
8. Wait ~60 seconds → your site is live at `https://YOUR-USERNAME.github.io/spesti`

---

### Option B — Git command line

```bash
git init
git add index.html README.md
git commit -m "Launch Spesti"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/spesti.git
git push -u origin main
```

Then enable Pages in **Settings → Pages → Deploy from main branch**.

---

## 📁 File Structure

```
spesti/
└── index.html     ← The entire app (single file, no build step)
└── README.md      ← This file
```

That's it. No npm, no build tools, no dependencies to install.  
Everything is bundled via CDN links inside `index.html`.

---

## ✨ Features

- **48 real Bulgarian grocery products** across 11 categories
- **4 stores compared:** Kaufland · Lidl · Billa · Fantastico
- **Weekly List** — check off items, set quantities, see live savings total
- **Find Item** — search any product, tap to see 4-store price comparison bar chart
- **By Store** — see exactly which items to buy at each store this week
- **Savings Report** — weekly savings, annual projection, store-by-store breakdown
- **Preference Profile** — personalize by brand, fat %, and size preferences
- **Price Watchlist** — flag items you want to monitor
- **🔥 Sale Spotlight** — see all this week's sale items at a glance
- **EN / БГ** bilingual (English / Bulgarian)
- **Mobile responsive**

---

## 🛠 Tech Stack

- React 18 (via CDN)
- Babel Standalone (JSX compilation in browser)
- Google Fonts (Playfair Display + Source Sans 3)
- Zero build step — works directly from `index.html`

---

## 📝 Customizing Data

All product data lives inside `index.html` in the `PRODUCTS` array.  
Each product follows this pattern:

```js
P("unique-id", "Category", "English Name", "Bulgarian Name",
  "Brand", "Size", IMG.category,
  { kaufland: 1.99, lidl: 1.89, billa: 2.09, fantastico: 2.04 },
  { lidl: true },   // sale flags (optional)
  3.7               // fat % (optional, dairy only)
)
```

To add a store: add it to the `STORES` array and create a matching SVG logo component.

---

Made with ❤️ for smart Bulgarian shoppers.
