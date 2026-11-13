# pmwhileblack.com

PM While Black, served by GitHub Pages. Ported from WordPress.com in November 2026.
GitHub builds the site with Jekyll on every push to `main`. There is no build step to run.

## Write a new post

Add a file to `_posts/` named `YYYY-MM-DD-your-slug.md`:

```markdown
---
title: "Your title"
cats: [becomeapm]
summary: "One or two sentences. Shown on the home page and category pages."
---

Write the post in Markdown here.
```

Commit and push. The post goes live at `/YYYY/MM/DD/your-slug/`.
A post dated in the future stays hidden until that date.

Category keys for `cats` are in `_data/categories.yml`:
`whatispm`, `becomeapm`, `developpmskills`, `climbtheladder`, `successstories`, `uncategorized`.

Put images in `assets/uploads/` and reference them as `/assets/uploads/your-image.jpg`.

## Where things live

| What | Where |
|---|---|
| Posts | `_posts/` (imported ones are HTML, new ones can be Markdown) |
| Pages (Consulting, Contact, legal) | `pages/` |
| Sidebar menu | `_data/nav.yml` |
| Footer links | `_data/footer.yml` |
| Old WordPress comments (read-only) | `_data/comments.json` |
| Look and layout | `assets/css/style.css`, `_layouts/`, `_includes/` |
| Posts shown on the home page | `home_post_count` in `_config.yml` |

## Preview locally (optional)

```bash
gem install jekyll jekyll-sitemap jekyll-feed
```

```bash
jekyll serve --baseurl ""
```

Then open http://localhost:4000.

## Domain

`CNAME` holds the custom domain. DNS for pmwhileblack.com points at GitHub Pages:
four `A` records on the root (185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153)
and a `CNAME` on `www` to `kayiitaj.github.io`.
