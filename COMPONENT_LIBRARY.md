# Racespot.tv Component Library

---

## 1. Navigation

### Global Header

```
┌─────────────────────────────────────────────────────────────────────┐
│ [RACESPOT▶] │ HOME  BROADCASTS  EVENTS  SERVICES  CALENDAR  LIVE  NEWS │ [DE/EN] │
└─────────────────────────────────────────────────────────────────────┘
```

**Specs:**
- Height: 64px desktop, 56px mobile
- Background: `#0A0A0A` with `border-bottom: 1px solid #1A1A1A`
- Logo: Eurostile Bold, "RACESPOT" + yellow play triangle `▶`
- Nav links: 13px, uppercase, letter-spacing 0.08em, weight 600
- Active state: Yellow bottom border (2px)
- Hover: Yellow text color
- Sticky on scroll with backdrop blur
- Mobile: hamburger → full-screen overlay menu

**State variants:**
- Default: transparent or #0A0A0A
- Scrolled: `background: rgba(10,10,10,0.95); backdrop-filter: blur(8px)`
- With LIVE active: Red "● LIVE" badge pulsing in nav

---

## 2. Buttons

### Primary CTA Button
```
┌─────────────────────┐
│  ▶  WATCH LIVE NOW  │
└─────────────────────┘
```
- Background: `#F5C000`
- Text: `#0A0A0A`, Eurostile, 13px, uppercase, weight 700, letter-spacing 0.1em
- Padding: 14px 28px
- Border-radius: 4px
- Hover: background `#E0A800`, slight scale 1.02
- Icon: optional left icon (play, arrow, etc.)

### Secondary Button (Outline)
```
┌─────────────────────┐
│   LEARN MORE  →     │  (yellow border, no fill)
└─────────────────────┘
```
- Border: `2px solid #F5C000`
- Text: `#F5C000`
- Background: transparent
- Hover: background `rgba(245,192,0,0.1)`

### Ghost Button
```
   VIEW ALL BROADCASTS →
```
- No border, no background
- Text: `#888888`
- Hover: text `#FFFFFF`
- Arrow slides right on hover

### Danger / Contact Button
```
┌──────────────────────┐
│   REQUEST A QUOTE    │
└──────────────────────┘
```
- White background, black text (for light sections)

---

## 3. Badges & Labels

### LIVE Badge
```
  ● LIVE
```
- Background: `#E53E3E`
- Text: white, 11px, uppercase, bold
- Padding: 4px 10px
- Border-radius: 4px
- Red dot with pulse animation
- Used on: nav, cards, hero

### Status Badge
```
  UPCOMING   |   PAST   |   TODAY
```
- Upcoming: yellow text, yellow border, transparent bg
- Past: muted text, muted border
- Today: white text, yellow background

### Category Label
```
  ESPORTS   |   MOTORSPORT   |   BEHIND THE SCENES
```
- Background: `rgba(245,192,0,0.1)`
- Text: `#F5C000`, 11px, uppercase, letter-spacing 0.1em

### Language Badge
```
  DE   EN   FI   NO   PT   ES   KO   DA
```
- Pill style, 24px height
- Active: yellow fill
- Inactive: border only

---

## 4. Cards

### Broadcast Card (Video Thumbnail)
```
┌──────────────────────────────┐
│ ████████████████████████████ │  ← 16:9 thumbnail
│ ████  ● LIVE  ████████████  │  ← badge overlay top-left
│ █████████████████████████▶  │  ← play button center
└──────────────────────────────┘
│ IRACING · GT3 CHAMPIONSHIP   │  ← category label
│ Racespot iRacing GT3 World..  │  ← title (2 lines max)
│ ↗ 2.1M views · Mar 2026      │  ← meta
└──────────────────────────────┘
```

**Specs:**
- Background: `#111111`
- Border: `1px solid #1A1A1A`
- Border-radius: 8px
- Hover: border-color `#F5C000`, scale 1.02, shadow yellow glow
- Thumbnail: always 16:9 with dark overlay
- LIVE variant: red pulsing badge top-left

### Event Card
```
┌──────────────────────────────┐
│  JUL    │                   │
│   08    │  RACE WEEK 2026   │
│  2026   │  Cologne, Germany │
│         │  ★★★★★ FLAGSHIP   │
└─────────┴───────────────────┘
│  08–12 July · Capacity 1500  │
│  [REGISTER INTEREST →]       │
└──────────────────────────────┘
```

- Date column: yellow background, black text, Eurostile
- Content: dark background
- Yellow CTA button at bottom
- Category: RACE WEEK shown as special badge

