# Creating Space Consulting

Website for [Creating Space Consulting](https://creatingspaceconsulting.com/) — a compassionate, guided approach to releasing belongings.

Built with [Hugo](https://gohugo.io/) using the [Hextra](https://github.com/imfing/hextra) theme.

## Prerequisites

- [Hugo](https://gohugo.io/installation/) (extended version, v0.157.0+)
- Git

## Getting Started

```bash
# Clone with theme submodule
git clone --recurse-submodules https://github.com/AshKing68/creating-space-consulting.git
cd creating-space-consulting

# If already cloned without submodules
git submodule update --init --recursive

# Start local dev server (includes draft content)
hugo server -D
```

The site will be available at http://localhost:1313/.

## Project Structure

```
content/          # Markdown pages and blog posts
themes/hextra/    # Hextra theme (git submodule)
hugo.toml         # Site configuration
.github/workflows # CI/CD for GitHub Pages deployment
```

## Deployment

Pushes to `main` automatically build and deploy to GitHub Pages via the workflow in `.github/workflows/hugo.yaml`.

To build locally:

```bash
hugo --gc --minify
```

Output is generated in the `public/` directory.
