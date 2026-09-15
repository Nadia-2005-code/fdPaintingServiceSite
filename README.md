# F&B Painting & Decorating Services

A lightning-fast, zero-JS static website built for F&B Painting & Decorating. 

This site is built with [Astro](https://astro.build/) and deployed on Cloudflare Pages. It is heavily optimized for local SEO, mobile performance, and accessibility, achieving a 100/100 Lighthouse score across all metrics.

## 🛠️ How to Update the Site

This project was built to be extremely easy to maintain without touching the core layout code.

### 1. Updating Contact Info & Socials
All global business data is centralized in one file. If Faisal changes his phone number, email, or social links, you only need to update it here:
👉 **`src/data/siteInfo.ts`**

Updating this file will automatically update the Header, Footer, WhatsApp buttons, and SEO meta tags across the entire site.

### 2. Adding to the Gallery
The Portfolio/Gallery page is fully automated. You do **not** need to write any HTML to add new photos.

1. Drop a high-quality image (`.jpg`, `.png`, or `.webp`) into **`src/assets/gallery/`**.
2. **Name the file what you want the caption to be.** Use dashes or underscores for spaces.
   * *Example:* Naming a file `Exterior-timber-sash-window-restoration.jpg` will automatically generate a gallery card with the caption **"Exterior timber sash window restoration"** and apply the correct SEO `alt` text.
3. Astro will automatically resize, compress, and convert the image to WebP during the next build.

## Tech Stack & Performance Notes

* **Framework:** Astro (Static Site Generation)
* **Styling:** Vanilla CSS (Scoped to components)
* **JavaScript:** Zero client-side JS shipped to the browser (except for a tiny inline script for the mobile menu).
* **Hosting:** Cloudflare Pages
* **Assets:** `astro:assets` handles all image optimization and responsive sizing at build time.

## Commands

All commands are run from the root of the project, from a terminal:

| Command                   | Action                                           |
| :------------------------ | :----------------------------------------------- |
| `npm install`             | Installs dependencies                            |
| `npm run dev`             | Starts local dev server at `localhost:4321`      |
| `npm run build`           | Build your production site to `./dist/`          |
| `npm run preview`         | Preview your build locally, before deploying     |
