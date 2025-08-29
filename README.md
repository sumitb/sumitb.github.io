# Personal Website - sumitb.github.io

[![Deploy Hugo site to Pages](https://github.com/sumitb/sumitb.github.io/actions/workflows/hugo.yml/badge.svg)](https://github.com/sumitb/sumitb.github.io/actions/workflows/hugo.yml)

Hugo-powered personal website and portfolio showcasing professional experience, projects, and technical expertise.

🌐 **Live Site**: [https://sumitb.github.io](https://sumitb.github.io)

## About

This is a professional portfolio website built with Hugo static site generator, featuring:

- **Professional Resume** - Comprehensive career history with interactive collapsible sections
- **Project Portfolio** - 10+ technical projects spanning distributed systems, security, and mobile development
- **Clean Design** - Modern, responsive design with dark/light mode toggle
- **Performance Optimized** - Fast loading static site with optimized assets

## Key Sections

- 📄 **Resume** - Professional experience, education, and achievements
- 🚀 **Projects** - Technical projects with detailed descriptions and technologies used
- 📞 **Contact** - Professional contact information and social media links
- 📝 **Blog** - Technical writing and insights (expandable section)

## Technology Stack

- **Framework**: Hugo Static Site Generator
- **Theme**: [hugo-coder](https://github.com/luizdepra/hugo-coder) 
- **Deployment**: GitHub Pages with GitHub Actions
- **Features**: Responsive design, SEO optimized, dark/light mode

## Development

### Local Development

```bash
# Start local development server
hugo server -D

# View at http://localhost:1313
```

### Requirements

- Hugo Extended version (0.142.0+)
- Git (for theme submodule management)

### Content Organization

- Resume: `/content/resume.md`
- Projects: `/content/projects/` (NATO phonetic naming: alfa.md, bravo.md, etc.)
- Contact: `/content/contact.md`
- Configuration: `config.toml`

## Deployment

The site automatically deploys to GitHub Pages when changes are pushed to the `main` branch. 

**Workflow**: 
1. Develop on `development` branch
2. Create Pull Request to `main`
3. Merge triggers automatic deployment
4. Site updates live within minutes

---

*This repository contains the source code for the personal website. For development guidelines and detailed documentation, see CLAUDE.md.*