# loadbearing-site

Marketing landing page for **Load Bearing** — the satirical incremental clicker
in development at [mscrnt/loadbearing](https://github.com/mscrnt/loadbearing).

Lives at https://loadbearing.games — Cloudflare Pages, custom domain on the
mscrnt CF account, auto-deploys from `main`.

## Stack

Pure static HTML/CSS/SVG. No build step, no JS framework, no bundler. One
`index.html`, one `style.css`, an inline SVG grid + an inline SVG stamp.
Per the LoadBearing [PRINCIPLES.md](https://github.com/mscrnt/loadbearing/blob/main/docs/PRINCIPLES.md) — *a consistent cheap thing beats an inconsistent expensive thing.*

## Local dev

```bash
python3 -m http.server 8000
# → http://localhost:8000
```

## Deploy

Push to `main` → Cloudflare Pages picks it up. The CF Pages project name is
`loadbearing-site`; the custom domain `loadbearing.games` is attached to the
production branch.

## Files

| File | Purpose |
|---|---|
| `index.html` | Single-page site. Hero + about + 6-card systems overview + CTA strip + footer. |
| `style.css` | Blueprint palette (`#0e2540` bg, `#f1f5f9` ink, `#d63837` stamp), draftsman serif + grotesque + mono stack, responsive grid. |
| `favicon.svg` | The CERTIFIED stamp, miniature. |
| `robots.txt` | Block AI training crawlers, allow AI live-search crawlers. |
| `sitemap.xml` | Single URL — landing page. |
