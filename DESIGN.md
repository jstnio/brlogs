---
name: BRLOGS
description: Bold freight forwarding — two worlds connected by decisive logistics.
colors:
  navy-deep: "#10153c"
  navy-surface: "#1b2045"
  cargo-gold: "#E8A020"
  ink: "#F0F4FF"
  muted-slate: "#6B8BAD"
  button-hover: "#f5b540"
  input-fill: "rgba(255,255,255,.06)"
  input-border: "rgba(255,255,255,.12)"
typography:
  display:
    fontFamily: "Bebas Neue, Impact, sans-serif"
    fontSize: "clamp(3.2rem, 9vw, 6rem)"
    fontWeight: 400
    lineHeight: 0.92
    letterSpacing: "0.02em"
  body:
    fontFamily: "Barlow, Arial, sans-serif"
    fontSize: "clamp(0.9rem, 2vw, 1.1rem)"
    fontWeight: 400
    lineHeight: 1.65
    letterSpacing: "0.12em"
  label:
    fontFamily: "Barlow, Arial, sans-serif"
    fontSize: "0.72rem"
    fontWeight: 600
    lineHeight: 1.4
    letterSpacing: "0.14em"
rounded:
  sharp: "2px"
  pill: "100px"
spacing:
  xs: "8px"
  sm: "16px"
  md: "24px"
  lg: "48px"
  xl: "3rem"
components:
  button-primary:
    backgroundColor: "{colors.cargo-gold}"
    textColor: "{colors.navy-deep}"
    rounded: "{rounded.sharp}"
    padding: "0.8rem 1.8rem"
  button-primary-hover:
    backgroundColor: "{colors.button-hover}"
  notify-input:
    backgroundColor: "{colors.input-fill}"
    textColor: "{colors.ink}"
    rounded: "{rounded.sharp}"
    padding: "0.8rem 1.2rem"
  service-pill:
    backgroundColor: "transparent"
    textColor: "{colors.muted-slate}"
    rounded: "{rounded.pill}"
    padding: "0.45rem 1rem"
---

# Design System: BRLOGS

## 1. Overview

**Creative North Star: "The Global Bridge"**

BRLOGS connects worlds. The design embodies that ambition physically: deep ocean-midnight backgrounds that evoke the open sea between origin and destination, a Cargo Gold accent that reads like a navigation beacon cutting through night water, and Bebas Neue headlines that feel stamped on a shipping manifest — compressed, unapologetic, built for scale. Every element communicates movement. The animated route lines crossing the hero are not decoration; they are the product.

This is not a startup. It is not a platform. It is a freight forwarder with decades of corridor knowledge encoded in its confidence. The typography leans in close, the layout refuses to hedge, and the palette commits fully to its identity. SMB importers and exporters — operators who move cargo across borders every week — need to see authority instantly. This system earns that read in under two seconds.

The system rejects three things by name: generic logistics clipart (stock-photo trucks, forgettable corporate blue), startup-pastel SaaS aesthetics (purple gradients, bubbly roundness, feature grids), and heavy corporate portal design (dense, form-heavy, government-feeling). Any element that could appear in any of those three categories is wrong here.

