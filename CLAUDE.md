# Claude Code Notes

This file contains important development guidelines and repository-specific information for Claude Code when working on this project.

## Repository Guidelines

### Git Workflow
- **Main branch is PROTECTED** - No direct pushes allowed
- **Always work on `development` branch** for changes
- **Create Pull Requests** from `development` → `main` for all changes
- Use `gh pr create` for creating PRs with proper descriptions

### Security & PII Guidelines
- **NEVER commit PII data** (Personal Identifiable Information)
  - No PDF files containing personal information
  - No files with real names in filenames
  - No contact information in plain text files
- **File exclusions:**
  - Avoid committing `*.pdf` files
  - Avoid committing `*:Zone.Identifier` files (Windows metadata)
  - Use generic filenames for any reference materials


## Project Structure

### Content Organization
- **Resume**: `/content/resume.md` - Main professional resume
  - Uses HTML `<details>/<summary>` tags for collapsible sections
- **Projects**: `/content/projects/` - Individual project files
  - Current: 10 projects (alfa.md through lima.md)
  - Future expansions: mike.md, november.md, oscar.md, papa.md, quebec.md, etc.
- **Contact**: `/content/contact.md` - Contact information page
- **Posts**: `/content/posts/` - Blog posts (currently minimal usage)
- **Configuration**: `config.toml` - Hugo site configuration


### Visual Design Patterns
- Use emojis for visual separation (📅 for dates, 🏆 for achievements)
- Font Awesome icons for technologies where available
- Clean spacing with manual line breaks for better text flow
- No bullet separators (•) - rely on icons/emojis for visual breaks

## Commands Reference

### Hugo Operations
```bash
# Local development
hugo server -D

# Build site (development)
hugo

# Build site (production)
hugo --minify --environment production
```

### Hugo Version Requirements
- **Local Development**: Hugo Extended version required (tested with 0.142.0+)
- **CI/CD Pipeline**: Uses Hugo Extended 0.148.2 with Dart Sass
- **Why Extended**: Required for SCSS processing and advanced features

### Theme Management (Git Submodule)
```bash
# Update theme to latest version
git submodule update --remote themes/hugo-coder

# Initialize submodules (if cloning fresh)
git submodule update --init --recursive
```

## Static Assets Management

### Logo Resources
- **Wikimedia Commons**: Good source for company logos in SVG format
- **Font Awesome**: Brand icons available for major tech companies
- Always check licensing before using external logos

### Asset Organization
- **Location**: `/static/images/` for all images
- **Required Images**: 
  - `avatar.jpg` - Profile picture
  - `favicon.svg` - Site favicon
- **Company Logos**: Adobe, Nutanix, Oracle (available in PNG and SVG formats)
- **Format Preferences**: SVG preferred for logos, JPG for photos

## Deployment & CI/CD

### GitHub Actions Workflow
- **File**: `/.github/workflows/hugo.yml`
- **Trigger**: Pushes to `main` branch + manual workflow dispatch
- **Hugo Version**: 0.148.2 Extended with Dart Sass
- **Build Command**: `hugo --minify` with `HUGO_ENVIRONMENT=production`
- **Deployment**: Automatic to GitHub Pages on successful build

### Legacy Systems
- CircleCI configuration exists (`/.circleci/config.yml`) but inactive
- HTMLProofer validation available in legacy CircleCI config

## Configuration Details

### Hugo Configuration (`config.toml`)
- **HTML Rendering**: `unsafe = true` (enables `<details>/<summary>` tags)
- **Color Scheme**: Auto-switching with toggle (`colorScheme = "auto"`)
- **Social Links**: GitHub, GitLab, LinkedIn, BlueSky configured
- **Theme**: `hugo-coder` (managed as git submodule)
- **Performance**: Minification enabled, sitemap generation, canonical URLs

### Theme Submodule
- **Repository**: `https://github.com/luizdepra/hugo-coder.git`
- **Location**: `/themes/hugo-coder`
- **Management**: Git submodule (update with commands above)

## Notes for Future Development
- Keep resume content sourced from official documents (referenced as `resumepdf`)
- Maintain consistent emoji/icon usage across sections
- Remember avatar config uses `avatarURL` not `avatar` in hugo-coder theme
- Repository name: `sumitb.github.io` (not `hugo-sumitb`)
- Public directory is generated content (should be in `.gitignore`)

---

*This file helps Claude Code maintain consistency and avoid common pitfalls when working on this repository.*