# Racespot.tv Layout Specifications

---

## Grid System

### Container

```css
.container {
  width: 100%;
  max-width: 1280px;
  margin: 0 auto;
  padding: 0 24px;
}

/* Wide variant (hero/full-bleed) */
.container--full {
  max-width: 100%;
  padding: 0;
}

/* Narrow variant (article, form) */
.container--narrow {
  max-width: 800px;
}
```

### Column Grid

12-column grid using CSS Grid:

```css
.grid {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  gap: 24px;
}

/* Common column spans */
.col-12 { grid-column: span 12; }  /* Full width */
.col-8  { grid-column: span 8; }   /* 2/3 */
.col-6  { grid-column: span 6; }   /* 1/2 */
.col-4  { grid-column: span 4; }   /* 1/3 */
.col-3  { grid-column: span 3; }   /* 1/4 */
```

---

## Breakpoints

| Name    | Value   | Description                |
|---------|---------|----------------------------|
| `xs`    | 375px   | Minimum mobile (iPhone SE) |
| `sm`    | 640px   | Large mobile / small tablet|
| `md`    | 768px   | Tablet portrait            |
| `lg`    | 1024px  | Tablet landscape / laptop  |
| `xl`    | 1280px  | Desktop (base container)   |
| `2xl`   | 1536px  | Wide desktop               |

```css
/* Media query system */
@media (min-width: 640px)  { /* sm  */ }
@media (min-width: 768px)  { /* md  */ }
@media (min-width: 1024px) { /* lg  */ }
@media (min-width: 1280px) { /* xl  */ }
@media (min-width: 1536px) { /* 2xl */ }
```

---

## Section Spacing

| Viewport | Section padding (vertical) | Between sections |
|----------|---------------------------|-----------------|
| Mobile   | 48px                       | 0               |
| Tablet   | 64px                       | 0               |
| Desktop  | 80px                       | 0               |
| Wide     | 96px                       | 0               |

Adjacent sections use background color changes as visual separators, not margins.

---

## Navigation Layout

### Desktop

```
[Logo 140px] ──[gap 48px]── [Nav links, flex, gap 32px] ──[push right]── [Lang 40px] [CTA 120px]
Total height: 64px
Position: sticky top 0, z-index 100
```

### Mobile

```
[Logo 120px] ──[push right]── [● LIVE badge?] [Hamburger 40px]
Total height: 56px
Position: sticky top 0
```

---

## Hero Section Specifications

### Full-Bleed Hero (Home, Events RACE WEEK)
```
Height:        100vh (min 600px, max 900px)
Background:    Video or image, object-fit cover
Overlay:       linear-gradient(to right, rgba(10,10,10,0.95) 35%, rgba(10,10,10,0.5) 70%, transparent 100%)
Content area:  left-aligned, vertically centered
Content width: max 640px
Padding:       0 24px → container
```

### Half-Height Hero (Interior pages)
```
Height:        50vh (min 360px, max 560px)
Background:    Image, object-fit cover, top center
Overlay:       rgba(10,10,10,0.75) solid overlay
Content:       centered, max-width 800px
Padding:       80px 24px
```

### Countdown Hero (RACE WEEK 2026)
```
Height:        100vh
Background:    Race Week artwork, darkened
Content:       centered, max-width 900px
Countdown:     4 blocks, 96px digits Eurostile
```

---

## Card Grids

### Broadcast Cards (Video)
```
Mobile  (< 640px):  1 column
Tablet  (640-1023): 2 columns, gap 16px
Desktop (1024px+):  3 columns, gap 24px
Wide    (1280px+):  4 columns, gap 24px
```

Aspect ratio: 16:9 thumbnail, text below
Card width: auto (fills column)

### Service Cards
```
Mobile:  1 column (stacked)
Tablet:  1 column
Desktop: 3 columns, equal width
```

Min height: 320px
Internal padding: 32px

### Team Cards
```
Mobile:  2 columns
Tablet:  3 columns
Desktop: 3 columns (centered if 3 people)
```

Photo: square or 3:4, centered above text
Centered text alignment

### News/Editorial Cards
```
Mobile:  1 column
Tablet:  2 columns
Desktop: 2-3 columns (featured + 2 secondary)
```

Featured card: spans full width or 2/3 width
Secondary: remaining columns

---

## Stat Bar

```
Mobile:   2×2 grid
Desktop:  4 columns horizontal
```

```css
.stats-bar {
  background: #F5C000;
  padding: 48px 24px;
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  text-align: center;
}

.stat-number {
  font-family: 'Eurostile', sans-serif;
  font-size: clamp(36px, 5vw, 64px);
  font-weight: 900;
  color: #0A0A0A;
}

.stat-label {
  font-size: 12px;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  color: #0A0A0A;
  opacity: 0.7;
}
```

