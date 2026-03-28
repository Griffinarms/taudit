# Unorthodox Suppression — Design System
## Source: unorthodox-suppression.com (Squarespace, extracted March 28, 2026)
## Purpose: Reference document for WordPress/WooCommerce rebuild

---

## Typography

### Font Stack
All three fonts are available free via Google Fonts.

| Role | Font | Weight | Use |
|------|------|--------|-----|
| Display / Headlines | **Bebas Neue** | 400 (Regular) | Hero text, section headers, product names |
| Secondary Headlines | **Archivo Black** | 400 (Regular) | Subheadings, callouts, nav items |
| Body / UI | **Space Grotesk** | 600, 700 | Body copy, buttons, price text, descriptions |

### Google Fonts Import URL
```
https://fonts.googleapis.com/css2?family=Archivo+Black:ital,wght@0,400&family=Bebas+Neue:ital,wght@0,400&family=Space+Grotesk:ital,wght@0,600;0,700&display=swap
```

### WordPress Theme CSS
```css
@import url('https://fonts.googleapis.com/css2?family=Archivo+Black:ital,wght@0,400&family=Bebas+Neue:ital,wght@0,400&family=Space+Grotesk:ital,wght@0,600;0,700&display=swap');

body {
  font-family: 'Space Grotesk', sans-serif;
  font-weight: 600;
}

h1, h2, h3, .hero-text, .product-name {
  font-family: 'Bebas Neue', sans-serif;
  font-weight: 400;
  letter-spacing: 0.05em;
  text-transform: uppercase;
}

.nav, .button, .badge, .callout {
  font-family: 'Archivo Black', sans-serif;
  font-weight: 400;
  text-transform: uppercase;
  letter-spacing: 0.08em;
}
```

---

## Color Palette

### Primary Colors
| Name | Hex | Use |
|------|-----|-----|
| Background Black | `#111111` | Primary background, site base |
| Deep Black | `#0a0a0a` | Secondary sections, footer |
| Off-White | `#ffffff` | Primary text on dark backgrounds |
| Gold / Brass | `#7A673F` | Accent, CTAs, highlights, borders |

### Secondary / Functional Colors
| Name | Hex | Use |
|------|-----|-----|
| Dark Blue-Gray | `#112233` | Subtle section variation |
| Success Green | `#27ae60` | In-stock indicators, success states |
| Alert Red | `#c0392b` | Sold out, warnings, error states |
| Light Warm | `#ffaacc` | Rare accent (avoid overuse) |

### CSS Custom Properties (Paste into WordPress theme)
```css
:root {
  --color-bg:        #111111;
  --color-bg-deep:   #0a0a0a;
  --color-text:      #ffffff;
  --color-gold:      #7A673F;
  --color-gold-light:#a08a55;
  --color-success:   #27ae60;
  --color-danger:    #c0392b;
  --color-muted:     #888888;
}
```

---

## Visual Identity

### Core Motif
The **hexagon** is the brand's defining visual element. It appears:
- In the product shape (external hexagonal cross-section)
- As a recurring geometric pattern/overlay on images
- As a structural element in layouts (hexagonal grid, hex borders)

### Aesthetic Direction
- **Dark, minimal, premium** — think tactical, military-grade quality
- Heavy use of **negative space** — let the product breathe
- **High-contrast** white text on black backgrounds
- Gold accents used sparingly for maximum impact
- Photography: dark backgrounds, dramatic lighting, product-forward

### Logo Files (saved in `/assets/images/`)
- `HEADER-LOGO.png` — Primary logo (transparent background, white)
- `HEADER-LOGO2.png` — Secondary/alternate logo variant

### Logo Usage Rules
- Always on dark backgrounds
- Minimum clear space: 1x logo height on all sides
- Never place on light backgrounds without inverting

---

## Layout & Spacing

### Site Width
- Max content width: ~1400px
- Content column: ~1200px with padding
- Full-bleed sections: 100vw

### Grid
- Desktop: 12-column grid
- Product grid: 3 columns desktop, 2 tablet, 1 mobile
- Section padding: 80–120px vertical

### Navigation
- Fixed header, transparent over hero, solid black on scroll
- Links: Archivo Black, uppercase, spaced
- Structure: Logo (left) | Nav links (center/right) | Cart icon

---

## Page Structure

### Announcement Bar
- Single line, full-width, dark background
- Gold or white text
- Current message: "THE NEW 22 SUPPRESSOR - SPLIT IS LIVE!"
- Used for product launches, promotions, urgent notices

