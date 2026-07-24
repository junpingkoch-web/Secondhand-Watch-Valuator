# Secondhand Watch Valuator

A free, static (no build step) tool for estimating the resale value of a
secondhand watch: pick brand, model, years held, and condition, and it
gives a heuristic reference value range and a value-retention score based
on typical brand resale patterns. Trilingual UI: 中文 / English / Deutsch.

This is also embedded directly in the [watch-guide-blog](https://github.com/junpingkoch-web/watch-guide-blog)
under `static/tools/watch-valuator/` — the two copies are kept in sync
manually; update both when changing the tool.

## Run locally

Just open `index.html` in a browser, or serve the folder with any static
server, e.g.:

```
npx serve .
```

## Deploy

Any static host works (GitHub Pages, Netlify, Vercel, Cloudflare Pages,
S3, etc.) — upload the folder as-is.

Before going live:

1. Replace `ca-pub-XXXXXXXXXXXXXXX` in `index.html` with your real AdSense
   publisher ID (already set correctly in `ads.txt`).
2. Add your AdSense `<ins>` snippet inside the `.ad-slot` placeholders in
   `index.html`.
3. Update the `buymeacoffee.com` link in `index.html` if you want the
   support button to point elsewhere.
4. The valuation heuristics are approximate reference figures, not a
   formal appraisal — double-check before relying on them.

## Structure

- `index.html` — single-file build: markup, styling, and the zh/en/de
  text dictionary + valuation logic are all inline in this one file
  (unlike the split `index.html`/`style.css`/`script.js` layout used by
  the other tools in this portfolio).
