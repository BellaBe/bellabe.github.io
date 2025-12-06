# bellabe.github.io

Personal blog and technical tutorials.

## Structure

```
├── _config.yml          # Site configuration
├── _layouts/            # Page templates
│   ├── default.html     # Base layout
│   └── post.html        # Post/tutorial layout
├── _posts/              # Blog posts (YYYY-MM-DD-title.md)
├── assets/css/          # Stylesheets
├── index.html           # Home page
└── tutorials.html       # Tutorials listing
```

## Writing a Post

Create a new file in `_posts/` with the format `YYYY-MM-DD-title.md`:

```yaml
---
layout: post
title: "Your Post Title"
date: 2025-12-06
description: "Brief description for SEO and listings"
reading_time: 10
tags: [tutorial, claude, ai]
leanos_ref: ".claude/skills"  # Optional: link to LeanOS code
---

Your content here...
```

## Local Development

```bash
# Install Jekyll
gem install bundler jekyll

# Run locally
bundle exec jekyll serve

# View at http://localhost:4000
```

## Deployment

Push to `master` branch. GitHub Pages builds automatically.

## Links

- [LeanOS](https://github.com/BellaBe/lean-os)
- [LinkedIn](https://www.linkedin.com/in/bellabelgarokova/)
