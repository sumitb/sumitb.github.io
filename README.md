# hugo-sumitb

[![Deploy Hugo site to Pages](https://github.com/sumitb/hugo-sumitb/actions/workflows/hugo.yml/badge.svg)](https://github.com/sumitb/hugo-sumitb/actions/workflows/hugo.yml)

Hugo source code repository for [sumitb.github.io](https://sumitb.github.io)

## Repository Workflow

This repository contains the Hugo source code and automated deployment. The workflow is:

1. **Development** → `hugo-sumitb` (this repo)
   - Contains Hugo source files, themes, content, and configuration
   - Uses `hugo-coder` theme as git submodule for easy updates

2. **CI/CD** → GitHub Actions
   - Automatically triggered on push to main branch
   - Builds the static site using Hugo 0.148.2 (Extended)
   - Deploys directly to GitHub Pages from this repository

3. **Live Site** → [https://sumitb.github.io](https://sumitb.github.io)
   - Served directly from this repository via GitHub Pages
   - No separate production repository needed

## Development Process

All development happens on the `development` branch:

1. **Make changes** on `development` branch
2. **Create Pull Request** to `main` branch  
3. **Merge PR** triggers automatic deployment via GitHub Actions
4. **Site updates** live at https://sumitb.github.io

## Configuration Notes

### Unsafe HTML Enabled
This site has `unsafe = true` enabled in `config.toml` under `[markup.goldmark.renderer]` to support collapsible resume sections using HTML `<details>` and `<summary>` tags. This allows for clean, interactive experience sections without custom CSS.

### Theme Updates

The hugo-coder theme is configured as a git submodule. To update to the latest version:

```bash
git submodule update --remote themes/hugo-coder
git commit -am "Update hugo-coder theme to latest version"
```

## Manual Deployment

You can manually trigger deployment using GitHub's web interface:
- Go to [Actions tab](https://github.com/sumitb/hugo-sumitb/actions/workflows/hugo.yml)
- Click "Run workflow" button