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
- **Projects**: `/content/projects/` - Individual project files
  - Use NATO phonetic alphabet naming: `alfa.md`, `bravo.md`, `charlie.md`, `delta.md`
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

# Build site
hugo
```

## Logo Resources
- **Wikimedia Commons**: Good source for company logos in SVG format
- **Font Awesome**: Brand icons available for major tech companies
- Always check licensing before using external logos

## Notes for Future Development
- Keep resume content sourced from official documents (referenced as `resumepdf`)
- Maintain consistent emoji/icon usage across sections
- Remember avatar config uses `avatarURL` not `avatar` in hugo-coder theme
- Projects section can expand using NATO phonetic alphabet (echo, foxtrot, golf, etc.)

---

*This file helps Claude Code maintain consistency and avoid common pitfalls when working on this repository.*