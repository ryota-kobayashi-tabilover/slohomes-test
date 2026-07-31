# slo — Design System

**"A Slightly Open slow Space"**

slo (スロー) is a semi-public membership lounge brand, launching as **slo nihonbashi** in Tokyo. The identity was designed by **staple studio** (2026.03.31). This design system is a working copy of that visual identity, translated into fonts, tokens, components and HTML previews so designers and engineers can build in-brand interfaces and applications.

---

## 1 · What slo is

slo is a membership lounge — an intentionally *semi-public* space for social exchange. Somewhere between a public café (too loud, too anonymous) and a closed club (too stagnant). The name is a deliberate fragment of **slow** — a missing "w" — signalling that something is withheld, curated, considered. A place that is *slightly open*.

Three design concepts structure the brand:

1. **slo** — the missing "w" in "slow"; reserve, quietness, not-everything-on-display.
2. **SLO NIHONBASHI** — rooted in Nihonbashi, Tokyo; the brand always appears with its location.
3. **a / b · public / private** — two modes. Bright outward-facing events ("a. public") and quiet members-only moments ("b. private") share one vocabulary.

### Keywords from the brief (page 5)
*Semi-public / Another place to belong / Neutral / Playful / Vitamin / Whitespace / Stimulating yet calm / Living space / Expansion / Ripple*

### Products / surfaces in scope

slo's surface area (as shown in the VI guide) is mainly **spatial & social**, not software-heavy. The system therefore optimises for print, signage, and social. The UI kits here recreate the digital surfaces we can infer from the brief:

| Surface | Source | UI kit folder |
|---|---|---|
| Instagram feed / event posts | Guide p.27–28 | `ui_kits/instagram/` |
| Member-facing web landing page | Inferred (product is pre-launch) | `ui_kits/website/` |
| Membership app (home, events, bookings) | Inferred | `ui_kits/app/` |

The app & website are **not** in the VI guide — they are plausible, in-brand extensions. See each UI kit's README for the source-of-truth / invention split.

---

## 2 · Sources

All source material was provided as file uploads (no Figma or codebase attached):

- `uploads/slo_vi_0331.pdf` — **slo Visual Identity**, staple studio, 2026.03.31 (29 pages). The single source of truth for the brand. Rendered pages are in `pdf_pages/` and cropped references are in `assets/reference/`.
- `uploads/PTSans.ttc` — PT Sans font family (used: **PT Sans Narrow Bold** for the logotype).
- `uploads/NotoSansJP-Regular.ttf` / `uploads/NotoSansJP-SemiBold.ttf` — Japanese body face.
- `uploads/38184073029.ttf` — **Neue Haas Grotesk Text Pro Bold** (Latin body, Bold).
- `uploads/31862445252.ttf` — **Neue Haas Grotesk Text Pro Regular** (Latin body, Regular).

Two Google Drive links are referenced in the guide (we do not have access):
- Font guide: `https://drive.google.com/drive/folders/1il5OfQ9xjb8NrYv85mUPwotIX6n2pkXd`
- Instagram format data: `https://drive.google.com/drive/folders/198GhTc6tB75Yo18OVIzXM3M-jB3AztAO`

---

## 3 · Index of this folder

| Path | What it is |
|---|---|
| `README.md` | This file — brand, foundations, and index. |
| `SKILL.md` | Agent-usable skill wrapper. |
| `colors_and_type.css` | **The foundation tokens file.** CSS variables for colors, type families, size scale, spacing, radii, shadows, motion. Import this anywhere. |
| `fonts/` | `.ttf` files + `fonts.css` with all `@font-face` declarations. |
| `assets/` | Logos (SVG) + reference images cropped from the VI PDF. |
| `pdf_pages/` | All 29 VI guide pages rendered to PNG, for reference only. |
| `preview/` | HTML cards shown in the Design System tab. |
| `ui_kits/instagram/` | IG feed / grid / event-post components. Directly from guide p.27-28. |
| `ui_kits/website/` | Plausible members landing page. **Inferred — not in the guide.** |
| `ui_kits/app/` | Plausible membership app. **Inferred — not in the guide.** |

---

## 4 · Content fundamentals

