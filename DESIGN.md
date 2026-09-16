---
version: alpha
name: BluTrace-design
description: >-
  A flat, hairline-bordered B2B engineering site. White canvas with a light gray-blue
  banded rhythm between sections, one saturated brand blue for every interactive element,
  and a sparing copper accent reserved for small non-interactive marks (bullets, dashes,
  a logo dot). Inter carries all headings and body copy with tight negative tracking on
  headings; IBM Plex Mono is used exclusively for eyebrows, labels, tags and numeric
  metadata, always uppercase with positive tracking when used as a label. Hierarchy comes
  from 1px hairline borders and background banding, not shadows or scale - the whole page
  has exactly two very soft shadows, both reserved for "floating" elements (the hero photo
  and the mobile nav popover).

colors:
  primary: "#0E4EA3"
  primary-hover: "#0A3C80"
  on-primary: "#FFFFFF"
  accent: "#C0843C"
  ink: "#1A2230"
  ink-soft: "#3C4656"
  muted: "#5C6675"
  faint: "#8A93A2"
  canvas: "#FFFFFF"
  surface-1: "#F5F7FA"
  surface-accent: "#EAF1FB"
  hairline: "#E3E8EF"
  hairline-strong: "#CDD5E0"
  navy: "#0F1B2D"
  footer-bg: "#0C1726"
  footer-ink: "#AEBCCD"
  footer-ink-soft: "#92A1B5"
  footer-muted: "#8FA0B5"
  footer-heading: "#6F8095"
  footer-strong: "#C6D2E2"
  footer-accent: "#6CA6F0"

typography:
  display-lg:
    fontFamily: Inter
    fontSize: 3.1rem
    fontWeight: 700
    lineHeight: 1.18
    letterSpacing: -0.018em
  headline:
    fontFamily: Inter
    fontSize: 2.3rem
    fontWeight: 700
    lineHeight: 1.18
    letterSpacing: -0.018em
  headline-sm:
    fontFamily: Inter
    fontSize: 1.2rem
    fontWeight: 700
    lineHeight: 1.18
    letterSpacing: -0.018em
  body-lg:
    fontFamily: Inter
    fontSize: 1.12rem
    fontWeight: 400
    lineHeight: 1.6
    letterSpacing: 0px
  body:
    fontFamily: Inter
    fontSize: 1rem
    fontWeight: 400
    lineHeight: 1.6
    letterSpacing: 0px
  body-sm:
    fontFamily: Inter
    fontSize: 0.92rem
    fontWeight: 500
    lineHeight: 1.5
    letterSpacing: 0px
  button-label:
    fontFamily: Inter
    fontSize: 0.92rem
    fontWeight: 600
    lineHeight: 1
    letterSpacing: 0px
  label-eyebrow:
    fontFamily: IBM Plex Mono
    fontSize: 0.72rem
    fontWeight: 600
    lineHeight: 1
    letterSpacing: 0.14em
  label-caps:
    fontFamily: IBM Plex Mono
    fontSize: 0.66rem
    fontWeight: 600
    lineHeight: 1
    letterSpacing: 0.12em
  data-mono:
    fontFamily: IBM Plex Mono
    fontSize: 0.8rem
    fontWeight: 600
    lineHeight: 1.2
    letterSpacing: 0.02em

rounded:
  sm: 5px
  md: 6px
  lg: 8px
  full: 9999px

spacing:
  xs: 8px
  sm: 14px
  md: 20px
  lg: 32px
  xl: 84px
  gutter: 32px
  maxw: 1200px

components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    typography: "{typography.button-label}"
    rounded: "{rounded.sm}"
    padding: 12px 22px
  button-primary-hover:
    backgroundColor: "{colors.primary-hover}"
    textColor: "{colors.on-primary}"
  button-ghost:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.ink}"
    typography: "{typography.button-label}"
    rounded: "{rounded.sm}"
    padding: 12px 22px
  button-ghost-hover:
    textColor: "{colors.primary}"
  button-light:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.navy}"
    typography: "{typography.button-label}"
    rounded: "{rounded.sm}"
    padding: 12px 22px
  card:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.ink}"
    rounded: "{rounded.md}"
    padding: 34px 32px
  icon-tile:
    backgroundColor: "{colors.surface-accent}"
    rounded: "{rounded.md}"
    width: 44px
    height: 44px
  nav-header:
    backgroundColor: "{colors.canvas}"
    height: 68px
  section-alt:
    backgroundColor: "{colors.surface-1}"
    textColor: "{colors.ink}"
  footer:
    backgroundColor: "{colors.footer-bg}"
    textColor: "{colors.footer-ink}"
    padding: 52px 0 36px
