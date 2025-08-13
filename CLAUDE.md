# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Development Commands

- `npm run dev` - Start development server at localhost:4321
- `npm run build` - Build production site to ./dist/
- `npm run preview` - Preview production build locally
- `npm install` - Install dependencies

## Project Architecture

This is a business website for Peak Season Services, a holiday lighting company in Denton, Texas, built with:

- **Astro 5.12.9** - Static site generator with island architecture
- **TailwindCSS 3.4.17** - Utility-first CSS framework with PostCSS
- **TypeScript** - Strict configuration extending Astro's strict tsconfig

### Site Structure

Each page in `src/pages/` is a complete Astro document that includes:
- Full HTML structure (html, head, body tags)
- SEO metadata (title, description, Open Graph, keywords)
- Structured data (JSON-LD for local business)
- Navigation component (duplicated across pages)
- Content sections with TailwindCSS classes

### Pages Architecture

All pages follow the same pattern:
- Import global.css for Tailwind and custom holiday styles
- Define SEO variables at the top
- Complete HTML document structure
- Sticky navigation with dropdown menus
- Main content sections
- Footer with contact info and schema markup

### Custom Styling

`src/styles/global.css` includes:
- `.holiday-gradient` - Green/red gradient backgrounds
- `.holiday-glow` - Green glow shadow effect  
- `.text-holiday-gradient` - Gradient text effect

### SEO Focus

Every page is heavily optimized for local SEO:
- Location-specific keywords (Denton TX zip codes)
- Structured data for local business
- Service-specific landing pages
- Geographic targeting for North Texas area

### Component Usage

- `Breadcrumbs.astro` - Schema.org compliant breadcrumb navigation
- Navigation is currently duplicated across pages (not componentized)