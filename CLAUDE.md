# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Personal portfolio website for Amber Gianvecchio. The site showcases professional projects and accomplishments to hiring managers, providing tangible evidence beyond resume bullet points.

**Hosting:** GitHub Pages
**Framework:** Astro (static site generator)

## Commands

```bash
npm run dev      # Start dev server at localhost:4321
npm run build    # Build for production (outputs to dist/)
npm run preview  # Preview production build locally
```

## Architecture

```
src/
├── layouts/Layout.astro    # Base HTML layout with meta tags
├── components/             # Reusable Astro components
│   ├── Header.astro        # Fixed navigation
│   ├── Hero.astro          # Homepage hero section
│   ├── ProjectCard.astro   # Reusable project card (props: title, description, tags, image, link, featured)
│   ├── WorkSection.astro   # Projects grid section
│   ├── AboutSection.astro  # Bio and skills
│   └── ContactSection.astro # Contact info and footer
├── pages/                  # File-based routing
│   └── index.astro         # Homepage
└── styles/global.css       # CSS variables and base styles
```

**Styling:** CSS variables defined in `global.css`. Dark theme with `--bg-primary: #0d0d0d`, accent `--accent: #3636ff`.

**Deployment:** GitHub Actions workflow (`.github/workflows/deploy.yml`) auto-deploys on push to main.

## Background Materials

The `Background Information/` folder contains source materials (not deployed):

- `Gianvecchio_Resume_2026.pdf` - Current resume
- `Notion - Website Brainstorm/` - Site planning and inspiration links
- `allUP Stats:Metrics:Projects/` - Project documentation and screenshots from allUP work:
  - Front AI Drafter project documentation (AI-powered customer support system)
  - Screenshots of Cursor IDE, Braintrust testing, Git workflows
  - Front analytics dashboard showing 17,000+ messages/year
  - Development workflow documentation

## Portfolio Content to Feature

**allUP (Primary showcase)**
- Front AI Drafter: AI agent system built with OpenAI Agents SDK
- 98%+ categorization accuracy through iterative prompt engineering
- Testing infrastructure with evaluation datasets and TypeScript test scripts
- Full development workflow: Cursor IDE → Git → OpenAI Agent Builder → Braintrust

**Advekit**
- Notion workspace for operations
- Retention campaigns and web design
- HubSpot CRM automation