---

## Overview

BluTrace is a hardware engineering firm's marketing site. It reads as conventional,
authoritative, B2B-serious - closer to an industrial spec sheet than a startup landing
page. The canvas is `{colors.canvas}` (#ffffff) with alternating `{colors.surface-1}`
(#f5f7fa) bands giving section rhythm without adding a border between every section.

**Key Characteristics:**
- One accent hue, `{colors.primary}` (#0e4ea3), carries every interactive and brand
  element: links, primary buttons, icon strokes, the "Blu" in the wordmark, active states.
- `{colors.accent}` (#c0843c, copper) is used sparingly and only on non-interactive marks:
  the eyebrow dash, list-item bullets, and the logo's center dot. It never appears on a
  clickable element.
- Hierarchy is carried by hairline borders and surface banding, not shadow or elevation.
  The entire page has exactly two shadows, both reserved for elements that visually float
  above the flow (hero photo, mobile nav popover).
- Two families: Inter for everything a visitor reads (headings, body, buttons, nav), IBM
  Plex Mono for everything a visitor scans (eyebrows, tags, labels, numeric metadata).
  Headings carry tight negative tracking (-0.018em); mono labels are uppercase with
  positive tracking (+0.12em to +0.14em). The two never swap roles.
- Corner radius is nearly uniform: `{rounded.md}` (6px) on every card, tile, and icon chip.
  Buttons alone get the slightly tighter `{rounded.sm}` (5px). Nothing on the page is fully
  rounded/pill-shaped.
- Two distinct near-black surfaces exist on purpose: `{colors.navy}` (#0f1b2d) for the CTA
  band and header logo mark, and a separate, slightly darker `{colors.footer-bg}` (#0c1726)
  for the footer only. Treat them as two tokens, not one - see Known Gaps.

## Colors

> Source: `Bluventra/site/index.html`, the `:root` custom-property block and the footer's
> hardcoded hex values (the footer uses its own darker ladder, not `:root` tokens).

- **`{colors.primary}` (#0e4ea3)** - links, primary button background, icon strokes inside
  the light icon tiles, the accent letters in "BluTrace", the hero's accent word span, the
  top border rule on each process step.
- **`{colors.primary-hover}` (#0a3c80)** - hover state for `button-primary` only.
- **`{colors.on-primary}` (#ffffff)** - text/icon color on top of `{colors.primary}` and
  `{colors.navy}` surfaces.
- **`{colors.accent}` (#c0843c, copper)** - eyebrow dash, list bullets, the small center
  dot in the logo mark. Sparing by design; do not put it on a button, link, or large area.
- **`{colors.ink}` (#1a2230)** - primary heading and body text color on light surfaces.
- **`{colors.ink-soft}` (#3c4656)** - secondary paragraph text (hero subhead, about copy)
  and nav link color.
- **`{colors.muted}` (#5c6675)** - tertiary/supporting text: section intros, step
  descriptions, why-item descriptions.
- **`{colors.faint}` (#8a93a2)** - the quietest text: capability-strip label, hero-figure
  caption, meta value labels, nav-toggle background border companion.
- **`{colors.canvas}` (#ffffff)** - page background, card/tile background, header background.
- **`{colors.surface-1}` (#f5f7fa)** - banded section backgrounds (industries, engagement,
  about) that alternate with `{colors.canvas}` for rhythm.
- **`{colors.surface-accent}` (#eaf1fb)** - background for the small icon chips on cards,
  industry tiles, and why-items; also the hover background for `button-light`.
- **`{colors.hairline}` (#e3e8ef)** - the default 1px border: card borders, section
  dividers, header bottom border, band top/bottom borders.
- **`{colors.hairline-strong}` (#cdd5e0)** - a slightly stronger 1px border used only on
  the ghost button and the nav-toggle square.
- **`{colors.navy}` (#0f1b2d)** - the CTA band background and the header/nav logo mark fill.
  Use this for any *new* dark section.
- **`{colors.footer-bg}` (#0c1726)** - footer background only. Deliberately darker than
  `{colors.navy}`; do not reuse `{colors.navy}` in the footer or `{colors.footer-bg}`
  elsewhere.
- **`{colors.footer-ink}` (#aebccd)**, **`{colors.footer-ink-soft}` (#92a1b5)**,
  **`{colors.footer-muted}` (#8fa0b5)**, **`{colors.footer-heading}` (#6f8095)**,
  **`{colors.footer-strong}` (#c6d2e2)** - the footer's own text ladder, from body links
  down to the quietest legal copy. Do not mix these with the light-surface ink ladder above.
- **`{colors.footer-accent}` (#6ca6f0)** - the brighter blue used only on dark surfaces
  (footer brand mark, footer mail icon, the CTA band's eyebrow) where the standard
  `{colors.primary}` would not have enough contrast against navy/footer-bg.

## Typography

Inter (weights 400/500/600/700) is loaded from Google Fonts for every heading, paragraph,
nav link, and button. IBM Plex Mono (weights 500/600) is loaded alongside it for eyebrows,
tags, labels, and numeric/metadata text. No italic weights are loaded for either family;
don't introduce italics. All headings (h1-h4) share `line-height: 1.18` and
`letter-spacing: -0.018em` from one combined rule - keep new heading levels on that same
line-height/tracking pair rather than inventing a third value.

| Token | Family | Size | Weight | Line height | Tracking | Used for |
|---|---|---|---|---|---|---|
| `display-lg` | Inter | 3.1rem (clamps down to 2.1rem on narrow viewports) | 700 | 1.18 | -0.018em | hero H1 |
| `headline` | Inter | 2.3rem (clamps down to 1.7rem) | 700 | 1.18 | -0.018em | section H2 |
| `headline-sm` | Inter | 1.2rem | 700 | 1.18 | -0.018em | card H3, why-item/step/engagement H4 |
| `body-lg` | Inter | 1.12rem | 400 | 1.6 | 0 | hero subhead, section intros, CTA intro |
| `body` | Inter | 1rem | 400 | 1.6 | 0 | default paragraph text |
| `body-sm` | Inter | 0.92rem | 500 | 1.5 | 0 | nav links, card/list body copy |
| `button-label` | Inter | 0.92rem | 600 | 1 | 0 | all button variants |
| `label-eyebrow` | IBM Plex Mono | 0.72rem | 600 | 1 | +0.14em | section eyebrows (uppercase) |
| `label-caps` | IBM Plex Mono | 0.66rem | 600 | 1 | +0.12em | capstrip label, engagement tags, footer column headings (uppercase) |
| `data-mono` | IBM Plex Mono | 0.66rem-0.95rem, use 0.8rem as default | 400-600 | 1.2 | 0 to +0.1em | utility bar text, hero stat values, card/step index numbers (weight and tracking scale slightly with emphasis - heavier/tighter for a hero stat, lighter/looser for a plain index number, but always this family) |

## Layout

Content sits in a `{spacing.maxw}` (1200px) `.wrap` container with `{spacing.gutter}`
(32px) side padding. Sections use `{spacing.xl}` (84px) of vertical padding on desktop,
dropping to 60px at the mobile breakpoint - see Responsive Behavior. Section intros
(`section-head`) cap their line length at 680px regardless of the wider container.

Grids are deliberately not uniform - pick the pattern that matches what you're building,
don't blend them:
- **Services cards**: a 2-column grid with a 1px gap filled by `{colors.hairline}`, so the
  gap itself reads as a border between cards (the grid container, not the cards, has the
  border and background color).
- **Industries / Why-us / Engagement**: real gaps (`{spacing.sm}` to `{spacing.md}`,
  14-20px) between independently bordered, independently rounded tiles.
- **Process steps**: a 5-column row, each step marked by a 2px top border in
  `{colors.primary}` rather than a card container.

## Elevation & Depth

This is a flat system. Hierarchy comes from `{colors.hairline}` borders and surface
banding (`{colors.canvas}` vs `{colors.surface-1}`), not shadow. There are exactly two
box-shadows on the whole site, both long, soft, and low-opacity, reserved for elements
that visually float above the page flow rather than sit in it:

- Hero photo: `0 20px 50px -30px rgba(15,27,45,.4)`
- Mobile nav dropdown popover: `0 20px 40px -20px rgba(15,27,45,.4)`

Do not add shadow to cards, buttons, or icon tiles - their separation comes entirely from
the `{colors.hairline}` border plus, where relevant, a background change.

## Shapes

`{rounded.md}` (6px) is the dominant radius - used on cards, industry/why-item tiles, icon
chips, and the hero photo frame. `{rounded.sm}` (5px) is reserved for buttons only, giving
them a very slightly tighter corner than the containers around them. `{rounded.lg}` (8px)
appears exactly once, on the mobile nav dropdown. `{rounded.full}` is used for the small
5px bullet dots (list markers, capability-strip dots) - visually a circle on a fixed-size
square. Borders are always 1px (`{colors.hairline}`) except the button border (1.5px,
transparent on primary/light, `{colors.hairline-strong}` on ghost) and the nav-toggle
square (1px, `{colors.hairline-strong}`).

## Components

### Buttons

**`button-primary`** - the single highest-emphasis action per view (hero CTA, nav CTA, CTA
band). Background `{colors.primary}`, text `{colors.on-primary}`, type
`{typography.button-label}`, padding 12px 22px, rounded `{rounded.sm}`. Hover swaps
background to `{colors.primary-hover}` via `button-primary-hover` - no other property
changes on hover.

**`button-ghost`** - secondary action next to a primary button (e.g. "See our
capabilities"). Background `{colors.canvas}`, text `{colors.ink}`, border
`{colors.hairline-strong}`. Hover (`button-ghost-hover`) turns both the border and the text
`{colors.primary}` - background stays flat, no fill-in.

**`button-light`** - the light-on-dark variant, used only inside the navy CTA band.
Background `{colors.canvas}`, text `{colors.navy}`. Hover background becomes
`{colors.surface-accent}`.

### Cards & Containers

**`card`** - services grid item. Background `{colors.canvas}`, text `{colors.ink}`, rounded
`{rounded.md}`, padding 34px 32px. Contains an `icon-tile`, a small mono index number
(`data-mono`, top-right), a `headline-sm` title, and a bulleted `body-sm` list with a
copper `{colors.accent}` dot marker.

**`icon-tile`** - the 44px square icon chip on cards (38-44px depending on section).
Background `{colors.surface-accent}`, rounded `{rounded.md}`, icon stroke
`{colors.primary}` at 1.7px stroke-width, no fill.

**`section-alt`** - the banded section background (industries, engagement, about).
Background `{colors.surface-1}`, text `{colors.ink}`, always bordered top/bottom with
`{colors.hairline}`. Alternates with plain `{colors.canvas}` sections.

**`footer`** - background `{colors.footer-bg}`, base text `{colors.footer-ink}`, padding
52px 0 36px. Internally it has its own text ladder (`footer-ink-soft`, `footer-muted`,
`footer-heading`, `footer-strong`) and its own brighter accent (`footer-accent`) for links
and the wordmark - see Colors.

### Inputs

No input fields exist in the current source (contact is `mailto:` links only - see Known
Gaps). If a form is added, base inputs on `{colors.canvas}` background,
`{colors.hairline}` border, `{colors.ink}` text, `{rounded.sm}` corners (matching
buttons), and a `{colors.primary}` focus ring - do not invent a new radius or border color
for form fields.

### Navigation

Two-tier header: a slim dark utility bar (`{colors.navy}` background, `label-caps`-sized
mono text, hidden below the mobile breakpoint) above a sticky white `nav-header`
(`{colors.canvas}`, `{colors.hairline}` bottom border, ~68px tall). Nav links use
`body-sm`/`{colors.ink-soft}`, hover to `{colors.primary}`. Below 760px, links collapse
into a fixed-position dropdown card (`{rounded.lg}`, the one 8px radius on the page) toggled
by a 3-line hamburger button.

## Do's and Don'ts

### Do
- Use `{colors.primary}` for links, primary CTA backgrounds, active icon strokes, and the
  accent letters in the wordmark - it is the only saturated hue that carries interactive
  meaning on this site.
- Reserve `{colors.accent}` (copper) for small, non-interactive marks: eyebrow dashes, list
  bullets, a logo dot. Never place it on a button or link.
- Separate cards and sections with 1px `{colors.hairline}` borders, not shadow.
- Alternate new sections between `{colors.canvas}` and `{colors.surface-1}` to build rhythm
  without a border on every seam.
- Use IBM Plex Mono only for eyebrows, tags, labels, and numeric/metadata text - always
  uppercase with positive tracking when it is a label.
- Use `{rounded.md}` (6px) for any new card, tile, or icon chip; keep `{rounded.sm}` (5px)
  for buttons only.
- Put new dark sections on `{colors.navy}`; keep `{colors.footer-bg}` exclusive to the
  footer.
- Keep the two-shadow budget: only a floating photo or a popover earns a shadow.

### Don't
- Don't introduce a third hue. Blue and copper are the only two colors in the system,
  besides the ink/surface neutrals.
- Don't add drop shadows to cards, buttons, or icon tiles - this is a flat, hairline system.
- Don't use pill/fully-rounded buttons; buttons are `{rounded.sm}` rectangles, not pills.
- Don't set body copy in IBM Plex Mono, or headings/buttons in anything but Inter.
- Don't collapse `{colors.navy}` and `{colors.footer-bg}` into one value, and don't add a
  third near-black - the two-token split is intentional (see Known Gaps).
- Don't exceed `{spacing.gutter}` (32px) side padding on a new full-bleed section; keep
  content width at or under `{spacing.maxw}` (1200px).
- Don't blend the services grid's hairline-gap trick with the tile-and-gap pattern used
  elsewhere - pick one per component.

## Responsive Behavior

| Name | Width | Key changes |
|---|---|---|
| Desktop | >980px | default: 2-col service cards, 3-col industries, 3-col engagement, 2-col why-us, 5-col process steps, 4-col footer |
| Tablet | ≤980px | hero grid drops to 1 column (photo moves above copy), industries grid to 2-col, engagement to 1-col, process steps to 2-col, footer to 2-col |
| Mobile | ≤760px | nav collapses into a fixed dropdown card behind a hamburger toggle, utility bar hides entirely, all grids (cards, industries, why-us, steps, footer) go to 1 column, `display-lg`/`headline` scale down via their `clamp()` minimums, section vertical padding drops from `{spacing.xl}` (84px) to 60px |

Touch targets: nav links and buttons use ~12px vertical padding, giving roughly a 44px tap
height once line-height is included - keep new mobile tap targets at or above that.
Images: the hero photo is fixed at a 4:3 aspect ratio with `object-fit: cover`; keep new
photography on the same ratio unless a section has a clear reason to differ.

## Known Gaps

- No dark-mode / `prefers-color-scheme` handling exists in the source; `theme-color` meta
  is fixed white.
- No form/input, validation, or error states are visible (contact is `mailto:` only) - see
  Components > Inputs for the extrapolation rule if a form gets added.
- No loading, disabled, or empty states are visible anywhere on the page.
- `--blue-bri` (#1763c7) is declared in the source `:root` block but is not referenced by
  any rule - treat it as reserved/dead, not a live token, unless a future change
  reactivates it for something like a button active/pressed state.
- The footer's `{colors.footer-bg}` (#0c1726) and the site's `{colors.navy}` (#0f1b2d) are
  two distinct near-black values in the live source with no documented reason for the
  difference. This file preserves that as two tokens rather than merging them, since
  merging would be a visual change nobody asked for - flag it to the user before "fixing" it.
