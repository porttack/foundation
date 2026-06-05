# SLV Foundation for Education

Website for the San Lorenzo Valley Foundation for Education — a 501(c)(3) non-profit supporting public education in the San Lorenzo Valley Unified School District since 2003.

**Live site:** https://slvfoundation.org  
**Staging:** https://porttack.github.io/foundation

## Built with

- [Jekyll](https://jekyllrb.com/) static site generator
- Hosted on [GitHub Pages](https://pages.github.com/)
- Custom CSS (green/gold theme)
- Fonts: Lora + Source Sans 3 (Google Fonts)

## How to edit content

All content pages are Markdown files — you can edit them directly in the GitHub web editor (no local setup needed).

| File | Page |
|------|------|
| `index.md` | Home |
| `about.md` | About Us |
| `scholarships.md` | Scholarships |
| `programs.md` | Programs |
| `community-partners.md` | Community Partners |
| `donate.md` | Donate |
| `news.md` | News listing |
| `_posts/YYYY-MM-DD-title.md` | Individual news posts |

## Adding a news post

1. Create a new file in `_posts/` named `YYYY-MM-DD-your-title.md`
2. Add this header at the top:
```
---
layout: post
title: "Your Post Title"
date: YYYY-MM-DD
---
```
3. Write your content in Markdown below the header
4. Commit — GitHub Pages will rebuild automatically

## Adding the logo

Drop your logo file into `assets/images/` named `logo.png` (or update the filename in `_layouts/default.html`).

## Adding the PayPal donate button

1. Log in to paypal.com → Tools → PayPal Buttons → Donate
2. Copy the embed code
3. Open `donate.md` and replace the placeholder comment block with your embed code

## Switching to the custom domain

When `slvfoundation.org` is fully propagated, edit `_config.yml`:
```yaml
baseurl: ""
url: "https://slvfoundation.org"
```

## Local development (optional)

```bash
gem install bundler
bundle install
bundle exec jekyll serve
# visit http://localhost:4000/foundation
```