---

## Calendar Layout

### Month View

```
Header row: 7 columns (Mon–Sun), 40px
Day cells:  auto height, min 120px desktop, 60px mobile
Event dot:  8px circle, yellow or red
```

```css
.calendar-grid {
  display: grid;
  grid-template-columns: repeat(7, 1fr);
  grid-auto-rows: minmax(120px, auto);
  border: 1px solid #2A2A2A;
}

.calendar-cell {
  border-right: 1px solid #1A1A1A;
  border-bottom: 1px solid #1A1A1A;
  padding: 8px;
}

.calendar-cell--today {
  border: 2px solid #F5C000;
}
```

### List View (Mobile preferred)

```
Full-width rows
Date column: 48px fixed
Content: flex grow
Each row: 72px height
```

---

## Ticker Layout

```css
.ticker {
  background: #F5C000;
  color: #0A0A0A;
  height: 36px;
  overflow: hidden;
  position: relative;
}

.ticker__content {
  display: flex;
  align-items: center;
  white-space: nowrap;
  animation: ticker-scroll 40s linear infinite;
}
```

---

## Video Embed Layout

### Primary Stream (Live page)

```css
.video-primary {
  position: relative;
  padding-bottom: 56.25%; /* 16:9 */
  height: 0;
  overflow: hidden;
  background: #111;
}

.video-primary iframe {
  position: absolute;
  top: 0; left: 0;
  width: 100%; height: 100%;
  border: none;
}
```

Max width: 100% on mobile, constrained on wide desktop (centered 1280px)

### Multi-stream Grid

```
2 streams: 2 columns, 16:9 each
3 streams: 2+1 or 3 equal
4+ streams: 2×2 grid
```

---

## Typography Responsive Scale

Using `clamp()` for fluid sizing:

```css
.hero-title    { font-size: clamp(40px, 7vw, 80px); }
.page-title    { font-size: clamp(32px, 5vw, 56px); }
.section-title { font-size: clamp(24px, 3.5vw, 36px); }
.card-title    { font-size: clamp(16px, 2vw, 22px); }
.body-text     { font-size: clamp(14px, 1.5vw, 16px); }
```

---

## Z-Index Layers

```
1    — Page content
10   — Sticky headers (ticker, section anchors)
100  — Navigation (sticky)
200  — Dropdowns, tooltips
300  — Modals backdrop
400  — Modals content
500  — Toasts, notifications
```

---

## Performance Targets

| Metric         | Target   | Notes                              |
|----------------|----------|------------------------------------|
| LCP            | < 2.5s   | Hero image/video preloaded         |
| FID            | < 100ms  | No render-blocking scripts         |
| CLS            | < 0.1    | Reserve space for images           |
| TTI            | < 3.5s   | Calendar loads after main content  |
| FCP            | < 1.8s   |                                    |

### Image Optimization
- Format: WebP with JPEG fallback
- Hero images: preloaded with `<link rel="preload">`
- Thumbnails: lazy loaded with `loading="lazy"`
- Aspect ratio boxes prevent CLS

### Video
- Hero video: poster image shown until autoplay possible
- YouTube embeds: use `loading="lazy"` on iframes
- Lite-YouTube-Embed component for performance

---

## Accessibility

### Focus Styles
```css
:focus-visible {
  outline: 2px solid #F5C000;
  outline-offset: 3px;
  border-radius: 2px;
}
```

### Color Contrast
- Yellow `#F5C000` on Black `#0A0A0A`: Contrast 13.7:1 (WCAG AAA)
- White `#FFFFFF` on Black `#0A0A0A`: Contrast 21:1 (WCAG AAA)
- Body text on dark surface: minimum 4.5:1 (WCAG AA)
- Muted text `#888888` on `#0A0A0A`: Contrast 5.7:1 (WCAG AA)

### Skip Links
```html
<a href="#main-content" class="skip-link">Skip to main content</a>
```

### ARIA Roles
- `role="banner"` on header
- `role="navigation"` on nav
- `role="main"` on main
- `role="contentinfo"` on footer
- `aria-live="polite"` on ticker and live status indicators
- `aria-label` on icon-only buttons

---

## RTL Support

Not required for initial launch. DE/EN both LTR. Note for future: abstract layout directions through logical CSS properties (`margin-inline-start` vs `margin-left`) where feasible.

---

## Print Styles

```css
@media print {
  .nav, .ticker, .video-embed, .cta-section { display: none; }
  body { background: white; color: black; }
  .hero { height: auto; }
}
```
