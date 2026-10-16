---
name: David Salazar Portfolio
description: A calm, warm one-page portfolio in cream and pastel orange, set in two grotesks, with no shadows.
colors:
  cream-bg: "#f8efe3"
  sand-surface: "#f1e1cd"
  apricot-step: "#f7d0b4"
  cocoa-ink: "#2e2218"
  umber-muted: "#6a5443"
  peach-accent: "#f5bd9b"
  peach-accent-hover: "#f0ae88"
  terracotta-chart: "#eaa781"
typography:
  display:
    fontFamily: "Cabinet Grotesk, Switzer, system-ui, sans-serif"
    fontSize: "clamp(2.25rem, 1.4rem + 2vw, 3.25rem)"
    fontWeight: 500
    lineHeight: 1.25
    letterSpacing: "-0.03em"
  case-title:
    fontFamily: "Cabinet Grotesk, Switzer, system-ui, sans-serif"
    fontSize: "clamp(2.5rem, 1.5rem + 6vw, 6rem)"
    fontWeight: 500
    lineHeight: 1
    letterSpacing: "-0.04em"
  headline:
    fontFamily: "Cabinet Grotesk, Switzer, system-ui, sans-serif"
    fontSize: "clamp(1.75rem, 1.4rem + 1.2vw, 2.25rem)"
    fontWeight: 500
    lineHeight: 1.1
    letterSpacing: "-0.03em"
  title:
    fontFamily: "Cabinet Grotesk, Switzer, system-ui, sans-serif"
    fontSize: "clamp(1.25rem, 1.1rem + 0.7vw, 1.625rem)"
    fontWeight: 500
    lineHeight: 1.2
    letterSpacing: "-0.02em"
  body:
    fontFamily: "Switzer, system-ui, sans-serif"
    fontSize: "clamp(1.0625rem, 1rem + 0.25vw, 1.1875rem)"
    fontWeight: 400
    lineHeight: 1.55
    letterSpacing: "0"
  label:
    fontFamily: "Switzer, system-ui, sans-serif"
    fontSize: "clamp(0.875rem, 0.85rem + 0.1vw, 0.9375rem)"
    fontWeight: 400
    lineHeight: 1.55
    letterSpacing: "0"
rounded:
  sm: "3px"
  control: "10px"
  image: "10px"
  container: "18px"
spacing:
  tap: "44px"
  section-phone: "72px"
  section-wide: "96px"
  gutter: "20px"
components:
  button-primary:
    backgroundColor: "{colors.peach-accent}"
    textColor: "{colors.cocoa-ink}"
    rounded: "{rounded.control}"
    padding: "0 20px"
    height: "44px"
  button-primary-hover:
    backgroundColor: "{colors.peach-accent-hover}"
  tab-bar:
    backgroundColor: "{colors.sand-surface}"
    rounded: "{rounded.control}"
    padding: "4px"
  tab-pill:
    backgroundColor: "{colors.apricot-step}"
    rounded: "{rounded.sm}"
  demo-card:
    backgroundColor: "{colors.sand-surface}"
    rounded: "{rounded.container}"
    padding: "20px"
  brief-card:
    backgroundColor: "{colors.sand-surface}"
    rounded: "{rounded.container}"
    padding: "20px 22px"
  chart-fill:
    backgroundColor: "{colors.terracotta-chart}"
    rounded: "{rounded.control}"
---

# Design System: David Salazar Portfolio

## Overview

**Creative North Star: "The Warm Page"**

A cream sheet with sand and peach laid on it in flat tonal steps, read the way a calm person talks: plain, first-person, unhurried. A hiring manager with a minute on a phone should find the structure at once and never be asked to admire the styling. Every surface is a tint of the same warm brown-orange family, so depth comes from stepping between four tones, not from shadows or lines.

Density is low. Sections are separated by space alone (72px on phones, 96px from 40rem), headings are large and tightly tracked, and body text is held to a reading measure. Decoration is absent; the only illustrations are the work's own screenshots and charts redrawn in the palette.

Visual rejections confirmed by the brief and the build: grain, gradients, glass, icon-card grids, loud shadows.

