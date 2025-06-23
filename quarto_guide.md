# Quarto Documentation Guide

This guide explains how to edit, preview, render, and publish the documentation site using [Quarto](https://quarto.org).

---

## 1. Setup

If Quarto is not installed, run:

```bash
wget https://quarto.org/download/latest/quarto-linux-amd64.deb
sudo apt install ./quarto-linux-amd64.deb
```

To check the installation:

```bash
quarto --version
```

---

## 2. Editing Content

Site content is written in `.qmd` files:

- `index.qmd`: Main landing page
- `about.qmd`: Information about the team or organisation
- `navigation/*.qmd`: Technical documentation pages

Use standard Markdown with optional LaTeX-style math and code blocks.

---

## 3. Preview the Site

To live-preview the site locally as you edit:

```bash
quarto preview
```

This starts a local server (usually at http://localhost:4200) and refreshes automatically when files are saved.

---

## 4. Render the Site

To build the static site into the `_site/` directory:

```bash
quarto render
```

This creates the final HTML version of the site locally.

---

## 5. Publish to GitHub Pages

To deploy the site to GitHub Pages (`gh-pages` branch):

```bash
quarto publish gh-pages
```

When prompted, confirm with `Y`.

Live site URL:
```
https://prograde-systems.github.io
```

---

## 6. Repository Cleanliness

The following should be excluded from version control via `.gitignore`:

```
_site/
.quarto/
*.deb
```

Only commit source files like `.qmd`, `.css`, `_quarto.yml`, and assets (e.g. images, diagrams).

---

## Further Resources

- Quarto Docs: https://quarto.org/docs/
- Markdown Reference: https://quarto.org/docs/authoring/markdown-basics.html
- Math and Equations: https://quarto.org/docs/authoring/markdown-basics.html#equations
