# Racespot.tv Design System

## Brand Philosophy

**"Precision in Motion"** — Racespot is the premium broadcast production studio for simracing. The design system reflects broadcast-grade professionalism with the energy and urgency of live motorsport.

---

## Color Palette

### Primary Colors

| Name           | Hex       | RGB               | Usage                                      |
|----------------|-----------|-------------------|--------------------------------------------|
| Racespot Yellow| `#F5C000` | rgb(245, 192, 0)  | CTAs, highlights, LIVE badges, logo accent |
| Racespot Black | `#0A0A0A` | rgb(10, 10, 10)   | Backgrounds, primary text on light         |
| Pure White     | `#FFFFFF` | rgb(255, 255, 255)| Text on dark, card backgrounds             |

### Secondary Colors

| Name           | Hex       | Usage                                 |
|----------------|-----------|---------------------------------------|
| Dark Surface   | `#111111` | Card backgrounds, nav                 |
| Mid Surface    | `#1A1A1A` | Section backgrounds, modals           |
| Border         | `#2A2A2A` | Dividers, card borders                |
| Muted Text     | `#888888` | Secondary text, metadata              |
| Light Gray     | `#F2F2F2` | Light mode backgrounds (rarely used)  |

### Semantic Colors

| Name      | Hex       | Usage                        |
|-----------|-----------|------------------------------|
| LIVE Red  | `#E53E3E` | Live indicator pulse         |
| Success   | `#38A169` | Confirmed events, success    |
| Warning   | `#DD6B20` | Upcoming alerts              |
| Info      | `#3182CE` | Info badges                  |

### Gradient System

```css
/* Hero gradient - dark to transparent */
--gradient-hero: linear-gradient(to right, rgba(10,10,10,1) 40%, transparent 80%);

/* Yellow accent glow */
--gradient-yellow: linear-gradient(135deg, #F5C000 0%, #E0A800 100%);

/* Card hover state */
--gradient-card-hover: linear-gradient(to bottom, transparent 0%, rgba(245,192,0,0.08) 100%);

/* Section separator */
--gradient-divider: linear-gradient(to right, transparent, #F5C000, transparent);
```

---

## Typography

### Font Stack

```css
/* Primary — Broadcast / Technical */
--font-primary: 'Eurostile', 'Eurostile Extended', 'Bank Gothic', 'Oswald', sans-serif;

/* Body — Clean readability */
--font-body: 'Inter', 'Helvetica Neue', Arial, sans-serif;

/* Monospace — Data, timestamps, counters */
--font-mono: 'JetBrains Mono', 'Courier New', monospace;
```

### Type Scale

| Token       | Size    | Weight | Line Height | Letter Spacing | Usage                    |
|-------------|---------|--------|-------------|----------------|--------------------------|
| `--text-xs` | 11px    | 500    | 1.4         | 0.08em         | Labels, badges, metadata |
| `--text-sm` | 13px    | 400    | 1.5         | 0.02em         | Caption, helper text     |
| `--text-base`| 16px   | 400    | 1.6         | 0              | Body copy                |
| `--text-md` | 18px    | 500    | 1.5         | -0.01em        | Lead paragraphs          |
| `--text-lg` | 22px    | 600    | 1.4         | -0.02em        | Card titles, subheads    |
| `--text-xl` | 28px    | 700    | 1.3         | -0.03em        | Section headers          |
| `--text-2xl`| 36px    | 700    | 1.2         | -0.04em        | Page titles              |
| `--text-3xl`| 48px    | 800    | 1.1         | -0.05em        | Hero headlines           |
| `--text-4xl`| 64px    | 900    | 1.0         | -0.06em        | Super hero text          |
| `--text-5xl`| 80px+   | 900    | 0.95        | -0.07em        | Full-bleed display text  |

### Text Treatments

```css
/* ALLCAPS label style */
.label-caps {
  font-family: var(--font-primary);
  font-size: 11px;
  font-weight: 700;
  letter-spacing: 0.15em;
  text-transform: uppercase;
}

/* Hero headline treatment */
.hero-title {
  font-family: var(--font-primary);
  font-weight: 900;
  text-transform: uppercase;
  letter-spacing: -0.05em;
  line-height: 0.95;
}

/* Section title with yellow underline */
.section-title::after {
  content: '';
  display: block;
  width: 48px;
  height: 3px;
  background: #F5C000;
  margin-top: 12px;
}
```

---