**Key Characteristics:**
- Four warm neutrals plus one peach accent; no cool colors, no gradients.
- Two grotesks: Cabinet Grotesk for voice, Switzer for reading.
- Zero box-shadows; depth is tonal.
- Two radius tiers: 10px for controls and media, 18px for containers.
- Motion is short and always gated for reduced motion and hover capability.

## Colors

Cream, sand, apricot and peach in graded steps, with one dark cocoa for all text.

### Primary
- **Peach Accent** (#f5bd9b): the one action color. Primary button fill, text selection. Deepens to Peach Accent Hover (#f0ae88) on hover.

### Secondary
- **Terracotta Chart** (#eaa781): data only. Bar fills and column-chart columns. Darker than the accent so marks read against the cream and sand.

### Neutral
- **Cream Background** (#f8efe3): page ground, sticky nav ground, chart tracks, panels inside bands.
- **Sand Surface** (#f1e1cd): containers and bands: tab bar, demo card, brief card, panels, flow nodes.
- **Apricot Step** (#f7d0b4): the selected state on sand: sliding tab pill, pressed demo segment, "bad" flow node.
- **Cocoa Ink** (#2e2218): all text, focus ring, skip link ground, text on the accent.
- **Umber Muted** (#6a5443): secondary text: meta, captions, labels, inactive tabs, dates.

### Named Rules
**The Tonal Step Rule.** Hierarchy between surfaces is cream, then sand, then apricot. A container inside a sand band flips to cream (`.band .panel`, `.band .demo`) instead of gaining a border or shadow.
**The Peach Is For Doing Rule.** Peach marks the thing to press; selected state uses apricot; data uses terracotta. Do not swap them.

## Typography

**Display Font:** Cabinet Grotesk 500 (fallback Switzer, system-ui)
**Body Font:** Switzer 400 and 500 (fallback system-ui)

**Character:** Cabinet Grotesk is slightly quirky and tight, used only at larger sizes and with negative tracking. Switzer is quiet and open so long reading stays easy. Only weight 500 is used as emphasis (no bold).

### Hierarchy
- **Case title** (500, clamp 2.5rem to 6rem, 1.0, -0.04em): case-study h1, the loudest thing on any page.
- **Display** (500, clamp 2.25rem to 3.25rem from 64rem; 1.5rem to 1.75rem below, 1.25, -0.03em): home h1, max 12em wide on desktop.
- **Headline** (500, 1.75rem to 2.25rem, 1.1, -0.03em): section h2 on home. On case pages at 64rem+ h2 drops to Title size and sits sticky in the left margin.
- **Title** (500, 1.25rem to 1.625rem, 1.2, -0.02em): h3, compact project titles, lede sentences, statements, fold summaries.
- **Body** (400, 1.0625rem to 1.1875rem, 1.55): everything else; paragraphs use `text-wrap: pretty`, headings `balance`.
- **Label** (400, 0.875rem to 0.9375rem): meta, captions, dates, dt terms, group captions, muted, in Switzer. Sentence case; not uppercase, not tracked.

### Named Rules
**The Two Voices Rule.** Cabinet Grotesk sets headings, ledes and the contact statement; Switzer sets the small bold-ish labels inside components (`.brief strong`, `.group`, change and glow-grow h3) even when they are h3s.

## Layout

One column on phones: `min(100% - 2.5rem, 35rem)`, 20px gutters. From 64rem the container becomes `min(100% - 4rem, 70rem)` and the page uses the width:
- Hero: intro text left, requirement demo (max 28rem) right, 5rem gap.
- Home work: Tetsu text left with its screenshots (31rem, sticky at top 6rem) right; the other projects in three columns, 3.5rem gap.
- About beside experience, 5rem gap; contact statement beside photo and lines.
- Case pages: title and lede left, brief card (27rem) right; each section has a 13rem sticky heading in a left margin and a content column capped at 44rem.
Between 40rem and 64rem the single column stays. Screenshot grids go 2-up on phones (third dropped) and 3 or 4-up from 40rem.

Rhythm: sections 4.5rem (phones) or 6rem (40rem+) top padding; bands add 6rem bottom and a 6rem top margin on home. Within sections: 2rem under h2 on home (1.5rem on case pages), 1.1rem paragraph gap, 1.75rem around figures. Touch targets are at least 2.75rem (44px) tall. The sticky nav is 4.25rem; anchors scroll with that plus 1rem of offset.

## Elevation & Depth

There are no shadows anywhere in the build. Depth is tonal layering: cream page, sand containers, apricot selection. Edges are made by the color change alone; there are no borders on containers.

### Named Rules
**The Flat Rule.** Nothing carries box-shadow, blur, gradient or border for depth. Press feedback is a scale, not a lift.

## Shapes

Soft but not pill-shaped. Controls, media, tab bar, charts and small nodes use 10px. Large containers (demo card, brief card, panels, about photo) use 18px. The sliding pill and the tab links inside the tab bar use 3px so they nest inside the 10px bar. Column chart columns round only the top corners (10px 10px 0 0). Focus ring is a 2px cocoa outline with 3px offset.

## Components

### Buttons
- **Shape:** 8px radius, 44px minimum height, 0 20px padding, weight 500.
- **Primary:** Peach fill, cocoa text, no border.
- **Hover:** deepens to the hover peach, only when a fine pointer with hover exists (140ms ease-out).
- **Active:** scale 0.97.
- **Text link:** underlined cocoa, 1px thickness growing to 2px on hover, offset 0.22em, 44px tall hit area; weight 500 for project links.

### Navigation (tab bar)
Inline sand bar, 4px padding, 8px radius, lowercase labels (intro, work, about, contact) in the small size. Inactive tabs are muted; the current tab is cocoa at weight 500. An apricot pill slides behind the current tab with a transform-only 240ms ease-in-out, sized by scaleX from the tab width, and spy-driven on home. Without JS the pill is hidden. The bar scrolls horizontally rather than wrapping on 320px screens.

### Requirement demo
A sand card (14px, 20px padding) with a segmented control of 44px-tall text buttons; the pressed one takes apricot fill. Panes occupy one grid cell so the card never changes height and cross-fade (200ms ease-out with a 4px rise). Without JS all panes show.

### Brief card (Problem / What I did / Result)
Sand 14px card on every case page, three paragraphs each opened by a muted small label. Beside the title on desktop, under the lede on phones.

### Bands, panels and folds
A band is a full-width sand section. A panel is a 14px card that is sand on cream and cream on a band. Long sections fold using details with the h2 as summary and a plus that rotates 45 degrees in 200ms.

### Charts
Bars: a cream 20px track with a terracotta fill, label, and a tabular-figure percent at right; stacked label above bar below 40rem. Column chart: terracotta columns with a value above the tall ones. Flow nodes: sand 8px chips joined by muted arrows; the failing node is apricot.

### Changes list and glow/grow
Capstone Before/After: a three-column grid (6.5rem label, before in muted, after on a cream 8px chip) from 40rem, stacked on phones with a hidden header row. Glow and grow: two plain bullet lists in two columns from 40rem.

### Motion
Reveals: 14px rise and fade, 320ms ease-out, staggered 50ms per item to a maximum of 250ms, content visible without script, items already in view skip animation. Easings: ease-out `cubic-bezier(0.23, 1, 0.32, 1)`, ease-in-out `cubic-bezier(0.77, 0, 0.175, 1)`. All transitions are inside `prefers-reduced-motion: no-preference`, or are color/transform state changes of 140 to 200ms; hover styles are gated on `(hover: hover) and (pointer: fine)`.

## Do's and Don'ts

### Do:
- **Do** set all text in cocoa (#2e2218) or muted umber (#6a5443); never pure black or white.
- **Do** step surfaces cream, sand, apricot; flip to cream for a card inside a sand band.
- **Do** keep controls at 8px and containers at 14px.
- **Do** keep tap targets at least 44px tall.
- **Do** use weight 500 for emphasis and Cabinet Grotesk only for headings, ledes and statements.
- **Do** gate every animation behind reduced motion and every hover behind hover capability.
- **Do** write labels and tabs in sentence or lower case.

### Don't:
- **Don't** add shadows, gradients, glass, grain or icon-card grids.
- **Don't** use peach for data or terracotta for buttons.
- **Don't** separate sections with rules or borders; use space.
- **Don't** use bold above 500, and don't track out small text.
- **Don't** let any element exceed the viewport: titles and values use `overflow-wrap: anywhere`.
