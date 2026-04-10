# The Excel Foundation — Website Files
## File Structure

```
excel-foundation/
├── index.html        ← Main landing page
├── events.html       ← Events & fundraising page
└── README.md         ← This file
```

## How to use

1. **Open locally** — Just double-click `index.html` in your browser to preview.
2. **Deploy** — Upload both files to any web host (Netlify, cPanel, GitHub Pages, etc.)
3. Events page links from the nav on `index.html` → `events.html`

## Customisation guide

### 🎨 Brand colours (change in the `<style>` block of each file)
- Primary dark: `#1a1a2e`  (navy)
- Gold accent:  `#F59E0B`  (amber/gold)
- Teal:         `#1D9E75`
- Blue:         `#185FA5`
- Brown/amber:  `#854F0B`

### 🖼️ Adding real photos
Replace the SVG placeholder blocks with real `<img>` tags:
```html
<!-- BEFORE -->
<div class="img-placeholder c1" style="min-height:260px;">
  <svg ...>...</svg>
  <div class="img-caption">Children's Education Program</div>
</div>

<!-- AFTER -->
<img src="images/kids-education.jpg"
     alt="Children in classroom"
     style="width:100%; height:260px; object-fit:cover; border-radius:12px;" />
```
Create an `images/` folder and drop your photos in there.

### 📝 Update your content
- Foundation name, tagline → search for "The Excel Foundation"
- Stats (12K+, 19, ₦2.4B, 94%) → update in the `.stats-bar` section
- Story cards → update names, quotes, locations in `.story-card`
- Events → update dates, venues, prices in `.ev-card` blocks
- Countdown target date → in `events.html` JS: `new Date('2026-07-19T18:00:00')`

### 💳 Connect a payment provider (for donations & tickets)
Replace the `onclick="alert(...)"` buttons with your payment link:
```html
<!-- Paystack example -->
<button onclick="window.location.href='https://paystack.com/pay/your-link'">
  Donate ₦25,000 securely →
</button>

<!-- Or embed Paystack inline popup -->
<script src="https://js.paystack.co/v1/inline.js"></script>
```

### 📧 Connect a newsletter provider
Replace the `subscribeNewsletter()` function with your Mailchimp / Brevo / ConvertKit form action.

### 🌐 Hosting options (free to low cost)
| Option | Cost | Best for |
|---|---|---|
| Netlify | Free | Quick deploy, drag & drop |
| GitHub Pages | Free | Developers |
| cPanel hosting | ~$5/mo | Full control |
| Vercel | Free | Fast global CDN |

## Next pages to build
- `donate.html` — Full donation checkout flow
- `blog.html`   — News & field reports
- `map.html`    — Interactive impact map
- `about.html`  — Team & mission

---
Built for The Excel Foundation · 2026