The VI guide speaks in two registers in parallel — **English** (marketing, pull-quote, mood) and **Japanese** (explanatory, practical). Both should be considered first-class; slo is bilingual.

### Voice
- **Calm, declarative, slightly literary.** Full sentences, not hype fragments. The brief reads like a manifesto, not ad copy: *"Through social interaction, we encounter unfamiliar stimuli and gain new insights."*
- **"We"** (collective, inclusive). Rarely "you". Never first-person-singular "I".
- **Evocative nouns over adjectives**: *noise / signal / ripple / whitespace / rhythm.* Writers reach for sensory words before descriptive ones.
- No exclamation marks. No hype words ("amazing", "incredible"). No em-dash clauses stacked for drama.

### Tone
- Quiet confidence. The brand assumes the reader is capable of nuance.
- Slightly cerebral — happy to talk about *redefining* and *disrupting rhythms*.
- **Playful only in form, never in voice.** The playful bits are visual (the stickers, the yellow), not textual.

### Casing & typography
- **Sentence case** everywhere in running copy — including headlines. *"A place that welcomes anyone with openness"*.
- The **brand name is always lowercase**: `slo`, `slo nihonbashi`, `lounge slo nihonbashi`. Never `Slo`, never `SLO` except when explicitly set as a spatial logotype (pg.7).
- Section titles in the guide are **Title Case** with spaces: *Mood / Image board*, *Color code / Paper*.
- Lists use numbered prefixes (`1.`, `2.`) rather than bullets. Sub-items use alphabetics (`a.`, `b.`) as seen on page 8.
- Slashes separate peer concepts: `a.public / b.private`, `Mood / Image board`, `Color code / Paper`.

### Emoji & symbols
- **No emoji.** Not in the guide, not on brand. Substitute with a color swatch, a sticker motif, or a numbered index.
- **Slashes** (`/`) are a recurring brand glyph — both as a typographic mark in slogans ("slow / stimulating yet calm") and as a visual motif in the sticker system (diagonal strokes).
- Numeric addresses and dates use clean prefixes (`03.31`, `2026.03.31`) with periods, not slashes.

### Example copy lifted from the guide
> *A Slightly Open slow Space* — brand promise.
> *A place that welcomes anyone with openness, yet still provides a genuine sense of security.* — member-facing tagline.
> *A place where conversation begins naturally, and new ideas quietly emerge.* — from the typography specimen.
> *この空間では、本をReadしたり、少しWork をしたり、ゆっくりとした時間を過ごすことができます。* — JP sample mixing English verbs inside Japanese prose (intentional).

### Mixed-language runs
- Latin words inside Japanese sentences are **capitalised and kept in Latin** (`本をReadしたり、少しWork をしたり`). They are not italicised and not bracketed.
- The type system handles this with `font-feature-settings: 'palt' 1` and matched x-heights between Neue Haas Grotesk and Noto Sans JP (the guide specifies Neue Haas at `-2%` tracking, `105%` size to harmonise).

---

## 5 · Visual foundations

### 5.1 · Color
One bright accent + four paper-tone base colors + ink. That's the whole palette.

| Token | Hex | Role |
|---|---|---|
| `--slo-yellow` | `#fff000` | **Vitamin Yellow** — logo, stickers, accent highlights, the ONE color that "pops". |
| `--slo-pale-blue` | `#5b6e75` | Pale Blue — calm base, daytime scenes. |
| `--slo-moss-green` | `#323b29` | Moss Green — deep, grounded, evening scenes. |
| `--slo-gray` | `#717071` | Gray 70 — neutral base. |
| `--slo-soil-brown` | `#9c8a78` | Soil Brown — warm earthen base. |
| `--slo-ink` | `#111111` | Text, primary logotype on paper. |
| `--slo-paper` | `#f4f2ec` | Default page — warm off-white. |

**Rules**:
- Use **exactly one base color** as the dominant scene background (full-bleed). Don't mix bases in the same composition.
- Vitamin Yellow is the **only** accent. Use it for logotype when the base is dark enough (blue / moss / gray / brown); use ink-black logotype on paper/yellow.
- The guide spec includes paper choice (`NT ラシャ`) — which signals that print output is considered from day one. Digital work should feel paper-ish too (muted, not screeny).
- No gradients. No shadows-as-color. No tinted glass. Color is flat.

