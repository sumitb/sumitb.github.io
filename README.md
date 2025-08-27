# hugo-sumitb

[![CircleCI](https://circleci.com/gh/sumitb/sumitb.github.io.svg?style=shield)](https://circleci.com/gh/circleci/circleci-docs)
[![codecov](https://codecov.io/gh/sumitb/sumitb.github.io/branch/main/graph/badge.svg?token=2HFMG4Q2AM)](https://codecov.io/gh/sumitb/sumitb.github.io)

Hugo source code repository for [sumitb.github.io](https://sumitb.github.io)

## Repository Workflow

This repository contains the Hugo source code and acts as the development repository. The deployment workflow is:

1. **Development** → `hugo-sumitb` (this repo)
   - Contains Hugo source files, themes, content, and configuration
   - Uses `hugo-coder` theme as git submodule for easy updates

2. **CI/CD** → CircleCI webhook
   - Automatically triggered on push to main branch
   - Builds the static site using Hugo
   - Runs tests and generates coverage reports

3. **Production** → [`sumitb.github.io`](https://github.com/sumitb/sumitb.github.io)
   - Receives the generated static HTML/CSS/JS files from CircleCI
   - Serves the live website via GitHub Pages

4. **Live Site** → [https://sumitb.github.io](https://sumitb.github.io)

## Theme Updates

The hugo-coder theme is configured as a git submodule. To update to the latest version:

```bash
git submodule update --remote themes/hugo-coder
git commit -am "Update hugo-coder theme to latest version"
```