**Key Characteristics:**
- Dark-committed: navy-deep (#081629) covers 80%+ of the surface; no light-mode hedging
- Typographically bold: Bebas Neue display paired with Barlow body for industrial precision
- Accent economy: Cargo Gold appears only on CTAs, the divider, and interactive highlights
- Motion as metaphor: animated route lines and pulsing port dots reflect cargo in transit
- Sharp geometry: 2px radius on interactive elements; no rounded softness

## 2. Colors: The Trade Night Palette

A drenched-dark palette with a single warm signal against deep ocean.

### Primary
- **Cargo Gold** (`#E8A020` / `oklch(73% 0.18 70)`): The brand's sole warm accent. Used on the horizontal divider, the CTA button, the `<em>` highlight in the headline, and link hovers. Its warmth is the weight of value moving — tonnage made visible. **Never use on body text, never as a background fill, never on more than ~10% of any surface.**

### Neutral
- **Ocean Midnight** (`#081629` / `oklch(15% 0.05 250)`): The primary background. 80%+ of every page surface. Dark enough to read as night sea, tinted toward navy-blue (not gray, not black).
- **Deep Berth** (`#0d2145` / `oklch(22% 0.06 250)`): Secondary surface layer. Used for subtle elevation when needed (hover states, input focus tint).
- **Ink White** (`#F0F4FF`): Primary text color. Slightly blue-tinted white that harmonizes with the navy background. Never pure white.
- **Muted Slate** (`#6B8BAD` / `oklch(55% 0.07 245)`): Secondary text, labels, placeholders, pill borders. A desaturated mid-tone of the same blue hue.

### Named Rules

**The Beacon Rule.** Cargo Gold appears on ≤10% of any surface. Its rarity is what makes it a signal. If it's everywhere, it stops being a beacon and becomes noise.

**The No-Warm-Background Rule.** Cargo Gold is never used as a background fill on any block larger than a button. The dark palette is the identity; do not dilute it.

## 3. Typography

**Display Font:** Bebas Neue (sans-serif, condensed, uppercase-only)
**Body Font:** Barlow (geometric sans, multiple weights)

**Character:** Bebas Neue is a manifesto typed on heavy stock — compressed authority, zero ornamentation, built for shipping labels and port signage. Barlow is its engineered complement: geometric, cool, built for legibility at functional sizes. Together they read as industrial precision without pretension.

### Hierarchy

- **Display** (400 weight, `clamp(3.2rem, 9vw, 6rem)`, line-height 0.92, letter-spacing 0.02em): Hero headlines only. The uppercase-only nature of Bebas Neue makes this a stamp, not a sentence. Use `text-wrap: balance`.
- **Body** (400 weight, `clamp(0.9rem, 2vw, 1.1rem)`, line-height 1.65, letter-spacing 0.12em, uppercase): Subheadlines, navigation body, short descriptive lines. Barlow in light tracking reads as calm authority.
- **Label** (600 weight, 0.72rem, letter-spacing 0.14em, UPPERCASE): Footer metadata, pill labels, bottom-bar text. Tight spacing at small size; never at large.

### Named Rules

**The Two-Family Rule.** Bebas Neue for display only; Barlow for everything else. Never use Bebas Neue below 2rem. Never use a third typeface without a specific justification documented in PRODUCT.md.

**The Uppercase Discipline Rule.** Body copy and prose are NOT uppercase. Only labels (`label` role) and the Bebas Neue display role are uppercase. Tracking-uppercase on body copy reads as a design reflex, not voice.

## 4. Elevation

This system is deliberately flat. Depth is expressed through background color transitions (Ocean Midnight → Deep Berth), not shadows. The animated route lines and pulsing dots create perceived depth through motion, not layering.

No `box-shadow` is used on any element at rest. The sole exception: a mild ambient glow (`0 4px 24px rgba(232,160,32,0.15)`) may be used on the CTA button on hover to reinforce the beacon quality of Cargo Gold.

### Named Rules

**The Flat-by-Default Rule.** Surfaces are flat at rest. The button hover glow is the only permitted shadow. If you find yourself adding `box-shadow` anywhere else, question whether depth is actually needed.

## 5. Components

### Buttons

Sharp identity — 2px radius, no softness, no pill shape. The button is a stamp.

- **Shape:** Sharp rectangular (2px radius)
- **Primary:** Cargo Gold (`#E8A020`) background, Ocean Midnight (`#081629`) text, Bebas Neue label, letter-spacing 0.12em, padding 0.8rem 1.8rem
- **Hover:** Background brightens to `#f5b540`, translates `-2px` on Y axis. Transition: `background 0.2s, transform 0.15s`
- **Active:** Returns to translateY(0)
- **No ghost / secondary button** currently defined. If needed, use full border in Cargo Gold with transparent fill.

### Inputs / Fields

- **Style:** `rgba(255,255,255,0.06)` fill, `rgba(255,255,255,0.12)` border, 2px radius, Ink White text
- **Placeholder:** Muted Slate — must pass 4.5:1 contrast against the fill background
- **Focus:** Border shifts to Cargo Gold (`#E8A020`), fill shifts to `rgba(232,160,32,0.06)`
- **Width:** 260px default; wraps responsively on mobile with `flex-wrap`

### Service Pills

Taxonomy tags that communicate service breadth without a card grid.

- **Style:** Transparent fill, 1px Muted Slate border at 25% opacity, 100px radius, Muted Slate text (0.72rem, 600 weight, 0.14em tracking, uppercase)
- **No hover state** — these are informational only, not interactive

### Route Animation Layer

Signature component. Three SVG `<path>` elements with animated `stroke-dashoffset` simulate cargo routes across the globe. Nine `<circle>` elements pulse as port markers.

- **Paths:** Amber (`#E8A020`) and Muted Slate strokes, 1px width, `stroke-dasharray: 6 10`, 18% opacity at container level
- **Dots:** Amber and Ink White, pulse on a 3s ease-in-out cycle between r=3 and r=5, opacity 0.3–1
- **Reduced motion:** Animation stops; elements remain visible at their resting state (opacity 0.18 container, opacity 0.3 dots)

## 6. Do's and Don'ts

### Do:

- **Do** keep Cargo Gold rare — headline `<em>` highlight, divider line, CTA button, link hovers. If it appears on more than 10% of any screen, strip it back.
- **Do** use Bebas Neue only for hero display text (≥2rem). Below that it becomes illegible.
- **Do** keep the dark background as the dominant surface. Light sections or light cards on this brand feel like a tonal breach.
- **Do** pair motion with meaning. The route lines move because cargo moves. Any new animation should pass the same test.
- **Do** verify contrast: Muted Slate (`#6B8BAD`) on Ocean Midnight (`#081629`) must be tested at every usage — it is near the 4.5:1 floor for body-sized text.
- **Do** apply `text-wrap: balance` to all Bebas Neue headlines to prevent single-word orphan lines on narrow viewports.
- **Do** include `@media (prefers-reduced-motion: reduce)` that stops all `animation` properties while keeping elements visible at their default opacity.

### Don't:

- **Don't** use generic logistics imagery: stock-photo trucks, container ships as clip-art, airport cargo bays. This is a brand identity play, not an image-led page.
- **Don't** use startup-pastel SaaS aesthetics: no purple gradients, no rounded pill hero cards, no bubbly CTA shapes, no feature-grid with icon + heading + text.
- **Don't** use heavy corporate portal design: no dense form layouts, no government-portal typography, no nested table structures.
- **Don't** apply `border-left` greater than 1px as a colored stripe on any card or callout. Rewrite with background tints or full borders.
- **Don't** use `background-clip: text` gradient fills on any text. Single solid color only.
- **Don't** add a third typeface. Two families, one mission.
- **Don't** use Bebas Neue below 2rem. At small sizes it collapses.
- **Don't** add rounded corners beyond 2px on buttons or inputs. The sharpness is intentional.
- **Don't** use uppercase tracking on prose body copy. That reflex belongs to labels only.
- **Don't** add a `box-shadow` at element rest state. Flat by default; the Cargo Gold hover glow on the button is the only exception.
