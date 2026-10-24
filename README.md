# ARMA Detailing Studio: demo site

Static single page: HTML, CSS, vanilla JS. GSAP 3.12.5 + ScrollTrigger (cdnjs) and Lenis 1.1.13 (jsDelivr), versions pinned.

```
arma-site/
  index.html
  css/style.css     (rebrand: edit the :root variables at the top)
  js/main.js        (WhatsApp number, reviews, partner tiles)
  assets/
```

## Assets

Already in `/assets` (renamed from your uploads):

| File | Used for |
|---|---|
| hero-1.mp4, hero-2.mp4 | Hero slides 1 and 2 |
| studio-hall.png, defender.png, storefront.png | Hero posters, services, gallery |
| m4.jpg, rs5-wash.jpg, bmw-detail.jpg, rs7.jpg | Services and gallery (already resized to 1800px) |
| car-top.png | Signature scroll section |
| logo.png | Brand reference (the header uses a text wordmark) |

Still needed:

| File | Spec |
|---|---|
| hero-3.mp4 | 1920x1080, H.264, muted, under 6 MB. Until it exists, slide 3 shows the storefront poster |
| partners/*.svg | 3 logos, square, ideally white or single colour |
| favicon.png | 64x64 |
| og.jpg | 1200x630 share image |

Performance notes: `hero-1.mp4` is 23 MB. Compress it before deploying (for example `ffmpeg -i hero-1.mp4 -vf scale=1920:-2 -crf 28 -an -movflags +faststart hero-1.mp4`). Convert the large PNGs (`studio-hall`, `storefront`, `defender`) to WebP or JPG.

## Fill in (search for `TODO`)

Phone, email, intro copy, stats, FAQ answers, partner logos, map address.

## Run locally

```
npx serve .
```

## Deploy free

**Netlify:** go to app.netlify.com/drop and drag the `arma-site` folder in.

**Vercel:** `npm i -g vercel`, then run `vercel` inside the folder (accept the defaults, no build command, output directory `.`). Or push to GitHub and import the repo at vercel.com/new.
