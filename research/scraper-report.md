# Dell Homepage Scraper Report

## Brand Colors
- Primary blue: `#0076CE` (rgb(0, 118, 206)) — confirmed via `.voc__feedbackicon`
- CTA/link blue: `#0063B8` (rgb(0, 99, 184)) — confirmed via `.skip-nav-link`
- Dark navy: `#0d2155` (carried from v1, not overridden)
- Mid blue derived: `color-mix(in srgb, #0076CE 60%, #000000)`

## CSS Variables
```css
:root {
  --brand-color: #0076CE;
  --brand-dark: #0d2155;
  --brand-mid: color-mix(in srgb, #0076CE 60%, #000000);
  --brand-light: color-mix(in srgb, #0076CE 12%, #ffffff);
}
```

## Live Hero Images (verified 200 OK from i.dell.com CDN)

### 2560×900 Hero Banners
1. Spring sale — Latitude 14 Plus + SE2726H monitor:
   `https://i.dell.com/is/image/DellContent/content/dam/ss2/page-specific/dell-homepage/en/shutterstock-2352697593-na-spring-sale-db14250nt-se2726h-2560x900.jpg?fmt=pjpg&pscan=auto&scl=1&hei=900&wid=2560&resMode=sharp2&size=2560,900&op_usm=1.75,0.3,2,0`

2. Copilot/AI PC hero — Latitude 14 Plus:
   `https://i.dell.com/is/image/DellContent/content/dam/ss2/page-specific/dell-homepage/na/heroes/us-ca-bigbets-homepage-desktop-site-banner-2560x900-db14250t-copilot.jpg?fmt=pjpg&pscan=auto&scl=1&hei=900&wid=2560&resMode=sharp2&size=2560,900&op_usm=1.75,0.3,2,0`

3. XPS 13 hero — "Roma in sky":
   `https://i.dell.com/is/image/DellContent/content/dam/documents-and-videos/dv2/pan-dell/en/product-launch/laptops-and-2n1s/dell-xps-laptops/dx13260-laptop/site-banners/2601g0169-dell-xps-13-dx13260-roma-in-sky-site-banners-2560x900-clean.jpg?fmt=pjpg&pscan=auto&scl=1&hei=900&wid=2560&resMode=sharp2&size=2560,900&op_usm=1.75,0.3,2,0`

### 1610×906 Product Banners
4. Dell Pro 5 Precision laptops (PW514260/PW516260):
   `https://i.dell.com/is/image/DellContent/content/dam/documents-and-videos/dv2/pan-dell/en/product-launch/laptops-and-2n1s/dell-pro-laptops/dell-pro-5-precision-pw514260-pw516260-pw514265-pw516265/site-banners/2601g0167-gl-bb-site-dell-pro-5-precision-laptops-pw514260-pw516260-1610x906-intel-clean.jpg?wid=1610&hei=906`

5. Dell S 14260/16260 laptops:
   `https://i.dell.com/is/image/DellContent/content/dam/documents-and-videos/dv2/pan-dell/en/product-launch/laptops-and-2n1s/dell-s-laptops/ds14260-ds16260-laptops/site-banners/family/2601g0157-gl-pd-site-dell-ds14260-ds16260-1610x906.jpg?wid=1610&hei=906`

6. Dell Pro 7 laptop (P703260/P704260):
   `https://i.dell.com/is/image/DellContent/content/dam/documents-and-videos/dv2/pan-dell/en/product-launch/laptops-and-2n1s/dell-pro-laptops/dell-pro-7-p703260-p703265-p704260-p704265/site-banners/2601g0170-gl-bb-site-dell-pro-7-laptop-p703260-p704260-family-shot-1610x906-intel.jpg?wid=1610&hei=906`

7. Alienware Area-51 desktop (AAT2250):
   `https://i.dell.com/is/image/DellContent/content/dam/documents-and-videos/dv2/csbg/en/product-launch/alienware/alienware-area51-aat2250-gaming-desktop-citadel/site-banners/cs2503g0009-gl-cs-co-fy25q2-sit-awarea51-aat2250-1610x906-360.jpg?wid=1610&hei=906`

8. Dell Pro laptop promo (Latitude 9450t + PowerEdge R760):
   `https://i.dell.com/is/image/DellContent/content/dam/ss2/page-specific/dell-homepage/ssl-bfcm-cons-dell-ls-latitude-9450t-poweredge-r760-uhp-2604-01-br-promo-c-lf-1610x906.jpg?wid=1610&hei=906`

9. Dell PC 14250 workstation setup:
   `https://i.dell.com/is/image/DellContent/content/dam/ss2/page-specific/dell-homepage/na/promo-carousel/wtn-showc-cons-dell-pc14250-e2725hm-km555-wd25-wl3024-wb3023-uhp-2604-01-us-promo-c-lf-1610x906.jpg?wid=1610&hei=906`

10. Dell Pro PC14250 product shot:
    `https://i.dell.com/is/image/DellContent/content/dam/ss2/page-specific/dell-homepage/prod-8062853-getty-2198589663-dell-pro-pc14250nt-wl3024-1610x906.jpg?wid=1610&hei=906`

11. B2L enterprise story (Wellcome Sanger Institute):
    `https://i.dell.com/is/image/DellContent/content/dam/ss2/product-images/page/uber/b2l-wellcome-sanger-institute-2880x1620.jpg?fmt=png&op_usm=1.75,0.3,2,0&resMode=sharp2&size=1024,576&wid=1024&hei=576`

## Key Messaging (homepage)
- "Dell 14 Plus — Save Up to $520"
- "New XPS 13 — Razor-thin. Featherlight. Starting at $699."
- "Days of Deals — Smartest Time to Buy"
- Current hero tagline: AI PC / Copilot+ PC positioning

## Product Lines Confirmed
- **Laptops:** XPS 13 (DX13260), Dell 14 Plus, Dell Pro 5 Precision, Dell Pro 7, Dell S 14260/16260, Latitude
- **Desktops:** OptiPlex, Alienware Area-51 (AAT2250), Dell Pro Precision Fixed
- **Monitors:** UltraSharp, Dell Pro, Alienware
- **Accessories:** Docking stations, keyboards/mice, webcams, bags
- **Servers/Infra:** PowerEdge, Data Storage, Cyber Resilience

## Notes
- Dell WAF blocks sub-page scraping (known) — homepage only scraped
- No videos on homepage (empty video element list)
- i.dell.com CDN images load without cookies in browser — confirmed 200 OK
- Logo: `https://cdn.cookielaw.org/logos/6b4a2d40-4b8f-497a-94a8-1eff21895199/0197cb06-53f6-70a3-9c35-a7955861d4ed/827e05b3-aa62-470e-b407-df48f06af95d/delltech-logo-prm-blue-rgb.png`
