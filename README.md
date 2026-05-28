# La politique française pour les nuls

A non-partisan civic education website that helps French citizens — especially first-time voters — understand how their political system actually works.

No punditry, no spin. Just structured, verified facts.

> [!NOTE]
> Content is primarily in French, with an optional English toggle available on every page.

## What's inside

| Page | Route | Description |
|------|-------|-------------|
| Home | `/` | Overview and navigation hub |
| Parties | `/partis/` | Profile for each major political party |
| Institutions | `/institutions` | Executive, legislative, judicial and territorial branches |
| Electoral system | `/systeme-electoral` | Voting rules, two-round system, upcoming 2027 elections |
| Timeline | `/chronologie` | 30 years of French political history (1995–2026) |
| Reforms | `/reformes` | Major reforms with balanced supporters/opponents perspectives |
| Glossary | `/glossaire` | 32+ political terms, searchable and filterable |

## Tech stack

- **[Astro](https://astro.build)** — static site generator with file-based routing
- **[Tailwind CSS v4](https://tailwindcss.com)** — via the official `@tailwindcss/vite` plugin
- **Vanilla JS** — client-side language toggle (stored in `localStorage`), glossary filtering, scroll-triggered reveal animations
- **JSON content** — all data lives in `content/` as structured, source-cited JSON files

## Getting started

**Prerequisites:** Node.js 20+

```bash
# Install dependencies
npm install

# Start the dev server
npm run dev

# Build for production
npm run build

# Preview the production build locally
npm run preview
```

## Project structure

```
content/          # All site content as JSON files
  parties/        # One file per political party
  glossary.json
  institutions.json
  electoral-system.json
  reforms.json
  timeline.json
src/
  components/     # Astro components (Nav, Footer, SpectrumStrip)
  layouts/        # Base Layout.astro
  pages/          # File-based routes
  styles/         # Global CSS with Tailwind theme
public/           # Static assets
.github/
  workflows/      # GitHub Actions deployment pipeline
```

## Deployment

The site is deployed to **GitHub Pages** via GitHub Actions on every push to `main`.

Live URL: `https://albaptis.github.io/french-politics-for-noobs`

> [!IMPORTANT]
> If you fork this repository, update the `site` and `base` values in `astro.config.mjs` to match your own GitHub username and repository name before deploying.

To enable GitHub Pages on a fork:
1. Go to **Settings → Pages**
2. Set the source to **GitHub Actions**

## Content

All content is stored as JSON in `content/`. Each file is structured with bilingual fields (`fr`/`en`), source citations, and a `status` field (`verified` / `needs-verification`).

Parties covered: Renaissance, RN, LFI, PS, LR, MoDem, and others.

> [!TIP]
> Content snapshots are dated. Check `status` fields and source URLs before citing any data.
