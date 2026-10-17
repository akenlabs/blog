# Ken's Blog

Source for [blog.akenlabs.com](https://blog.akenlabs.com) — a personal blog about AI, business, and life.

Built with Jekyll and deployed to GitHub Pages through GitHub Actions.

## Local development

```bash
bundle install
bundle exec jekyll serve
```

## Writing

Posts live in `_posts/` with the filename `YYYY-MM-DD-slug.md`.

```yaml
---
layout: post
title: "Post title"
date: 2026-10-17 14:30:00 +0800
tags: [AI]
description: "One sentence used for the list summary and SEO."
---
```

## Deployment

Push to `main`. The workflow in `.github/workflows/pages.yml` builds the site and deploys it to GitHub Pages.

## Content boundary

Only publishable material belongs here. No credentials, internal endpoints, customer data, or private workspace paths.

## Draft 与发布

未完成的文章用 `published: false`（Jekyll 只认这个字段；`draft: true` 是 Hugo 语法，无效）。发布前改成 `true` 或删掉该行。
