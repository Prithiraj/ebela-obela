# EBELA OBELA website

Conversion-focused, research-backed static website for EBELA OBELA, Naktala/Brahmapur, Kolkata.

## Structure

- `DESIGN_PLAN.md` — approved research/design/implementation plan
- `PHOTO_RIGHTS.md` — prototype photography provenance and replacement requirements
- `site/` — deployable static website
- `.github/workflows/pages.yml` — GitHub Pages deployment

## Local preview

```bash
python3 -m http.server 8080 --directory site
```

Then open `http://localhost:8080`.

## Deployment

Pushes to `main` deploy `site/` to GitHub Pages through the official Pages Actions workflow.

Expected project URL: `https://prithiraj.github.io/ebela-obela/`

## Content policy

The visible business facts and menu examples are evidence-backed as documented in `DESIGN_PLAN.md`. Do not add prices, offers, opening hours, reviews, policies, or claims without re-verifying them first.

## Photography

The current prototype uses actual EBELA OBELA photography referenced from third-party pages. **Replace or license those photos before commercial launch.** See `PHOTO_RIGHTS.md`.
