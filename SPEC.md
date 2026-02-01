# Zelipt Marketing Site — Spec

This repository contains a minimal marketing site for **Zelipt**, built with **Astro** and **Tailwind CSS**.

## Goals

- Provide a simple public-facing marketing website (static pages)
- Keep content editable as plain `.astro` files
- Keep styling minimal and utility-first via Tailwind

## Tech Stack

- **Astro** (static site generator)
- **Tailwind CSS** (via the official `astro add tailwind` setup)

## Information Architecture

### Shared Layout

File: `src/layouts/Layout.astro`

- Global `<head>`:
  - `title` + `description` (props)
  - viewport + generator meta
  - favicon links
- Header:
  - Site name (links to `/`)
  - Navigation: Home / Pricing / Contact
- Main content area:
  - centered container with padding
- Footer:
  - copyright line (placeholder)

### Routes / Pages

#### `/` — Home

File: `src/pages/index.astro`

Sections / placeholders:
- Hero headline: **"Scrape & enrich leads automatically"**
- Short value proposition paragraph (placeholder)
- Feature list (placeholder)
- Primary CTA button (placeholder)
- Secondary link to pricing

#### `/pricing` — Pricing

File: `src/pages/pricing.astro`

Sections / placeholders:
- Page title
- 3 pricing blocks (Starter / Pro / Enterprise)
  - short description
  - price placeholder

#### `/contact` — Contact

File: `src/pages/contact.astro`

Sections / placeholders:
- Page title
- Contact email (placeholder)
- Note to add a form integration later (placeholder)

## Styling

- Global stylesheet: `src/styles/global.css`
  - Tailwind included via `@import "tailwindcss";`
- Page styling is intentionally light (basic spacing/typography/layout) using Tailwind utilities.

## Development

```sh
npm install
npm run dev
```

## Tests / Checks

```sh
npm test
```

(Uses `astro check` as a lightweight sanity check.)

## Build

```sh
npm run build
npm run preview
```

Build output is generated in `dist/`.

## Deployment Notes

This project is a static site.

Common deployment defaults:
- **Netlify**
  - Build command: `npm run build`
  - Publish directory: `dist`
- **Vercel**
  - Framework preset: Astro
  - Output directory: `dist`

No environment variables are required for the current placeholder pages.
