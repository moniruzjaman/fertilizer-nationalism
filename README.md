# Fertilizer Management: The Path to Bloom 🌾
Self-contained interactive landing page for the Ministry of Agriculture briefing (Sept 2026).
Single `index.html` — no build step, no CDN, no external assets.

## Deploy to GitHub Pages (auto)
1. Create a **public** repo, e.g. `fertilizer-path-to-bloom`.
2. Add `index.html` at the root and `.github/workflows/deploy.yml` as shown.
3. `git add . && git commit -m "launch" && git push`.
4. One-time: **Settings → Pages → Build and deployment → Source: GitHub Actions**.
5. Every push to `main` now auto-deploys to `https://<user>.github.io/<repo>/`.

## Icons (zero binary files in repo)
- **Favicon:** inline SVG data-URI of a golden panicle of rice (works with JS disabled).
- **Apple touch icon:** generated at runtime on a `<canvas>` and attached as a **JPEG data-URI**
  (`link rel="apple-touch-icon"`), with a PNG fallback link for legacy browsers.
- Want a static file? Open the page, run `copy(window.__iconDataURL)` in the console,
  save as `apple-touch-icon.jpg` at the repo root, and replace the empty `href` in `<head>`.
