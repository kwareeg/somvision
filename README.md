# SOMVISION Website

Static website for Som Vision Consultancy Services Ltd, built with Astro and Tailwind CSS. Optimized for Cloudflare Pages.

## Tech Stack

- Astro 6 (static site generator)
- Tailwind CSS v4
- Zero JavaScript frameworks (pure HTML/CSS with minimal vanilla JS for mobile menu and form)
- Cloudflare Pages compatible

## Development

```bash
npm install
npm run dev
```

## Production Build

```bash
npm run build
```

Output goes to `dist/`. Total build size is under 400KB.

## Deploy to Cloudflare Pages

1. Push this repo to GitHub
2. Go to dash.cloudflare.com > Workers & Pages > Create > Pages
3. Connect your GitHub repo
4. Build settings:
   - Build command: `npm run build`
   - Build output directory: `dist`
   - Framework preset: Astro (or leave blank)
5. Deploy

Cloudflare Pages will rebuild automatically on every push to main.

## Project Structure

```
src/
  layouts/Base.astro       - HTML shell, head, meta, font loading
  components/
    Header.astro           - Sticky nav with dropdowns + mobile menu
    Footer.astro           - Dark footer with nav columns
    PageHero.astro         - Reusable page banner
    SectionIntro.astro     - Section heading block
    CTABand.astro          - Call-to-action band
  pages/
    index.astro            - Home
    about/index.astro      - About (5 anchor sections)
    services/index.astro   - Services (5 service sections)
    sectors/index.astro    - Sectors (4 sector sections)
    work/index.astro       - Our Work (projects, clients, impact)
    publications/index.astro - Publications (reports, briefs, insights, papers)
    contact/index.astro    - Contact form
  styles/global.css        - Design system and Tailwind theme
```