### 5.2 · Typography
Four families work together:

| Family | File | Role |
|---|---|---|
| **PT Sans Narrow Bold** | `PTSans-NarrowBold.ttf` | Logotype, display type, posters. High-impact, tall-narrow. |
| **Neue Haas Grotesk Text Pro** | Regular + Bold | Latin body & headlines. The workhorse. |
| **Noto Sans JP** | Regular + SemiBold | Japanese body. Pairs with Neue Haas Grotesk. |
| *(Latin fallback)* | — | Helvetica / system-ui as last resort. |

**Mixing rule (from guide p.26):** in bilingual runs, set Neue Haas Grotesk at **-2% tracking** and **105% size** to match Noto Sans JP's optical weight.

Type is never:
- Italicised (no italic faces in the system).
- All-caps except for very small labels (eyebrows, navigation meta).
- Stretched or condensed beyond what PT Sans Narrow already provides.
- Given a stroke / outline / drop shadow.

### 5.3 · Layout & composition

- **Grid-forward but not a strict grid.** The guide uses a generous 4-column feel with each page built around one hero asset (logo, swatch, photo grid) floating inside whitespace.
- **Massive whitespace.** 50%+ of every page is empty. In product design, mimic this by choosing generous gutters (`--gutter: clamp(16px, 4vw, 64px)`) and letting hero elements breathe.
- **Top-left navigation meta**: every VI page has `staple studio · slo Visual Identity · [Section] · 2026.03.31` across the top edge. This "running header" pattern is a signature — use it in slide decks and long-form layouts.
- **Page numbers bottom-right** in a small weight.
- **Left-aligned indices** (`1. Primary / 2. Secondary …`) with the active item bolded.

### 5.4 · Imagery
The mood board tells us exactly what imagery feels like:
- **Muted, natural color**. Warm woods, moss greens, steel blues, terracotta reds, yellow accents.
- **Interior photography**: people in-space. Always people-in-context, never product-on-white.
- **Mid-century & modernist furniture**: Gio Ponti / Bauhaus shapes. Curved armchairs, low sofas, paper lanterns.
- **Art objects mid-frame** — a framed red canvas, a paper lantern, a sculpture — communicating "curated".
- **Texture** matters: stucco walls, linen upholstery, raw wood, paper posters. Nothing glossy.
- **Print ephemera** is welcome as photographic subject — event posters, stickers on hands, a wall of flyers.

For the brand's own content: IG grid (p.27) uses **6×6 tiles alternating between hand-photographed interiors and yellow-on-paper tile stacks**. The yellow tiles are printed logos photographed on a surface, not digital flats.

### 5.5 · Backgrounds
- **Full-bleed flat base color** is the primary treatment. No gradients.
- **Paper texture** may be implied through the chosen stock (`NT ラシャ`) but we do NOT overlay fake paper-texture noise on digital surfaces. Keep it flat.
- **Sticker motif**: the "N" sticker (p.29) — two brushstroke strokes + diagonal, with "slo" stamped on top — is the one ornament the brand has. It can be used tiled, tilted, singular, or as a loading state. Never photographed.

### 5.6 · Motion
- **Calm and paper-like.** Short durations (120–480ms). `ease-out` and `ease-in-out`. **No bouncy easing.** No over-shoot.
- **Fades and tiny translates** (≤8px) only. No scaling > 1.04, no rotation unless it's a sticker.
- **Hover**: drop opacity to 0.7 or darken by 5%. Never a color change that re-brands.
- **Press**: no shrink. A tiny opacity dip (0.85) is enough.
- A **ripple** motion from the keyword list ("Ripple") can be used sparingly on focus states or accent interactions — a radial 300ms wave at the yellow color.

### 5.7 · Borders, corners & shadows
- **Radii**: mostly 0. A 2–8px radius is allowed on UI chrome (inputs, cards). The brand sticker itself has fully rounded stroke-ends but it's a single custom object, not a pattern to repeat.
- **Borders**: 1px hairline in `rgba(17,17,17,.14)`. Never thicker. Never colored.
- **Shadows**: virtually none. `--shadow-sheet` for floating surfaces is already close to invisible.
- **No inner glow / inner shadow / colored glow** in any direction.
- **No left-border-accent cards.** The brand solves emphasis with whitespace and hierarchy, not colored sidebars.

