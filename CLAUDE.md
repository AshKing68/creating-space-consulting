# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Hugo static site for Creating Space Consulting (creatingspaceconsulting.com) — a decluttering/organizing service. Uses the **Hextra** theme via git submodule.

## Common Commands

```bash
# Local development (serves drafts)
hugo server -D

# Production build
hugo --gc --minify --baseURL "https://creatingspaceconsulting.com/"

# Create new content
hugo new content/blog/my-post.md

# Initialize theme submodule (after fresh clone)
git submodule update --init --recursive
```

## Architecture

- **Content**: Markdown files with TOML front matter in `content/`. Pages: about, services, contact, blog.
- **Theme**: Hextra theme in `themes/hextra/` (git submodule — do not edit directly).
- **Config**: `hugo.toml` — site settings, menu structure, theme params.
- **CI/CD**: `.github/workflows/hugo.yaml` — builds with Hugo 0.157.0 extended and deploys to GitHub Pages on push to main.
- **Output**: `public/` is the generated build directory (gitignored).

## Notes

- All content pages are currently in **draft** status (`draft = true`). Use `-D` flag when serving locally to see them.
- Hugo extended version is required (for SCSS/asset processing in Hextra theme).
