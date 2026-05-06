# gzuk.app

![그려적어 GZUK](https://github.com/user-attachments/assets/b5a7e55e-d7f4-42a4-b8c2-0e1ae854a63e)

[🔗 Landing page for 그려적어 (GZUK)](https://gzuk-app.vercel.app/)

## Setup

```bash
npm install
npm run dev
```

Open http://localhost:3000.

## Structure

```
app/
├─ layout.tsx       — root HTML, loads Gowun Dodum (Korean handwriting font)
├─ page.tsx         — entire landing page (single client component, sections inlined)
├─ i18n.ts          — Korean ⇆ English string table + lang toggle helper
└─ globals.css      — Tailwind base + light/dark backgrounds

public/
└─ screenshots/     — drop hero.png, demo.png etc. here
```

## Deploy

1. Push this repo to GitHub
2. On Vercel, import the repo → Framework: Next.js (auto-detected)
3. No env vars needed
4. Custom domain: add `gzuk.app` in Vercel project settings, update DNS at registrar (CNAME → cname.vercel-dns.com)

## Adding screenshots

Put PNGs in `public/screenshots/` and update the `<img src="/screenshots/...">` paths in `app/page.tsx`.
