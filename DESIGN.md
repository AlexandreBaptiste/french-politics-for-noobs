---
name: La politique Française pour les nuls
description: Non-partisan civic education reference for French politics — institutions, parties, reforms, and vocabulary.
colors:
  # RF Blue — structural surfaces
  rf-blue-950: "oklch(22% 0.15 258)"
  rf-blue-900: "oklch(29% 0.18 258)"
  rf-blue-800: "oklch(39% 0.20 258)"
  # RF Red — primary accent
  rf-red: "oklch(57% 0.215 30)"
  rf-red-light: "oklch(73% 0.145 30)"
  rf-red-dark: "oklch(48% 0.178 30)"
  rf-red-reversed: "oklch(90% 0.028 30)"
  # RF White — body surfaces
  page-bg: "oklch(98.5% 0.004 258)"
  card-surface: "oklch(97.5% 0.006 258)"
  section-tint: "oklch(94% 0.010 258)"
  border: "oklch(87% 0.018 258)"
  # Ink — dark blue-gray family
  muted-text: "oklch(36% 0.048 260)"
  reading-ink: "oklch(27% 0.058 260)"
  heading-ink: "oklch(19% 0.088 260)"
  deepest-ink: "oklch(13% 0.068 260)"
typography:
  display:
    fontFamily: "Spectral, Georgia, serif"
    fontWeight: 700
    lineHeight: 1.08
  headline:
    fontFamily: "Spectral, Georgia, serif"
    fontWeight: 700
    lineHeight: 1.15
  title:
    fontFamily: "Spectral, Georgia, serif"
    fontWeight: 600
    lineHeight: 1.3
  body:
    fontFamily: "Figtree, system-ui, sans-serif"
    fontSize: "0.875rem"
    fontWeight: 400
    lineHeight: 1.6
  label:
    fontFamily: "Figtree, system-ui, sans-serif"
    fontSize: "0.75rem"
    fontWeight: 500
    letterSpacing: "0.12em"
rounded:
  sm: "2px"
  full: "9999px"
spacing:
  card-inner: "20px"
  hero-pad: "48px 20px"
  section-gap: "56px"
components:
  button-primary:
    backgroundColor: "{colors.civic-amber}"
    textColor: "{colors.reading-ink}"
    rounded: "{rounded.sm}"
    padding: "12px 24px"
  button-primary-hover:
    backgroundColor: "{colors.amber-hover}"
    textColor: "{colors.reading-ink}"
  button-ghost-dark:
    backgroundColor: "transparent"
    textColor: "{colors.gilt-text}"
    rounded: "{rounded.sm}"
    padding: "12px 24px"
  button-ghost-dark-hover:
    backgroundColor: "{colors.civic-blue-hover}"
    textColor: "{colors.section-tint}"
  nav-link:
    backgroundColor: "transparent"
    textColor: "{colors.civic-amber}"
    padding: "8px 12px"
    rounded: "{rounded.sm}"
  nav-link-active:
    backgroundColor: "{colors.civic-blue-active}"
    textColor: "{colors.section-tint}"
  card:
    backgroundColor: "{colors.page-bg}"
    rounded: "{rounded.sm}"
    padding: "{spacing.card-inner}"
  card-hover:
    backgroundColor: "{colors.archive-paper}"
---

# Design System: La politique Française pour les nuls

## 1. Overview

**Creative North Star: "The Impartial Ledger"**

La politique Française pour les nuls is a civic education tool that respects the reader's intelligence. The design system embodies that posture: it carries authority without asserting opinion, warmth without flattery. Every screen should feel like consulting a well-maintained reference — one that was designed by people who care about both truth and craft. Dense information is laid out with breathing room. Nothing competes with the content for attention.

The two-color architecture is the system's strongest visual idea: a deep institutional blue (the seal blue of the Republique Francaise, not the campaign blue of the tricolore) anchors every header and navigation band, while a warm civic amber runs through the body as the sole accent. The contrast between cool blue and warm amber creates a French civic identity without a single flag in sight. The amber pages themselves — off-white with warm borders — feel like parchment, like a dossier assembled with care.

