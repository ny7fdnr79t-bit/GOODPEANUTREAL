# Peanut — going live

`index.html` is the whole site: one self-contained file. No build step, no server, no dependencies to install. Open it locally by double-clicking it.

Note: the 3D house loads three.js from a CDN (unpkg.com), so the page needs an internet connection to draw it. Everything else works offline.

## Option 1 — Netlify Drop (fastest, free)

1. Go to app.netlify.com/drop
2. Drag the `deploy` folder onto the page.
3. You get a live URL in about ten seconds, e.g. `peanut-x7f2.netlify.app`.
4. To use your own domain: Site configuration → Domain management → Add a domain, then point your registrar's DNS at Netlify.

## Option 2 — Vercel

1. Install: `npm i -g vercel`
2. From this folder: `vercel --prod`
3. Follow the prompts. Same result, custom domains under Project → Domains.

## Option 3 — Cloudflare Pages

1. dash.cloudflare.com → Workers & Pages → Create → Pages → Upload assets.
2. Upload the `deploy` folder. Build command: none. Output directory: `/`.

## Option 4 — your existing host

Upload `index.html` to the web root (often `public_html/` or `www/`) via FTP or your host's file manager. It must be named `index.html` to serve at the domain root.

## Updating the site later

Re-export the bundle after any change to the design, then re-upload (or re-drag) `index.html`. Netlify and Cloudflare both let you drag a new folder over the existing site to replace it.

## Before you launch

- The dollar figures, the 2.9× return, "140 properties" and the 19-day claim are placeholders. Replace them with your real numbers.
- Phone and email are placeholders: `(000) 000-0000` and `hello@peanut.example`.
- Forms are front-end only — nothing is sent anywhere yet. To collect submissions, Netlify Forms is the least work: add `netlify` to the `<form>` tag, or wire the intake to Formspree.
- No analytics installed. Plausible or Cloudflare Web Analytics is a one-line paste in `<head>`.
