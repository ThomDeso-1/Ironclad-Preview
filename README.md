# Ironclad-Preview

`index.html` — a self-contained, Steam-style preview page for showing **Ironclad**
off (on a personal site, in a portfolio, embedded in Notion, etc.) **without**
publishing the game's source repo. It is prose + gameplay screenshots only.

## Hosting

The page is one static HTML file with no build step. It's served here via GitHub
Pages:

- **Live URL:** https://thomdeso-1.github.io/Ironclad-Preview/

To embed in Notion: `/embed` → paste that URL → drag the frame tall (the page is
long). GitHub Pages sends no `X-Frame-Options`, so framing works.

## About the file

- **Self-contained.** All screenshots and the key art are base64 data URIs. The
  only external request is the Google Fonts stylesheet (Big Shoulders Display /
  Inter / JetBrains Mono). Safe to drop on any static host or open with `file://`.
  ~4 MB, so first load is a beat, then cached.
- **Theme-aware.** Follows the visitor's light/dark preference; a corner toggle
  overrides.
- **Not affiliated** with Hasbro / Avalon Hill / Wizards of the Coast, or with
  Steam / Valve — the footer says so. "Steam-styled" means the *layout*, not the
  branding. No price, no fabricated reviews.

## Updating

Regenerate `ironclad-store-page.html` in the main Ironclad repo (`marketing/`),
copy it here as `index.html`, and push.