### 5.8 · Transparency & blur
- **Transparency** is used on ink black (`--slo-ink-60`, `--slo-ink-20`) for text hierarchy; never on base colors (moss / yellow / brown stay at 100%).
- **Backdrop blur** is never used. slo does not have a "glassy" aesthetic. If you need a sticky overlay, use a solid paper panel with a hairline rule.

### 5.9 · Cards
When a card is truly necessary:
- 1px hairline border OR the `--shadow-sheet` elevation, **not both**.
- 0–8px radius.
- Ink-black text on paper (or paper text on a base color).
- No gradient. No glow. No accent stripe. No icon-in-a-circle.
- Think: index card pinned on a cork wall, not "Material 3".

### 5.10 · Fixed elements / overlays
The brand has almost no fixed chrome in the guide. When building UIs, keep sticky headers **minimal**: one-line running header matching the guide (`slo · Section · YY.MM.DD`), no drop shadow, separated from the body with a hairline.

---

## 6 · Iconography

> **The guide does not define an icon system.** What follows is an extension.

### What the brief gives us
- **The "N" sticker** is effectively the one official pictogram (see `assets/brand-sticker-N.svg`). It doubles as a wordmark and a social-media mascot.
- **Slash characters** `/` are used as inline separators and as a visual motif.
- **Numbered indices** (`1.`, `2.`, `3.`) are used instead of bullet icons.
- **No emoji anywhere.**

### Our extension for UI work
For general UI icons (settings, calendar, map pin, etc.) the guide is silent, so we recommend:

- **Primary icon set: [Phosphor Icons — Regular (1.5px stroke)](https://phosphoricons.com/).** Its narrow, tall, line-weight feel matches PT Sans Narrow and Neue Haas Grotesk much better than Material / Heroicons. Load from CDN: `https://unpkg.com/@phosphor-icons/web@2.1.1/src/regular/style.css`. **Flagged: this is a substitution we chose — the brand has no icon set of record.**
- **Stroke width** fixed at 1.5px across all icons.
- **Size scale**: 16 / 20 / 24 px. 24px is the most common in-UI size.
- **Color**: icons inherit `currentColor`. On paper they are ink; on a base-color scene they are paper.
- **Fills are reserved for the yellow accent** — a filled icon = active/selected state, filled yellow.
- **Never combine two icon sets.** Don't mix Phosphor with Material in the same screen.

See `preview/card-iconography.html` and the UI kits for live samples.

---

## 7 · Substitutions & caveats

- **Font licensing**: PT Sans, Noto Sans JP and Neue Haas Grotesk ship with their respective licenses. PT Sans + Noto Sans JP are OFL-licensed and free. Neue Haas Grotesk Text Pro is a **commercial** Linotype/Monotype face; the project already provides the files. Confirm with the brand owner before using in commercial output.
- **Icons**: Phosphor Regular is our substitution (see §6). If the brand introduces a custom set later, swap it here.
- **Logo SVG**: `assets/logo-slo.svg` references PT Sans Narrow Bold via `@font-face`. For portable contexts where the font can't be loaded, use the rasterised version at `assets/reference/logo-primary.png` or have the foundation font available.
- **Neue Haas Grotesk Text Pro** — the two TTF files uploaded were anonymously-named (`38184073029.ttf` / `31862445252.ttf`); we verified them against their internal name tables and re-exported as `NeueHaasGroteskTextPro-{Bold,Regular}.ttf`.
- **App & website UI kits** are extrapolations, not source-of-truth. They follow the tokens strictly but invent flows. Treat as starting points.

---

## 8 · How to use this system

```css
/* 1. Import once */
@import url('./colors_and_type.css');

/* 2. Use semantic tokens */
.scene {
  background: var(--slo-moss-green);
  color: var(--fg-on-dark);
  padding: var(--s-16) var(--gutter);
}
.scene h1 { 
  /* ready-made */ 
}
```

Or use the pre-built type utilities: `.display-1`, `.h1–.h4`, `.body`, `.body-sm`, `.eyebrow`, `.jp-body`, `.caption`.

Last updated 2026.04.19 — this is a v1. Expect iteration once the production site & app exist.
