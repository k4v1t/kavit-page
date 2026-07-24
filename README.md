# Quarto personal website starter

A deliberately small Quarto website for visual essays on mathematics, AI, and science.

## 1. Replace the placeholders

Search the project for:

- `YOUR NAME`
- `YOUR_GITHUB_USERNAME`
- `YOUR_LINKEDIN_SLUG`

## 2. Install the tools on macOS

Install Quarto from the official installer and install VS Code plus the Quarto VS Code extension.

Confirm the installation:

```bash
quarto --version
```

## 3. Preview locally

From this project directory:

```bash
quarto preview
```

Quarto will render the site and open a local browser preview. Changes are reflected as files are saved.

## 4. Create the GitHub repository

Recommended repository name:

```text
personal-site
```

Then run:

```bash
git init
git add .
git commit -m "Create initial Quarto website"
git branch -M main
git remote add origin git@github.com:YOUR_GITHUB_USERNAME/personal-site.git
git push -u origin main
```

## 5. Publish to GitHub Pages

Run:

```bash
quarto publish gh-pages
```

For a project repository, the initial address will normally be:

```text
https://YOUR_GITHUB_USERNAME.github.io/personal-site/
```

The publish command creates and pushes the `gh-pages` branch. GitHub should detect it as the Pages source.

## 6. Add a custom domain later

Do not add a `CNAME` file yet. First purchase the domain, then configure it in the repository's **Settings → Pages** screen and add the required DNS records at the registrar.

## Content workflow

Each visual essay gets its own directory:

```text
posts/
  article-slug/
    index.qmd
    figures/
    data/
```

To add an essay, copy the existing `posts/high-dimensional-geometry` directory, rename it, and update the YAML metadata and content.

## Interactive graphics

The included essay uses Observable JS (`{ojs}` cells). Its sliders and plot run in the browser, which is suitable for GitHub Pages and does not require a live Python server.
