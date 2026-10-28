---
name: FusiLite Labs
description: Small tools for better days. One at a time.
colors:
  sheet: "#ffd34e"
  sheet-dark: "#1a1546"
  ink: "#1d1648"
  ink-soft: "#3e356f"
  ink-dark: "#fff1c9"
  pop: "#b8341b"
  paper: "#ffffff"
  underside: "#ece8f6"
  cuewoven-vinyl: "#2350d8"
  cuewoven-tag: "#ffd23f"
  partfinder-vinyl: "#3b2357"
  partfinder-tag: "#f2aa3c"
typography:
  display:
    fontFamily: "Shrikhand, Atkinson Hyperlegible Next, sans-serif"
    fontSize: "clamp(3rem, 7.4vw, 6rem)"
    fontWeight: 400
    lineHeight: 0.98
    letterSpacing: "0em"
  display-second:
    fontFamily: "Shrikhand, Atkinson Hyperlegible Next, sans-serif"
    fontSize: "clamp(1.8rem, 3.6vw, 2.9rem)"
    fontWeight: 400
    lineHeight: 1.1
  body:
    fontFamily: "Atkinson Hyperlegible Next, system-ui, sans-serif"
    fontSize: "1.0625rem"
    fontWeight: 400
    lineHeight: 1.6
  label:
    fontFamily: "Atkinson Hyperlegible Next, system-ui, sans-serif"
    fontSize: "0.95rem"
    fontWeight: 700
rounded:
  label: "10px"
  mark: "12px"
  sticker: "30px"
  slot: "40px"
  panel: "40px"
  pill: "999px"
spacing:
  gutter: "16px"
  die-cut: "10px"
  panel-die-cut: "14px"
components:
  sticker:
    backgroundColor: "{colors.cuewoven-vinyl}"
    textColor: "{colors.paper}"
    rounded: "{rounded.sticker}"
    padding: "20px 22px"
  label-sticker:
    backgroundColor: "{colors.paper}"
    textColor: "{colors.ink}"
    rounded: "{rounded.label}"
    padding: "7px 14px"
  status-tag:
    backgroundColor: "{colors.cuewoven-tag}"
    textColor: "{colors.ink}"
    rounded: "{rounded.pill}"
    padding: "3px 12px"
  tool-panel:
    backgroundColor: "{colors.partfinder-vinyl}"
    textColor: "{colors.paper}"
    rounded: "{rounded.panel}"
---

# Design System: FusiLite Labs

## Overview

The page is one sticker sheet. A sunny marigold backing sheet (deep indigo in dark mode) owns the whole viewport; each extension is a die-cut vinyl sticker in that product's own colours with a thick white border, sitting in a dashed kiss-cut outline printed on the sheet. Facts are small white printed label stickers. The voice is one maker's, first person and optimistic. It refuses the centered SaaS hero over a row of equal rounded cards.

## Colors

### Primary
- **Sheet** `#ffd34e` (light) / `#1a1546` (dark): the backing sheet. It is the page, never an accent.
- **Ink** `#1d1648` (light) / `#fff1c9` (dark): all text printed on the sheet; secondary text uses Ink soft.

### Secondary
- **Pop** `#b8341b` (light) / sheet yellow (dark): the second display line only.
- Each product brings its own vinyl and tag colour: CueWoven blue `#2350d8` with yellow `#ffd23f`, Part Finder plum `#3b2357` with amber `#f2aa3c`.

### Neutral
- **Paper** `#ffffff`: die-cut borders and label stickers. Stays white in dark mode (stickers are physical).
- **Underside** `#ece8f6`: the back of a peeled corner.

### Named Rules
- **The sheet is the colour.** Never put a neutral page under the stickers.
- **Products keep their own colours.** A new tool arrives as a new vinyl colour, not a new page accent.

## Typography

- **Display:** Shrikhand (self-hosted, OFL), for the headline, product names and the wordmark. Never for body or labels.
- **Body and labels:** Atkinson Hyperlegible Next 400/700 (self-hosted, OFL).

### Hierarchy
Headline 3–6rem, second line 1.8–2.9rem, panel names 2.4–3.6rem, sticker names 1.65rem, body 1.0625rem, labels 0.95rem bold. Body measure stays under ~38em.

## Layout

Content width `min(1160px, 100% - 32px)`. First viewport: copy on the left (headline, second line, one first-person sentence, label stickers); the two stickers on the right, tilted (-3.5°, +2.5°) and offset. Below, one full-size panel per tool, screenshot opposite the copy (alternating sides). Under 860px everything stacks; screenshots crop to the product itself (CueWoven 3:4 from the right, Part Finder 7:8 at 86%). Under 420px a sticker stacks its icon above its text.

## Elevation & Depth

Stickers rest on the sheet with a soft offset shadow and lift on hover/focus.

### Shadow Vocabulary
- **Rest:** `0 6px 14px rgba(29,22,72,.22), 0 1px 3px rgba(29,22,72,.16)`
- **Lift:** `0 14px 28px rgba(29,22,72,.28), 0 3px 6px rgba(29,22,72,.18)`
- Dark mode uses black shadows at higher opacity.

## Shapes

Rounded die-cut rectangles only: stickers 30px, panels and kiss-cut slots 40px, labels 10px, tags fully rounded. No circles, blobs or polygons.

## Components

### Sticker (signature)
Link to the tool's panel. White 10px die-cut border, product vinyl fill, icon with a 4px white printed ring, name in display face, one-line job, status tag. On hover/focus it lifts 6px and the bottom-right corner peels back (sheet colour under it, Underside on the flap). On load the two stickers are pressed onto the sheet once (scale 1.06 to 1, 0.7s expo ease-out); nothing else animates. Reduced motion removes both.

### Label sticker
White, bold ink text, alternating ±1.5° tilt, Rest shadow on the sheet, no shadow inside a panel.

### Tool panel
A peeled-off sticker at full size: 14px white die-cut border, product vinyl, a static peeled corner at top right, name, job line, status tag, two short paragraphs, label stickers, text links in white.

### Navigation
A small white wordmark label (tilted -2°) and the support email. No menu.

## Do's and Don'ts

### Do:
- Show the real product screenshots and say facts plainly ("No account", "No tracking").
- Keep the maker's first-person voice.
- Theme selection, focus rings and scrollbars from the palette.

### Don't:
- Add eyebrows/kickers above headings, gradient text, glass, or a neutral card grid.
- Invent store links, user counts, ratings or testimonials.
- Use the display face for body text or labels.
