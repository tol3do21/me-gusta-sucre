# Me Gusta Sucre — Project Review

> Read and update this file at the start and end of every session.

---

## Links

| Resource | URL |
|---|---|
| Live site | https://tol3do21.github.io/me-gusta-sucre/ |
| GitHub repo | https://github.com/tol3do21/me-gusta-sucre |
| GitHub account | tol3do21 |

---

## Project Overview

**Me Gusta Sucre** is a tourist information website for the city of Sucre, Bolivia ("La Ciudad Blanca"). Single-page HTML site using Tailwind CSS via CDN.

- **Location:** `D:/proyectos/me-gusta-sucre/`
- **Main file:** `index.html`
- **Images:** `Imagenes/sucre-bolivia.webp` (note capital I — case-sensitive on GitHub Pages)
- **Fonts:** Playfair Display, Cormorant SC, Inter (Google Fonts)
- **Color palette:** Navy `#1e3a5f`, Royal Blue `#2563eb`, Crimson `#dc2626`, Cream `#f8f5f0`

---

## Sections Built

1. **Navbar** — sticky, turns solid navy on scroll, mobile hamburger menu, Bolivia flag stripe
2. **Hero** — local image `Imagenes/sucre-bolivia.webp`, cinematic filter (grayscale + crimson tint + letterbox bars)
3. **About** — split layout, UNESCO badge card, stats (300K pop / 22°C / 1538 founded)
4. **Attractions** — 6 cards: Casa de la Libertad, Catedral Metropolitana, Parque Cretácico, Recoleta Mirador, Tarabuco Market, ASUR Textile Museum
5. **Activities** — paragliding, hiking, Spanish schools, coffee tasting + Cholita Wrestling card
6. **Food & Drink** — bento grid: chocolate, salteñas, api & singani + 4 food tiles
7. **Plan Your Visit** — 3 info cards (getting there, best time, practical tips) + CTA banner
8. **Footer** — links, quick facts, Bolivia flag stripe

---

## Hero Animations

- Ken Burns effect on background image
- Letter-by-letter title reveal (`letterDrop` keyframe, 3D flip + blur)
- Floating particles (28 dots, white & crimson, drifting upward via JS)
- Scan line sweep across hero every 9s
- Scroll parallax on background wrapper (0.32× scroll speed)
- Glow pulse on the red/blue divider rule
- Stat counter animation (numbers count up: 2,810m / 5,000+ / 1809)
- CTA shimmer sweep on "Explore the City" button
- Badge slide-in from right with staggered delays
- Eyebrow line draw animation

---

## Cinematic Hero Filter

Applied to `Imagenes/sucre-bolivia.webp`:
- `filter: grayscale(100%) contrast(1.15) brightness(0.78)` on the `<img>`
- Crimson-to-navy gradient overlay on top
- Heavy bottom fog + top vignette
- Thin black letterbox bars (top & bottom, `h-5`)

---

## Deployment

- **Platform:** GitHub Pages (free)
- **Branch:** `main`, root `/`
- **GitHub CLI:** installed at `C:/Program Files/GitHub CLI/gh.exe`
- **Git identity set locally:** `tol3do21@users.noreply.github.com`

To push updates:
```bash
cd D:/proyectos/me-gusta-sucre
git add .
git commit -m "your message"
git push
```

---

## Standing Instructions for Claude

- **Auto-push to GitHub after every change.** Whenever any file in this project is modified, immediately run `git add . && git commit -m "<description>" && git push` without waiting to be asked. Do not batch changes — push after each task is complete.

---

## Outstanding Issues / TODO

- [ ] All attraction card images are Unsplash stock — replace with real Sucre photos if available (local files not yet obtained)
- [ ] WhatsApp number in footer and CTA is a placeholder (`59172000000`) — update to real number before launch

---

## Session Log

### Session 1 — 2026-04-05
- Built full single-page tourist site from scratch using frontend-design skill
- Color palette: blue, red, white as requested
- Set local hero image (`Imagenes/sucre-bolivia.webp`)
- Added advanced hero animations (particles, parallax, letter split, counters, scan line)
- Applied cinematic filter to hero (grayscale + crimson tint + letterbox)
- Installed GitHub CLI via winget, authenticated as `tol3do21`
- Created GitHub repo, pushed code, enabled GitHub Pages
- Fixed case-sensitivity bug: `imagenes/` → `Imagenes/` (Linux FS is case-sensitive)
- Site live at https://tol3do21.github.io/me-gusta-sucre/

### Session 2 — 2026-04-05
- Fixed all 7 outstanding TODO items in one commit (ae41448)
- Added SVG favicon (crimson "M" circle, inline data URL)
- Added meta description, Open Graph, and Twitter Card tags (OG image points to hero WebP)
- Fixed mobile hero title overflow: added `xs` (360px) breakpoint, base font now 3rem scaling to 9rem on desktop
- Replaced Tarabuco Market card image (was duplicate of Salteñas Unsplash photo)
- Wired "Plan My Trip" CTA banner button to WhatsApp with pre-filled message (placeholder number `59172000000`)
- Replaced dead footer social icons (Facebook/Instagram/Twitter) with a single WhatsApp contact button
- Remaining: replace placeholder WhatsApp number with real one before launch; swap Unsplash images for real Sucre photos when available
