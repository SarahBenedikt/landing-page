# Style Guide — Sarah Benedikt Consulting

This is the single source of truth for brand colors, typography, and UI patterns.
Any new page or component should reference this file before introducing new values.

---

## Color Palette

### Backgrounds & Structure

| Token | Hex | Usage |
|-------|-----|-------|
| `color-bg-dark` | `#1a2332` | Header, footer, all dark section backgrounds, nav bar |
| `color-bg-light` | `#f7f8f9` | Light content sections (`.wrapper.style5`) |
| `color-bg-code` | `#1e242b` | Code block backgrounds |

### Brand Accent

| Token | Hex | Usage |
|-------|-----|-------|
| `color-accent-primary` | `#3a6897` | Primary CTA buttons, focus rings, icon highlights, step numbers, borders on accent elements |
| `color-accent-primary-hover` | `#2d6099` | Hover state for primary accent |
| `color-accent-primary-active` | `#163a5e` | Active/pressed state for primary accent |
| `color-accent-secondary` | `#2c4a6e` | Secondary section backgrounds (`.wrapper.style2` variant) |
| `color-accent-cta` | `#1e4d7b` | Filled CTA button background (`.button.primary`) |
| `color-accent-cta-hover` | `#2d6099` | Hover state for CTA button |
| `color-accent-cta-active` | `#163a5e` | Active state for CTA button |

### Chart Colors (monochromatic slate blue scale)

| Token | Hex / rgba | Usage |
|-------|-----------|-------|
| `color-chart-1` | `rgba(58, 104, 151, 0.85)` | Chart segment / bar 1 (strongest) |
| `color-chart-2` | `rgba(107, 157, 194, 0.85)` | Chart segment / bar 2 |
| `color-chart-3` | `rgba(164, 196, 220, 0.85)` | Chart segment / bar 3 |
| `color-chart-4` | `rgba(208, 227, 240, 0.85)` | Chart segment / bar 4 (lightest) |
| `color-chart-star` | `#c9a84c` | Star ratings only — warm gold, used nowhere else |

### Icon Accents (on dark section backgrounds)

| Token | Hex | Usage |
|-------|-----|-------|
| `color-icon-1` | `#ffffff` | `.icon.style1` — strongest contrast |
| `color-icon-2` | `#d0e3f0` | `.icon.style2` — medium |
| `color-icon-3` | `#a4c4dc` | `.icon.style3` — subtle |

### Text

| Token | Hex | Usage |
|-------|-----|-------|
| `color-text-body` | `#2c2c2e` | Body text on light backgrounds |
| `color-text-muted` | `#6b7280` | Secondary / muted text on light backgrounds |
| `color-text-on-dark` | `#ffffff` | Primary text on dark backgrounds |
| `color-text-on-dark-muted` | `rgba(255, 255, 255, 0.5)` | Muted text on dark backgrounds |

### Section Text (on accent-colored backgrounds)

| Token | Hex | Usage |
|-------|-----|-------|
| `color-text-accent-light` | `#d0e3f0` | Body text on `color-accent-primary` sections |
| `color-text-accent-muted` | `#a4c4dc` | Dimmed text on `color-accent-primary` sections |
| `color-text-secondary-light` | `#ccd9e8` | Body text on `color-accent-secondary` sections |
| `color-text-secondary-muted` | `#9ab5cc` | Dimmed text on `color-accent-secondary` sections |

### Borders & Dividers

| Token | Hex | Usage |
|-------|-----|-------|
| `color-border-light` | `#e4e6ea` | Borders and `<hr>` on light sections |
| `color-border-on-dark` | `rgba(255, 255, 255, 0.1)` | Borders on dark backgrounds (cards, containers) |
| `color-border-testimonial` | `rgba(255, 255, 255, 0.2)` | Left border on testimonial quotes |

---

## Typography

All type is set in **Open Sans** (loaded via Google Fonts).

| Role | Weight | Size | Transform |
|------|--------|------|-----------|
| Page / section headings | 800 | `1.75em` | Uppercase + letter-spacing |
| Sub-headings | 600 | `1.35em` | Uppercase + letter-spacing |
| Body copy | 400 | `1em` | None |
| Muted labels / attribution | 400 | `0.82–0.9em` | None |
| Code | Courier New, monospace | `0.9em` | None |

---

## Buttons

| Variant | Class | Style | When to use |
|---------|-------|-------|-------------|
| Primary CTA | `.button.primary` | Filled — `#1e4d7b` background, white text | Single most important action per page (e.g. Get in Touch) |
| Secondary / navigation | `.button` or `.button.small` | Outline — white border on dark bg | Supporting links, page navigation, deeper exploration |

**Rule:** Never use more than one `.button.primary` in the same visible viewport. Hierarchy breaks if everything is filled.

---

## Gradients

### Hero / page header overlay (left-to-right directional)

Used on both the homepage banner and all subpage headers to keep the photo visible on the right.

```css
background-image: linear-gradient(
  to right,
  rgba(0,0,0,0.82) 0%,
  rgba(0,0,0,0.55) 40%,
  rgba(0,0,0,0.15) 65%,
  rgba(0,0,0,0)    85%
), url("path/to/banner.jpg");
background-position: 65% center;
```

---

## Layout Rules

- **Left alignment** — hero text and subpage header text align left at `padding-left: 8%`. Reverts to centered on mobile (≤736px).
- **Content max-width** — `.inner` containers cap at their framework defaults. Testimonial strip caps at `62em`.
- **Section backgrounds alternate** — dark → dark spotlight → dark → CTA → light content. Do not insert a new light section between dark ones without reviewing contrast.

---

## What NOT to use

These colors were part of the original HTML5 UP template and have been deliberately removed. Do not reintroduce them.

| Removed | Was used for | Replaced by |
|---------|-------------|-------------|
| `#21b2a6` teal | Buttons, CTA bg | `#3a6897` slate blue |
| `#ed4933` red-orange | Primary buttons | `#1e4d7b` navy |
| `#505393` muted purple | Section bg | `#2c4a6e` deep slate |
| `#00ffcc` neon green | Icon accent | `#ffffff` white |
| `#00f0ff` neon cyan | Icon accent | `#d0e3f0` light blue |
| `#76ddff` neon sky | Icon accent | `#a4c4dc` medium blue |
| `#8e44ad` wisteria purple | Charts, borders, steps | `#3a6897` slate blue |
