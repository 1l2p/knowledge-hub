# Knowledge Hub — GitHub Pages Site

This folder contains the source for the Knowledge Hub wiki, built with [Jekyll](https://jekyllrb.com) and the [Just the Docs](https://just-the-docs.com) theme, ready to publish on GitHub Pages.

## Deploying to GitHub Pages

1. Create a new GitHub repository (e.g. `knowledge-hub`)
2. Upload the contents of this `wiki-github/` folder as the root of the repository
3. In the repository **Settings → Pages**, set:
   - **Source:** `Deploy from a branch`
   - **Branch:** `main` (or `master`), folder `/` (root)
4. GitHub will build and publish the site automatically — the URL will appear in Settings → Pages once the build completes (usually 1–2 minutes)

## Previewing Locally

Requires Ruby ≥ 3.1 and Bundler.

```bash
# From the wiki-github/ directory:
bundle install
bundle exec jekyll serve
# Open http://localhost:4000
```

## Updating Content

All content lives in the `.md` files. Each file begins with a YAML front matter block (between `---` lines) that controls the title and navigation. To update a page, edit the markdown below the front matter and push to GitHub — the site rebuilds automatically.

To add a new page, copy an existing `.md` file, update the front matter (`title`, `nav_order`, and optionally `parent`), and add your content.

## Site Structure

| File | Section | Description |
|------|---------|-------------|
| `index.md` | Home | Landing page and overview |
| `core-topics.md` | Core Topics | Section parent |
| `academic-readiness-and-course-design.md` | Core Topics | |
| `student-support-belonging-persistence.md` | Core Topics | |
| `credentials-pathways-labor-market.md` | Core Topics | |
| `workforce-development-career-navigation.md` | Core Topics | |
| `learning-analytics-institutional-operations.md` | Core Topics | |
| `analysis.md` | Cross-Cutting Analysis | Section parent |
| `cross-cutting-themes.md` | Cross-Cutting Analysis | |
| `overlooked-opportunities.md` | Cross-Cutting Analysis | |
| `document-registry.md` | Reference | |
