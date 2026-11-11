# Xin-Yu Xiao's Academic Homepage

Source of [xin-yuxiao.github.io](https://xin-yuxiao.github.io), built with Jekyll and served by GitHub Pages from the `main` branch.
The site is based on the [academic-homepage](https://github.com/luost26/academic-homepage) template by Shitong Luo.

## Preview locally

GitHub Pages only builds `main`, so check other branches locally before merging.

```bash
bundle install              # first time only
bundle exec jekyll serve    # then open http://127.0.0.1:4000
```

## Where things live

| What | File |
| --- | --- |
| Name, bio, portrait, contact links, education, awards | `_data/profile.yml` |
| Bold names, links and display names of authors | `_data/authors.yml` |
| Navbar entries | `_data/navigation.yml` |
| Homepage sections and number of news items | `_data/display.yml` |
| Publications (one file per paper) | `_publications/<year>/*.md` |
| News (one file per item) | `_news/*.md` |
| Paper PDFs and CV | `assets/files/` |
| Publication cover images | `assets/images/covers/` |
| Portrait, mobile avatar | `assets/images/photos/` |
| Favicon and touch icon | `assets/images/favicon-32.png`, `assets/images/apple-touch-icon.png` |

## Adding a publication

Create `_publications/<year>/<year>-pub-<Name>.md`:

```yaml
---
title: "Paper Title"
date: 2026-01-01 00:00:00 +0800   # used for sorting
selected: true                    # also show on the homepage
pub: "Venue name"
pub_date: "2026"
pub_last: ' <span class="badge badge-pill badge-publication badge-success">Published</span>'
abstract: >-
  One-paragraph summary.
cover: /assets/images/covers/CoverN.jpg
authors:
  - Xin-Yu Xiao        # bold via _data/authors.yml
  - "Co Author*"       # * = equal contribution
  - "Other Author#"    # # = corresponding author
links:
  Paper: /assets/files/paper.pdf
  ACL Anthology: https://aclanthology.org/...
---
```

Optional fields: `semantic_scholar_id` (40-character Semantic Scholar paper ID, shows a citation badge), `pub_pre`, `pub_post`.

## Adding a news item

Create `_news/<year>-<slug>.md` with a `title` and a `date`; the homepage shows the latest items.

## License

Template code is under the MIT License, see `LICENSE`.