### News/Editorial Card
```
┌──────────────────────────────┐
│  [Category Image 16:9]       │
└──────────────────────────────┘
│ BEHIND THE SCENES            │  ← category
│ How We Broadcast 400+ Events │  ← headline (2 lines)
│ By Philip Stamm · Mar 2026   │  ← author + date
└──────────────────────────────┘
```

### Team Member Card
```
┌──────────────────────────────┐
│  ╭──────────╮                │
│  │  [PHOTO] │                │
│  ╰──────────╯                │
│  Philip Stamm                │
│  CEO & Founder               │
│  Simracing since 1997        │
│  [LinkedIn ↗]                │
└──────────────────────────────┘
```

### Service Card
```
┌──────────────────────────────┐
│  ◉  BROADCAST PRODUCTION     │
│─────────────────────────────-│
│  400+ events/year            │
│  TV partnerships             │
│  8 languages                 │
│  100M+ impressions/year      │
│─────────────────────────────-│
│  [GET A QUOTE →]             │
└──────────────────────────────┘
```

- Icon top-left (yellow)
- Feature list with yellow checkmarks
- CTA button at base
- Hover: yellow left border (4px accent)

### Stat Card
```
┌──────────────────────────────┐
│         400+                 │
│  Broadcasts per year         │
└──────────────────────────────┘
```
- Large number: Eurostile, 48-64px, yellow
- Label: white, 14px
- Background: subtle border card

---

## 5. Hero Sections

### Full-Bleed Video Hero
```
┌─────────────────────────────────────────────────────┐
│ [BACKGROUND VIDEO / IMAGE - full viewport]           │
│                                                      │
│  ● LIVE NOW                                          │
│                                                      │
│  RACESPOT IRACING                                    │
│  GT3 WORLD                                           │
│  CHAMPIONSHIP                                        │
│                                                      │
│  Round 3 · Monza · 10,000 watching                  │
│                                                      │
│  [▶ WATCH LIVE]    [VIEW SCHEDULE]                  │
└─────────────────────────────────────────────────────┘
```

- Full viewport height (100vh)
- Dark overlay: `linear-gradient(to right, rgba(10,10,10,0.95) 40%, rgba(10,10,10,0.4) 100%)`
- Content max-width: 720px, vertically centered left
- LIVE badge with red pulse above title
- Title: Eurostile, 64-80px, all-caps, stacked

### Event Countdown Hero
```
┌─────────────────────────────────────────────────────┐
│ [RACE WEEK 2026 artwork background]                 │
│                                                      │
│  RACE WEEK 2026                                      │
│  Europe's Festival of Virtual Motorsport             │
│                                                      │
│  08 JULY 2026 · COLOGNE, GERMANY                    │
│                                                      │
│  [  82  ]  [  14  ]  [  36  ]  [  22  ]            │
│    DAYS      HRS      MIN       SEC                  │
│                                                      │
│  [REGISTER INTEREST]    [PARTNER WITH US]           │
└─────────────────────────────────────────────────────┘
```

---

## 6. Navigation Ticker (Breaking News Style)

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
● LIVE  iRacing GT3 Round 3 ·  ● UPCOMING  NASCAR 25 Oval Series Thu 20:00 CET  ·  RESULTS: Le Mans Virtual - Racespot tops 2.1M views
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

- Yellow background, black text
- Auto-scrolling left
- Dots and separators between items
- Red "● LIVE" prefix for live events

---

## 7. Forms

### Quote Request Form
```
┌────────────────────────────────────────────┐
│  REQUEST A QUOTE                           │
├────────────────────────────────────────────┤
│  Name *           [________________________]│
│  Company *        [________________________]│
│  Email *          [________________________]│
│  Service          [▼ Select service        ]│
│  Budget Range     [▼ Select range          ]│
│  Message          [________________________]│
│                   [________________________]│
│                   [________________________]│
│                      [SEND REQUEST →]      │
└────────────────────────────────────────────┘
```

- Dark background inputs (`#1A1A1A`)
- Yellow focus border
- Error state: red border + message below
- Success: yellow checkmark + "We'll be in touch within 24h"

### Newsletter
```
│ Stay updated on broadcasts & events        │
│ [your@email.com_____________] [SUBSCRIBE →]│
```

---

## 8. Calendar Component

### Month View Header
```
  ← FEBRUARY 2026         MARCH 2026         APRIL 2026 →
  [MONTH] [WEEK] [LIST]                    [TODAY]
```

