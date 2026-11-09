# ARCA / HAUS — Contemporary Architecture & Residences

A cinematic, scroll-driven website for a contemporary residential architecture studio. It shows off a featured villa and a city apartment through layered motion, full-screen photography and smooth editorial transitions.

> **Portfolio project.** ARCA / HAUS, Villa Solenne and all business details on this site are fictional. They were created to demonstrate design and front-end development work. Any resemblance to a real company is coincidental.

**Designed & developed by [Creatovix](https://creatovix.com)**

---

## Overview

| | |
|---|---|
| **Type** | Marketing / showcase website (single page) |
| **Industry** | Architecture, residential design, real estate |
| **Focus** | Storytelling through scroll, motion and photography |
| **Output** | Static export, so it can be hosted anywhere |
| **Devices** | Desktop, laptop, tablet, mobile (portrait & landscape) |

## Highlights

- **Branded loading sequence.** The wordmark is revealed letter by letter, with a live percentage counter and progress line. It exits with a two-layer curtain reveal.
- **Editorial hero.** A full-screen image with a slow zoom, a masked line-by-line headline reveal, a supporting intro and an animated scroll cue.
- **About section with a floating gallery.** Image tiles drift in on scroll. A centre image expands into an auto-playing slideshow and then settles inline within the statement text.
- **Marquee transition.** A large wordmark marquee hands off into the featured residence.
- **Structure walkthrough.** A pinned, seven-step scroll sequence (Full View, Walls, Floor, Roof, Facade, Stairs, Windows & Doors) with cross-fading photography, a progress rail, clickable steps and a live counter.
- **Residence slides.** Split-screen story panels that pair large serif headlines with imagery.
- **Apartment showcase.** A pinned slider for the living room, main bedroom and guest room, with a synced counter.
- **Expanding feature card.** The "Step inside" card grows to full screen on scroll, with a call to book a viewing.
- **Contact panel.** A full-screen overlay with copy-to-clipboard email, enquiry shortcuts and social links.
- **Smooth scrolling** throughout, plus character and line text reveals on headings.
- **Accessible details.** Semantic sections, descriptive alt text, ARIA labels on controls, and support for `prefers-reduced-motion`.

## Tech Stack

| Layer | Technology |
|---|---|
| Framework | Next.js (App Router), React |
| Styling | Tailwind CSS plus a small custom stylesheet |
| Animation | GSAP, ScrollTrigger, SplitText-style text reveals |
| Smooth scroll | Lenis |
| Fonts | Self-hosted web fonts (`woff2`) |
| Images | Optimised WebP photography |
| Build | Static export (Turbopack) |

## Project Structure

```
site/
├── index.html                 # Pre-rendered page
├── favicon.ico                # A/H monogram
├── images/
│   └── arca-haus-social.jpg   # Social share (Open Graph) image
├── assets/
│   └── images/                # Hero, gallery, structure and interior photography (.webp)
└── _next/
    └── static/
        ├── chunks/            # Compiled JavaScript and CSS
        └── media/             # Web fonts
```

## Running Locally

The site is a static build. It must be served from the **root of a web server**, because asset paths start with `/`. Opening `index.html` directly from disk will not work.

```bash
# Option 1: Node
npx serve site

# Option 2: Python
cd site
python3 -m http.server 8080
```

Then open `http://localhost:8080` (or the address shown in the terminal).

## Deployment

Upload the contents of the `site/` folder to any static host, for example:

- **Netlify / Vercel / Cloudflare Pages.** Drag and drop the folder, or point the output directory to `site`.
- **Traditional hosting (cPanel, etc.).** Upload the folder contents into `public_html` or the domain root.

No server-side code, database or environment variables are needed.

## Performance Notes

- All photography is delivered as compressed WebP at fixed dimensions.
- The loader preloads only what the first screen needs (fonts, hero and transition imagery).
- Heavy 3D assets were removed and replaced with photography, which cut the build size roughly in half.
- Animations run on transforms and opacity for smooth, GPU-friendly motion.

## Browser Support

Latest versions of Chrome, Edge, Firefox and Safari on desktop, plus Safari (iOS) and Chrome (Android) on mobile.

## Credits

- **Design & development:** Taiba Creations
- **Photography:** [Unsplash](https://unsplash.com), used under the [Unsplash License](https://unsplash.com/license)

| File | Source |
|---|---|
| `hero3.webp` | https://images.unsplash.com/photo-1613977257363-707ba9348227 |
| `hero5.webp` | https://images.unsplash.com/photo-1580587771525-78b9dba3b914 |
| `top.webp` | https://images.unsplash.com/photo-1599809275671-b5942cabc7a2 |
| `side.webp` | https://images.unsplash.com/photo-1613490493576-7fde63acd811 |
| `nightSide.webp` | https://images.unsplash.com/photo-1600585154363-67eb9e2e2099 |
| `landscape-house-clean.webp` | https://images.unsplash.com/photo-1600607688969-a5bfcd646154 |
| `exterior-garden-clean.webp` | https://images.unsplash.com/photo-1613553507747-5f8d62ad5904 |
| `patio-front-clean.webp` | https://images.unsplash.com/photo-1512917774080-9991f1c4c750 |
| `living-room-clean.webp` | https://images.unsplash.com/photo-1600607687939-ce8a6c25118c |
| `kitchen-clean.webp` | https://images.unsplash.com/photo-1604014237800-1c9102c219da |
| `apartment-tour.webp` | https://images.unsplash.com/photo-1600566753376-12c8ab7fb75b |
| `apartment-living.webp` | https://images.unsplash.com/photo-1618221195710-dd6b41faaea6 |
| `apartment-bedroom.webp` | https://images.unsplash.com/photo-1600573472591-ee6b68d14c68 |
| `apartment-bedroom-2.webp` | https://images.unsplash.com/photo-1615874959474-d609969a20ed |
| `structure-01.webp` | https://images.unsplash.com/photo-1600596542815-ffad4c1539a9 |
| `structure-02.webp` | https://images.unsplash.com/photo-1600047509807-ba8f99d2cdde |
| `structure-03.webp` | https://images.unsplash.com/photo-1613545325278-f24b0cae1224 |
| `structure-04.webp` | https://images.unsplash.com/photo-1602343168117-bb8ffe3e2e9f |
| `structure-05.webp` | https://images.unsplash.com/photo-1600585154526-990dced4db0d |
| `structure-06.webp` | https://images.unsplash.com/photo-1600047508788-786f3865b4b9 |
| `structure-07.webp` | https://images.unsplash.com/photo-1600573472550-8090b5e0745e |

---

© 2026 Taiba Creations. ARCA / HAUS is a fictional brand created for portfolio purposes.