### Age Gate Modal
- Full-screen overlay on first visit
- Dark background with logo
- 21+ age verification required (NFA compliance)
- Cookie-based — shows once per session/browser
- Must be rebuilt in WordPress with Age Gate plugin

### Header / Navigation
```
[LOGO]                    [HOME] [SHOP] [ABOUT] [CONTACT]  [CART]
```
- Dark background (#111)
- Logo left-aligned
- Nav right-aligned (or centered)
- Cart icon with item count

### Footer
- Dark background
- Social links: Instagram, YouTube, Facebook
- Email: griffinarms@protonmail.com (to be updated to branded email)
- Phone: 724-376-2757
- Address: Stoneboro, PA 16153
- Privacy Policy link

---

## UI Components

### Buttons
```css
.btn-primary {
  background: var(--color-gold);
  color: #ffffff;
  font-family: 'Archivo Black', sans-serif;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  padding: 14px 32px;
  border: none;
  border-radius: 0; /* sharp corners — matches tactical aesthetic */
}

.btn-outline {
  background: transparent;
  color: #ffffff;
  border: 2px solid var(--color-gold);
  font-family: 'Archivo Black', sans-serif;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  padding: 12px 30px;
}

.btn-primary:hover {
  background: var(--color-gold-light);
}
```

### Product Cards
- Dark card background (#1a1a1a or transparent)
- Product image full-width top
- Product name in Bebas Neue, large
- Price in Space Grotesk 700
- "Add to Cart" or "Order Now" CTA in gold
- Subtle border or shadow

### Section Dividers
- Thin gold horizontal rules (`border: 1px solid #7A673F`)
- Or hexagonal geometric separators

---

## Photography & Media

### Hero Image
- File: `US-HEADER.jpg` (3840×2160 — full 4K)
- Full-bleed, dark overlay, product or brand imagery
- Overlaid with white headline text

### Product Photography Style
- Dark/black backgrounds
- Dramatic side lighting to show hexagonal geometry
- High contrast, minimal props
- Files: `001-SPLIT.jpg`, `001-SMOKEY.jpg`, `product-19893.jpg`, `product-22136.jpg`, `product-20046.jpg`

### Gallery / Instagram Grid
- Square format images
- Lifestyle shots, range use, manufacturing process
- 12 gallery images saved in `/assets/images/gallery-*.jpeg`

---

## Social Channels
| Platform | Handle | Notes |
|----------|--------|-------|
| Instagram | @unorthodoxsupression | MISSPELLED — missing a 'p'. Fix to @unorthodoxsuppression |
| YouTube | @GriffinArms | Should migrate to @UnorthodoxSuppression |
| Facebook | griffinarmsllc86 | Griffin Arms LLC brand |

---

## Content Inventory

### Pages
| Page | URL | Status |
|------|-----|--------|
| Home | / | Live — strong hero, placeholder shop section |
| Shop | /shop | Live — ALL products are placeholders ($25 "Product Name") |
| About | /about | Live — good brand story content |
| Contact | /contact | Live — form + reCAPTCHA, no hours/map |
| Privacy Policy | /privacy-policiy | Live — note the TYPO in URL ("policiy") |

### Squarespace Site IDs (for reference / export)
- **Site ID:** `6952fed7d9ebd61506c03277`
- **Shop Collection ID:** `6952ff84809a9f25ef6bd311`
- **Contact Form ID:** `6969a8744b133c7a59688783`
- **Template:** viola-clarinet-lsjc

---

## WordPress Rebuild Checklist

### Theme Requirements
- [ ] Dark background (#111) as site default
- [ ] Bebas Neue + Archivo Black + Space Grotesk loaded
- [ ] Gold (#7A673F) as primary accent color
- [ ] Sharp corners on all buttons and cards (no border-radius)
- [ ] Announcement bar at top
- [ ] Fixed transparent-to-solid header on scroll
- [ ] Full-bleed hero with overlay text
- [ ] Hexagonal motif in design elements where possible
- [ ] 21+ age gate on entry
- [ ] Mobile-first responsive

### Plugins Needed
- Age Gate (21+ modal)
- WooCommerce (core)
- Astra Pro or Kadence Pro (theme)
- Elementor Pro (page builder)
- Yoast SEO (meta/sitemap)
- WPForms Pro (contact form + reCAPTCHA)
- FFL Checkout by Texas Technology Group (dealer selection)
- WooCommerce Product Add-Ons (muzzle adapter upsell)
- Instagram Feed by Smash Balloon (gallery)
- Site Kit by Google (GA4 + Search Console)