The system explicitly rejects: partisan websites (biased by definition), French government sites (intimidating and bureaucratic), newspaper editorial pages (opinionated and loud), Wikipedia (too neutral to a fault), and flashy campaign design (tricolore everywhere, bold slogans). The system is also not a SaaS product page, not a dashboard, and not a portfolio. It is a reference.

**Key Characteristics:**
- Two-color architecture: civic blue + civic amber, never a third brand color
- Flat-by-default: no resting-state shadows; elevation is a hover state, not decoration
- Amber as the sole accent: links, highlights, primary actions — always amber, never blue
- Spectral for authority, Figtree for accessibility; they don't fight, they cooperate
- Mobile-first content hierarchy: the phone reader is the primary audience
- Language toggle always visible; bilingual (FR primary, EN secondary) is a design requirement

## 2. Colors: The Seal Palette

Two families. The blue grounds. The amber glows. They never compete.

### Primary
- **Civic Amber** (`oklch(62% 0.13 65)`): The single interactive accent. Used for primary CTA backgrounds, link text on light surfaces, breadcrumb highlights, the timeline year numerals, the nav logo mark. Every interactive affordance in the system is amber. Its rarity on the cool blue surfaces makes it feel like a warm light source.
- **Amber Hover** (`oklch(70% 0.11 65)`): CTA button hover state. Lighter, not darker — hovers move toward light.

### Neutral (dark)
- **Seal Blue** (`oklch(17% 0.07 252)`): The institutional anchor. Used for the nav header background and every page hero band. A very dark navy with just enough blue chroma to read as civic — not as corporate dark mode, not as amber-brown. All text on this surface uses gilt-text or amber-50 variants.
- **Civic Blue Hover** (`oklch(23% 0.09 255)`): Resting nav hover states on the dark band; ghost button hover on dark surfaces.
- **Civic Blue Active** (`oklch(32% 0.10 255)`): Active nav link background at 60% opacity.

### Neutral (light)
- **Reading Ink** (`oklch(30% 0.08 68)`): Primary body text on light surfaces. Warm dark brown; never pure black.
- **Ledger Tone** (`oklch(52% 0.12 64)`): Labels, subtext, metadata, category chips. The gray of the system is always amber-tinted.
- **Gilt Text** (`oklch(79% 0.082 66)`): Reversed text on the dark civic blue bands — subtitles, descriptions, breadcrumbs.
- **Vellum Edge** (`oklch(88% 0.048 68)`): Every border and divider in the system. One value, used consistently.
- **Archive Paper** (`oklch(97.5% 0.008 72)`): Card and panel backgrounds. Slightly warmer than the page background.
- **Section Tint** (`oklch(94% 0.022 70)`): Subtle section band tints (how-to bands, inner card panels). Not quite a card; not the page.
- **Page Background** (`oklch(97.5% 0.006 75)`): The html background. Barely cooler than Archive Paper; creates imperceptible depth.

### Named Rules
**The One Accent Rule.** The civic amber (`oklch(62% 0.13 65)`) is the only interactive color. No links are blue on the light surfaces. No UI uses the civic blue as a tint on the body. The blue is reserved for structural headers; the amber carries all meaning below.

**The No-Party Rule.** Individual party colors (RN navy, LFI red, Renaissance yellow, etc.) appear only as small color badges/chips — a maximum 44×44px swatch identifying the party. They never appear as large backgrounds, borders, or text colors in the UI chrome.

**The Neutral Is Never Gray Rule.** Every neutral in this system is amber-tinted (hue 65–72). Pure gray or cool neutral is banned; it reads as un-French and lifeless against the amber/blue architecture.

## 3. Typography: The Dispatch Pairing

**Display Font:** Spectral (with Georgia, serif fallback)
**Body Font:** Figtree (with system-ui, sans-serif fallback)

**Character:** Spectral brings editorial authority — its slightly condensed proportions and generous ink traps read as a serious newspaper of record. Figtree is geometric-humanist, warm, and legible at small sizes on phone screens. Together they say: "this is important, and it respects your time."