## Spacing System

Based on 8px grid:

```
--space-1:   4px
--space-2:   8px
--space-3:  12px
--space-4:  16px
--space-5:  20px
--space-6:  24px
--space-8:  32px
--space-10: 40px
--space-12: 48px
--space-16: 64px
--space-20: 80px
--space-24: 96px
--space-32: 128px
```

---

## Border & Radius

```css
--radius-sm:  4px    /* Badges, tags */
--radius-md:  8px    /* Cards, inputs */
--radius-lg: 12px    /* Modal, overlay panels */
--radius-xl: 16px    /* Large cards */
--radius-pill: 999px /* Pills, status badges */

--border-thin:   1px solid #2A2A2A
--border-medium: 2px solid #2A2A2A
--border-yellow: 2px solid #F5C000
--border-glow:   0 0 0 2px rgba(245, 192, 0, 0.4)
```

---

## Shadow System

```css
--shadow-sm:   0 1px 3px rgba(0,0,0,0.4);
--shadow-md:   0 4px 12px rgba(0,0,0,0.5);
--shadow-lg:   0 12px 40px rgba(0,0,0,0.6);
--shadow-xl:   0 24px 64px rgba(0,0,0,0.7);
--shadow-yellow: 0 0 20px rgba(245,192,0,0.3);
--shadow-inset: inset 0 1px 0 rgba(255,255,255,0.05);
```

---

## Animation & Motion

```css
/* Timing functions */
--ease-sharp:    cubic-bezier(0.4, 0, 0.2, 1)
--ease-bounce:   cubic-bezier(0.34, 1.56, 0.64, 1)
--ease-smooth:   cubic-bezier(0.25, 0.46, 0.45, 0.94)

/* Duration */
--duration-fast:   150ms
--duration-base:   250ms
--duration-slow:   400ms
--duration-slower: 600ms

/* Common transitions */
--transition-all:    all var(--duration-base) var(--ease-sharp);
--transition-color:  color var(--duration-fast) var(--ease-sharp);
--transition-bg:     background-color var(--duration-fast) var(--ease-sharp);
--transition-transform: transform var(--duration-base) var(--ease-smooth);
```

### Keyframe Animations

```css
/* LIVE pulse indicator */
@keyframes live-pulse {
  0%, 100% { opacity: 1; transform: scale(1); }
  50%       { opacity: 0.6; transform: scale(1.1); }
}

/* Ticker scroll */
@keyframes ticker-scroll {
  from { transform: translateX(100%); }
  to   { transform: translateX(-100%); }
}

/* Fade in up */
@keyframes fade-in-up {
  from { opacity: 0; transform: translateY(20px); }
  to   { opacity: 1; transform: translateY(0); }
}

/* Yellow flash on hover */
@keyframes yellow-flash {
  0%   { box-shadow: 0 0 0 0 rgba(245,192,0,0.6); }
  70%  { box-shadow: 0 0 0 10px rgba(245,192,0,0); }
  100% { box-shadow: 0 0 0 0 rgba(245,192,0,0); }
}
```

---

## Iconography

- **Icon Library:** Lucide or Heroicons (outline style)
- **Sizes:** 16px (inline), 20px (default), 24px (action), 32px (feature)
- **Color:** Inherit from text color; yellow for active/accent states
- **Custom Icons:**
  - Checkered flag (motorsport identifier)
  - Broadcast tower (services)
  - Steering wheel
  - Headphones/commentary
  - Lap timer display

---

## Image Treatment

### Video Thumbnails
- **Aspect ratio:** 16:9
- **Overlay:** Dark gradient bottom-left for text legibility
- **Hover:** Scale 1.05, reduce overlay opacity
- **LIVE badge:** Absolute top-left, red with pulse

### Portrait Images (Team)
- **Aspect ratio:** 3:4 or 1:1 (cropped to circle on mobile)
- **Treatment:** High contrast, slight desaturation
- **Hover:** Grayscale removed, yellow border glow

### Hero/Background Images
- Deeply darkened (60-80% overlay)
- Always paired with strong typography
- Video backgrounds preferred when available

---

## Dark Mode Default

The site is **dark-first**. All components default to dark backgrounds. No light/dark toggle needed — the brand is dark with yellow accents.

Dark surface hierarchy:
```
Page background:  #0A0A0A
Section alt:      #111111
Card surface:     #141414
Card elevated:    #1A1A1A
Input background: #1E1E1E
```
