# Your Blog (GitHub Pages)

A minimal, fast, SEO-friendly static blog in English covering **AI**, **Finance**, and **Life**.
No build step, no framework — just HTML + one shared CSS file.

## Structure

```
github-blog/
├─ index.html            # Home: hero + category filter + post cards
├─ about.html            # About page
├─ assets/
│  └─ style.css          # ONE shared stylesheet for every page
└─ posts/
   ├─ _template.html     # Copy this to start a new post
   ├─ example-post.html  # A filled-in example
   └─ images/            # Put each post's images here
```

## Publish on GitHub Pages

1. Create a repo named `aifinote` under the `leeduri` account.
2. Put the **contents** of this `github-blog/` folder at the repo root.
3. Push to the `main` branch.
4. Repo → **Settings → Pages → Build from branch → main / root**.
5. Your site is live at `https://leeduri.github.io/aifinote/`.

> This is a **project page** (served under `/aifinote/`), not a user page. The
> relative links (`assets/…`, `posts/…`, `../`) work as-is; the absolute URLs in
> canonical / Open Graph / JSON-LD are already set to
> `https://leeduri.github.io/aifinote/…`. Still replace `Your Blog` / `Your Name`
> with your real blog name and author name before publishing.

## Add a new post

1. Copy `posts/_template.html` → `posts/my-new-post.html`.
2. Fill in: `<title>`, meta description, canonical/OG URLs, the JSON-LD block,
   the `data-cat` category (`ai` | `finance` | `life`), title, body.
3. Put images in `posts/images/` (use `1200×630` WebP/PNG for the cover).
4. Add a card to `index.html` (copy an existing `<a class="card">` block, set its
   `href`, `data-cat`, thumbnail, title, excerpt, date). Newest first.

## Ads

Paste the AdSense code into the `<div class="ad-slot">` at the end of each post's
`<article>` — the very last thing in the body, per this project's rule.

## SEO notes (already baked in)

- `Article` + `BreadcrumbList` structured data (the combo that still earns rich
  results / AI citations in 2026).
- Canonical + Open Graph tags per page.
- Semantic headings (one H1, H2/H3 hierarchy), question-then-answer sections.
- Light/dark mode, mobile-first, lazy-loaded images.

**Still to do after publishing:** register the site in Google Search Console,
submit a `sitemap.xml`, and keep `dateModified` current when you edit a post.