### Hierarchy
- **Display** (Spectral 700, ~4xl–6xl, line-height 1.08): Hero headlines only. The `font-display` Tailwind class. Max one per page. Used on the home page hero and not repeated on content pages.
- **Headline** (Spectral 700, ~3xl–4xl, line-height 1.15): Page titles (the `<h1>` on every content page inside the hero band).
- **Title** (Spectral 600, xl, line-height 1.3): Section headings within content (`<h2>`). Used with a bottom border rule in amber-200.
- **Body** (Figtree 400, 0.875rem/14px, line-height 1.6): All content paragraphs. Max line length 65ch on desktop. The reading experience.
- **Label** (Figtree 500–600, 0.75rem/12px, letter-spacing 0.12em, uppercase): Category chips, section eyebrow text, nav links, metadata. Never used for body copy.

### Named Rules
**The Spectral-Only Display Rule.** Only `font-display` (Spectral) headings may appear inside the dark civic-blue hero band. Body copy never enters the hero. This creates a consistent editorial distinction: the blue band is for orientation, the white/amber body is for reading.

**The Line Length Rule.** Body text containers cap at 65ch on desktop. Content pages use `max-w-3xl` or `max-w-4xl` with generous horizontal padding; never full-width prose.

## 4. Elevation

This system is **flat-by-default**. No surface has a resting-state shadow. Depth is expressed through tonal layering: page-bg → archive-paper (cards) → section-tint (inner panels) → vellum-edge borders. The hierarchy of lightness creates perceived depth without any shadows.

The single exception is hover state.

### Shadow Vocabulary
- **Whisper Hover** (`0 2px 16px oklch(17% 0.07 252 / 8%)`): Applied on interactive card hover via `.js-card`. The shadow color is seal-blue, not black — it reads as a cool depth rather than a dark lift. Combined with `translate: 0 -1px` for a 1px physical lift. Duration: 200ms ease-out-quart.

### Named Rules
**The Flat-By-Default Rule.** No surface renders a shadow at rest. Whisper hover is earned by interaction, not given as decoration. If a design review finds shadows on non-interactive elements, remove them.

## 5. Components

### Buttons
Blunt, direct, immediate. No pill radius, no gradient, no icon-heavy styling. The button earns attention by position and color, not by decoration.

- **Shape:** `rounded-sm` (2px). Square-shouldered; feels like a printed form field, not a SaaS product.
- **Primary** (`bg-civic-amber text-amber-950 px-6 py-3 font-semibold text-sm`): Full amber background, dark amber text for contrast. Always used on light surfaces (page body).
- **Primary hover:** `bg-amber-400` (lighter amber). Hover moves toward light, not dark.
- **Ghost / Dark** (`border border-amber-700 text-amber-300 px-6 py-3 font-medium text-sm`): Wire-frame on civic-blue surfaces (hero band, CTA pairs). The amber wire against blue is the system's color relationship made explicit.
- **Ghost / Dark hover:** `bg-civic-900` (very dark blue tint). Stays within the blue register; doesn't introduce a new color.

### Cards / Content Containers
Flat at rest; lift on hover via `.js-card`.

- **Corner Style:** `rounded-sm` (2px).
- **Background:** `archive-paper` (`amber-50`) on hover; `page-bg` at rest.
- **Border:** `vellum-edge` (`amber-200`); deepens to `amber-400` on hover.
- **Shadow:** none at rest; whisper-hover on `.js-card` elements.
- **Internal Padding:** `p-5` (20px) for list cards; `p-6` (24px) for section cards.
- **Scroll Reveal:** All content cards use `.js-reveal` for an entrance fade-up (500ms ease-out-quart, 10px translate). Stagger via `transition-delay` inline style.

### Navigation
Dark civic-blue band (`bg-civic-950`), 56px tall on desktop.

