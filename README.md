# solvern.dev

The Solvern company page: one static HTML file, no build step, no JavaScript,
no external resources. Served by Cloudflare Pages from this repository —
every push to `main` deploys.

- `public/index.html` — the page (inline CSS, inline SVG favicon, light and dark via `prefers-color-scheme`)
- `public/_headers` — Cloudflare Pages response headers (HSTS, a deny-everything CSP, nosniff, referrer and permissions policies)
- `public/robots.txt`
- `wrangler.jsonc` — lets the Workers flow deploy `public/` as static assets; the Pages flow needs output directory `public`

To change the page: edit `public/index.html`, push. To preview locally: open the file in a browser.
