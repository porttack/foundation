# SLV Foundation for Education

Website for the San Lorenzo Valley Foundation for Education — a 501(c)(3) non-profit supporting public education in the San Lorenzo Valley Unified School District since 2003.

**Live site:** https://slvfoundation.org  
**GitHub repo:** https://github.com/porttack/foundation

## Built with

- [Jekyll](https://jekyllrb.com/) static site generator
- Hosted on [GitHub Pages](https://pages.github.com/)
- Custom CSS (green/gold theme)
- Fonts: Lora + Source Sans 3 (Google Fonts)
- Donations via PayPal (hosted button `UZDX47HHMQKHN`)

## Current pages

| File | Page | Status |
|------|------|--------|
| `index.md` | Home | Live |
| `programs.md` | Programs | Live |
| `donate.md` | Donate | Live — PayPal linked |

Pages removed for now (content preserved in git history): About, Scholarships, Community Partners, News.

## How to edit content

All content pages are Markdown files — edit them directly in the GitHub web editor (no local setup needed). Committing to `main` triggers an automatic rebuild via GitHub Pages.

## Adding a news post

1. Create a new file in `_posts/` named `YYYY-MM-DD-your-title.md`
2. Add this front matter:
```
---
layout: post
title: "Your Post Title"
date: YYYY-MM-DD
---
```
3. Write content below, then commit — GitHub Pages rebuilds automatically.

## Restoring removed pages

To restore a removed page (About, Scholarships, etc.):
1. Find the file in git history: `git log --all -- about.md`
2. Restore it: `git checkout <commit> -- about.md`
3. Add it back to `nav_pages` in `_config.yml`

## TODO

- [ ] Redirect `slvfoundation.com` and `www.slvfoundation.com` → `slvfoundation.org` (via registrar URL forwarding or Cloudflare)
- [ ] Confirm PayPal donate button goes to the right account (test the live link)
- [ ] Convert logo to PNG for better favicon compatibility across older browsers
- [ ] Restore and update the About page
- [ ] Restore and update the Scholarships page
- [ ] Add board meeting dates/info once available
- [ ] Add real Facebook URL to `_config.yml` (currently a placeholder)

## Local development (optional)

```bash
gem install bundler
bundle install
bundle exec jekyll serve
# visit http://localhost:4000
```