- **Logo mark:** Hexagonal SVG in `civic-amber` stroke + RF monotype. Logotype in Spectral, `text-amber-100`.
- **Nav links (default):** `text-amber-400 text-xs font-medium tracking-wide`. Amber text reads warm against the blue band.
- **Nav links (hover):** `text-amber-100 bg-civic-800/40` (subtle blue tint).
- **Nav links (active):** `text-amber-100 bg-civic-800/60` (stronger blue tint).
- **Language toggle:** Wire-frame amber button. Amber border on blue background; hover fills with `civic-800`.
- **Mobile:** Two-column grid below the header band. Same amber-on-blue treatment.

### Verify Badge
A signature component: marks content that requires source verification before use.

- **Style:** Pill (`rounded-full`), `amber-100` background, `oklch(40% 0.10 65)` text, `oklch(82% 0.07 70)` border. 0.7rem Figtree 500.
- **Usage:** Inline after the element it qualifies (party leader name, policy claim, historical date). Always accompanied by the warning emoji (&#9888;&#65039;) as a universal signal regardless of language.

### Timeline
The chronologie page uses a two-column timeline layout: Spectral numerals on the left (amber-500), a 1px amber-200 vertical rule, prose entries on the right.

- **Year column:** `width: 3.5rem`, right-aligned Spectral 700 in civic-amber. The year is the structural glue.
- **Entry column:** `border-left: 1px solid vellum-edge`, `padding-left: 1.25rem`. The thin rule is structural, not decorative (1px, not an accent stripe).
- **Scroll reveal:** Each event fades in with staggered delay, capped at 400ms total so the last event doesn't wait.

## 6. Do's and Don'ts

### Do:
- **Do** use `bg-civic-950` for every page header/hero band and the nav. The seal blue is the structural anchor; breaking it on any page makes that page feel unaffiliated.
- **Do** use civic amber as the sole interactive color on light surfaces — links, primary buttons, highlights, the timeline year numerals.
- **Do** use Spectral (font-display) for all headings. Mix weights (600 for titles, 700 for headlines) and use the italic variant sparingly for added texture.
- **Do** add `.js-card` to every interactive card element so hover elevation is consistent across the site.
- **Do** add `.js-reveal` to content groups (not individual words) so scroll entrance feels page-level, not chaotic.
- **Do** show party colors as small color badges only (max 44×44px). Name the party by typography, not by painting the UI in their colors.
- **Do** mark every unverified claim with `.verify-badge` and the warning emoji. This is a non-negotiable trust signal.
- **Do** keep body line length under 65ch. Use `max-w-3xl` or `max-w-4xl` containers with `leading-relaxed` for all reading content.
- **Do** use `oklch()` for any new color values. Never introduce an sRGB hex that isn't derived from an existing OKLCH token.

### Don't:
- **Don't** use `border-left` greater than 1px as a colored stripe accent. The 1px timeline rule is the only permitted side-rule and its role is structural (a vertical thread), not decorative. All other callouts, alerts, and cards use full borders or background tints.
- **Don't** use the civic blue (`civic-950`, `civic-800`, `civic-900`) as a tint or accent on light surfaces. Blue is reserved for structural headers. Amber is the accent. Mixing them on white pages creates visual noise.
- **Don't** add a resting-state box-shadow to any element. Whisper hover only; flat at rest.
- **Don't** make gradient text (background-clip: text + gradient). Single-color Spectral headings only.
- **Don't** use glassmorphism. No backdrop-filter on decorative elements.
- **Don't** put any French flag tricolore in the UI chrome — no blue-white-red sequence as a border, background, or decorative band. The civic blue + amber combination is the French identity; the literal tricolore belongs on no surface.
- **Don't** display party websites, editorial newspaper layouts, or government site aesthetics as references. Per PRODUCT.md, these are all anti-references.
- **Don't** use pure black or pure white (`#000`, `#fff`). Every dark surface has blue chroma; every light surface has amber chroma.
- **Don't** add a third brand color. If a design feels under-colored, the answer is tonal variation within the amber scale, not a new hue.
- **Don't** create identical card grids where every card is the same size with icon + heading + text. The party listing cards vary in content density; the section cards use large display numerals to break rhythm.
