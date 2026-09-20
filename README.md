# solvern.dev

The Solvern company page: one static HTML file, no build step, no JavaScript,
no external resources. Served by Cloudflare Pages from this repository —
every push to `main` deploys.

- `index.html` — the page (inline CSS, inline SVG favicon, light and dark via `prefers-color-scheme`)
- `_headers` — Cloudflare Pages response headers (HSTS, a deny-everything CSP, nosniff, referrer and permissions policies)
- `robots.txt`
- `wrangler.jsonc` — lets the Workers flow deploy this directory as static assets (`.assetsignore` keeps the repo files out); the Pages flow uses output directory `/`

To change the page: edit `index.html`, push. To preview locally: open the file in a browser.
