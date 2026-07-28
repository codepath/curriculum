# curriculum — public-facing CodePath curriculum pages

**This repo hosts CodePath's public-facing GitHub Pages for curriculum.** Anything committed to `main` is published to the open internet. Treat every file here as partner-facing.

- **GitHub repo:** https://github.com/codepath/curriculum (org: `codepath`, public)
- **Live site (base URL):** https://codepath.github.io/curriculum/
- **Local working copy:** `/Users/sarcodepath/Code/curriculum/`

## How publishing works

GitHub Pages deploys from the `main` branch, root folder (`/`). **Push to `main` → the site rebuilds automatically** (usually live within ~1 minute). There is no separate deploy step and no build tooling — files are served as-is.

To confirm a deploy finished:
```bash
gh api "repos/codepath/curriculum/pages" --jq '.status'   # "built" when done
```

## URL structure

| File in repo | Public URL |
|---|---|
| `index.html` | https://codepath.github.io/curriculum/ (landing/hub page) |
| `catalog/index.html` | https://codepath.github.io/curriculum/catalog/ |
| `cir-curriculum-2026.html` | https://codepath.github.io/curriculum/cir-curriculum-2026.html |

Two page patterns are in use:
- **Folder + `index.html`** (e.g. `catalog/`) → gives a clean URL ending in `/`. **Preferred for pages meant to be shared as evergreen links.**
- **Flat `name.html`** at the root → URL ends in `.html`. Fine for one-off or standalone pages.

## Conventions for pages

- **Self-contained HTML.** Each page is a single `.html` file with CSS inlined in a `<style>` block. No build step, no shared stylesheet, no JS frameworks. Fonts load from Google Fonts via `<link>`.
- **Brand.** Match the existing pages: fonts `Space Mono` (headings/wordmark) + `Poppins` (body); colors navy `#1B1C57`, green accent `#00C385`, ink `#2b2d55`, muted `#6b6f8a`. A 5px green `.topbar` sits at the top; content is centered in a `.container`.
- **"Last updated" dates.** If a page shows a last-updated date, bump it whenever you edit the content.

## Adding a new page

1. Create the file — prefer `newpage/index.html` for a clean URL.
2. If it should be discoverable from the hub, add a `.page-card` link to it in the root `index.html`. **Not every page has to be linked** — e.g. `cir-curriculum-2026.html` (an instructor briefing) is intentionally unlisted on the landing page.
3. Commit and push to `main`. Verify the new URL returns 200.

## Before you publish — reminders

- **Everything here is public.** Do not commit anything not cleared for external eyes (internal notes, unreleased plans, PII, credentials).
- These pages are shared with partners as evergreen links, so **avoid renaming or moving files that are already circulating** — it breaks the shared URL. Add redirects or keep the old path if a move is unavoidable.

## Roadmap

- AI automation to keep pages in sync with the source of truth for course descriptions/syllabi and redeploy automatically. Source of truth for course data is not yet wired up — ask the user where it lives (Notion / Google Doc / syllabi repo) before building this.