### Day Cell
```
┌─────────┐    ┌─────────┐
│  Sat 7  │    │  Sun 8  │ ← today (yellow border)
│         │    │         │
│ ● iRacer│    │ ◑ NASCAR│
│   GT3   │    │   25    │
│  20:00  │    │  18:00  │
└─────────┘    └─────────┘
```

- Event dots: yellow (Racespot broadcast), white (external)
- LIVE events: red dot with pulse
- Click → modal with full event details + watch link

---

## 9. Video Player Component

### Embedded YouTube Player
```
┌──────────────────────────────────────────────────────┐
│ ██████████████ VIDEO PLAYER █████████████████████████│
│ ██████████████  (YouTube embed or placeholder)███████│
│ ██████████████████████████████████████████████████▶ │
│ ─────────────────────────── 42:17 / 1:32:44 ─────── │
└──────────────────────────────────────────────────────┘
│ [Share] [Open in YouTube] [Fullscreen]               │
│ GT3 World Championship - Round 3 - Monza            │
│ 10,243 watching                                      │
```

### Stream Grid (Multiple Live)
```
┌─────────────────┐  ┌─────────────────┐
│  [STREAM 1 ●]  │  │  [STREAM 2]     │
│  GT3 · iRacing  │  │  NASCAR 25      │
└─────────────────┘  └─────────────────┘
```

---

## 10. Footer

```
┌─────────────────────────────────────────────────────────────────┐
│ [RACESPOT▶]                                                      │
│ The world's leading simracing broadcast studio.                  │
│ Cologne, Germany                                                 │
│                                                                  │
│ BROADCASTS    SERVICES    EVENTS    COMPANY    LEGAL             │
│ Portfolio     Production  Calendar  About       Privacy          │
│ Live Streams  Esports     RACE WEEK Team        Imprint         │
│ Archive       Events      Past      Contact     Terms            │
│                                                                  │
│ ─────────────────────────────────────────────────────────────── │
│ [YouTube] [Twitch] [Instagram] [LinkedIn] [X/Twitter]           │
│ © 2026 Racespot GmbH · Cologne, Germany    [DE] [EN]            │
└─────────────────────────────────────────────────────────────────┘
```

---

## 11. Modal / Overlay

### Event Detail Modal
```
┌────────────────────────────────────┐
│  [×]                               │
│  ● LIVE NOW                        │
│                                    │
│  iRacing GT3 World Championship    │
│  Round 3 — Monza Circuit           │
│                                    │
│  Sat, 8 Mar 2026 · 20:00 CET      │
│  Language: English / German        │
│                                    │
│  [▶ WATCH LIVE]  [+ ADD TO CAL]  │
└────────────────────────────────────┘
```

- Backdrop: `rgba(0,0,0,0.85)` blur
- Modal: `#111111`, border `1px solid #2A2A2A`
- Yellow CTA primary

---

## 12. Section Headers

### Standard Section Header
```
  ──── LATEST BROADCASTS ──────────────────── [VIEW ALL →]
```

- Yellow 3px line left
- Label: 11px, uppercase, letter-spacing 0.15em
- "View all" ghost button right-aligned

### Stat Bar (between sections)
```
┌──────────┬──────────┬──────────┬──────────┐
│  400+    │  100M+   │  2.5M+   │    8     │
│  Events  │ Impressions│ YouTube │ Languages│
│  Per Year│  Per Year │  Views  │  Covered │
└──────────┴──────────┴──────────┴──────────┘
```

- Full-width yellow background section
- Numbers: Eurostile, 48px, black
- Labels: 13px, uppercase, black, muted

---

## 13. Loading States

### Skeleton Card
```
┌──────────────────────────────┐
│  ▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓  │  ← shimmer animation
│  ▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓  │
│  ▓▓▓▓▓▓▓▓▓                  │
└──────────────────────────────┘
```

- Background: `#1A1A1A` with shimmer sweep `#2A2A2A`
- Used while fetching Google Sheets calendar data

---

## Component Token Reference

```css
:root {
  /* Colors */
  --color-yellow:    #F5C000;
  --color-black:     #0A0A0A;
  --color-white:     #FFFFFF;
  --color-surface-1: #111111;
  --color-surface-2: #1A1A1A;
  --color-border:    #2A2A2A;
  --color-muted:     #888888;
  --color-live:      #E53E3E;

  /* Typography */
  --font-display: 'Eurostile', 'Oswald', sans-serif;
  --font-body:    'Inter', Arial, sans-serif;

  /* Spacing */
  --container-max:   1280px;
  --section-padding: 80px;
  --card-padding:    24px;

  /* Transitions */
  --transition: all 250ms cubic-bezier(0.4, 0, 0.2, 1);
}
```
