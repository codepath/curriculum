# Curriculum

A home for CodePath's shareable curriculum pages, published to GitHub Pages as evergreen URLs.

**Live site:** https://codepath.github.io/curriculum/

## Pages

| Page | Path | URL |
|------|------|-----|
| Landing | [`index.html`](index.html) | https://codepath.github.io/curriculum/ |
| Course Catalog | [`catalog/index.html`](catalog/index.html) | https://codepath.github.io/curriculum/catalog/ |
| CS1 with GenAI — Year 2 Instructor Briefing | [`cir-curriculum-2026.html`](cir-curriculum-2026.html) | https://codepath.github.io/curriculum/cir-curriculum-2026.html |

> **Note:** everything in this repo is published publicly. See [`CLAUDE.md`](CLAUDE.md) for full conventions.

## How it works

- Each page is a single self-contained HTML file (styles inlined).
- Pushing to `main` automatically publishes to GitHub Pages.
- New pages go in their own folder (e.g. `pathways/index.html` → `/curriculum/pathways/`) and get linked from the landing page.

## Updating

Edit the relevant HTML file and push to `main`. For the catalog, bump the "Last updated" date in the header to match.

## Roadmap

- AI automation to keep pages in sync with approved course descriptions and syllabi, and redeploy automatically.
