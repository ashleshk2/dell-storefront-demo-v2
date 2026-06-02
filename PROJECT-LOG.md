# Dell Technologies Amazon Brand Store — v2 Project Log

**Client:** Dell Technologies  
**Project:** Amazon Brand Store Demo (Version 2 Rebuild)  
**Purpose:** CloudCare pitch asset — demonstrates Amazon channel management services  
**Status:** Complete — 2026-06-03  

---

## Live URLs

| Environment | URL |
|---|---|
| Production | https://dell-storefront-demo-v2.vercel.app |
| GitHub | https://github.com/ashleshk2/dell-storefront-demo-v2 |
| Local | C:\Users\ashle\CloudCare\dell-storefront-demo-v2\ |

---

## Pages

| Page | File | Category |
|---|---|---|
| Homepage | index.html | Brand landing |
| Laptops | laptops.html | Dell Pro 7, Pro 5 Precision, S-series, XPS 13 |
| Monitors | monitors.html | UltraSharp U2725QE, U3225QE |
| Desktops | desktops.html | OptiPlex 7020 Micro, Pro Desktop |
| Accessories | accessories.html | WD25TB5 dock, KM555, WB3023, EcoLoop |
| Servers | servers.html | PowerEdge R760xs, R760, NVIDIA AI Factory |

---

## Build Summary

**Steps completed:**
1. Store research — strategy document, buyer profiling, competitor analysis
2. Chrome scraping — Dell homepage, brand colors, CDN image extraction
3. Image sourcing — 34 assets verified from i.dell.com and m.media-amazon.com CDN
4. Repo setup — GitHub + Vercel, copied v1 infrastructure as base
5. Hero banner — Style 3 (full-bleed photography), Latitude 14 Plus + SE2726H
6. Store build — all 6 pages built with brand CSS variables throughout
7. Design QA — 11 issues found and fixed, design score 9/10

**Design score:** 9/10 (up from 6.5/10 in v1)

---

## Key Technical Facts

- All images served from i.dell.com and m.media-amazon.com CDN — no local images required (v1 needed 8 local images due to Dell WAF cookie requirements on product pages; this was resolved by using only homepage-level CDN URLs that load without auth)
- Hero image: 2560×900 Latitude 14 Plus + SE2726H from Dell's Scene7 CDN, confirmed 200 OK
- Partials: header + footer via fetch() in main.js
- CSS variables: --brand-dark (#091840), --brand-dark-tint (#0d2155), --brand-blue (#0076CE), --brand-mid (#0c32a4), --brand-light (#E8F1FB)
- Hero style: Style 3 (full-bleed photography) — logged in hero-style-log.md
- No external links, no YouTube embeds (Amazon policy compliance)
- Scroll-reveal: IntersectionObserver with 800ms safety fallback for off-screen sections
- Mobile-responsive: 2-column grids, full-width hero, no horizontal overflow

---

## Brand Colors

| Variable | Hex | Use |
|---|---|---|
| --brand-blue | #0076CE | Primary CTA, accents |
| --brand-dark | #091840 | Darkest section backgrounds |
| --brand-dark-tint | #0d2155 | Dark navy backgrounds |
| --brand-mid | #0c32a4 | Gradient stops |
| --brand-light | #E8F1FB | Light tint backgrounds |

---

## QA Issues Fixed

1. Scroll-reveal stuck at opacity:0 — observer threshold + 800ms fallback
2. Horizontal scroll on CTA banner — contain: layout on ::before pseudo
3. Product cards unequal height — flex column + margin-top:auto on CTA
4. Duplicate category tile images on homepage — replaced with distinct scenes
5. Monitors card 3 duplicate image — replaced with E2725HM CDN image
6. Accessories backpack card wrong image — corrected to Dell CDN
7. Desktops card 3 wrong image — corrected to Dell CDN
8. Three 404 Amazon CDN URLs from guessed ASINs — replaced with confirmed Dell CDN
9. 18× hardcoded #0076CE in inline styles — replaced with var(--brand-blue)
10. Hardcoded #0d2a5e gradient stop — replaced with var(--brand-mid)
11. White-background product image halo on dark section — mix-blend-mode: luminosity

---

## Improvement Over v1

| Dimension | v1 | v2 |
|---|---|---|
| Design score | 6.5/10 | 9/10 |
| Images | 8 local files (CDN failed) | 34 verified CDN images |
| Pages | 6 (incl. Gaming) | 6 (incl. Servers — more relevant) |
| Image inventory | Limited to homepage scrape | Full product line coverage |
| CSS hygiene | Some hardcoded colors | 100% CSS variables |
| Scroll behavior | Reveal stuck on some sections | Fixed with fallback |
