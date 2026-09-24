# Erinc's Blog

A minimal Astro blog. Posts are plain markdown files in `src/content/blog/`.

## Run locally

```bash
npm install
npm run dev
```

Open http://localhost:4321

## Add a new post

Create `src/content/blog/my-post-slug.md`:

```md
---
title: "My Post Title"
description: "One-line summary"
pubDate: 2026-09-22
tags: ["life", "code"]
---

Post content in markdown goes here.
```

The homepage lists posts automatically, newest first.

## Deploy to Cloudflare Pages

1. Push this project to a GitHub repo.
2. Go to the Cloudflare dashboard → **Workers & Pages** → **Create application** → **Pages** → **Connect to Git**.
3. Select your repo. For build settings use:
   - **Framework preset:** Astro
   - **Build command:** `npm run build`
   - **Build output directory:** `dist`
4. Deploy. Cloudflare will give you a `*.pages.dev` URL, and every future push to `main` auto-deploys.
5. Optional: add a custom domain under the Pages project's **Custom domains** tab.

Update `site` in `astro.config.mjs` to match your final domain (used for RSS/sitemap links if you add them later).
