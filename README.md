
# Personal academic website

A Quarto website organized around research, teaching, software, talks, and posts, inspired by the structure of [James E. Pustejovsky's site](https://jepusto.com/) and [repository](https://github.com/jepusto/jepusto-quarto). Content and styling here are an original starter, not a copy of his work.

## Where to edit

| File or folder | Purpose |
| --- | --- |
| `_quarto.yml` | Site title, navigation, theme, and website address |
| `index.qmd` | Homepage, biography, education, and recent posts |
| `publications/index.qmd` | Research, publications, and ongoing projects |
| `teaching/index.qmd` | Courses and teaching materials |
| `software/index.qmd` | Software and research tools |
| `presentations/index.qmd` | Talks and workshops |
| `posts/` | One folder per post, each with an `index.qmd` |
| `cv.qmd`, `contact.qmd` | CV and contact information |
| `files/`, `img/` | Downloadable documents and images |
| `styles.css` | Visual styling |
| `docs/` | Generated website; do not edit by hand |

Quarto turns `.qmd` files (Markdown text with page settings) into HTML. GitHub stores the source and generated pages; GitHub Pages serves the generated website.

## Preview locally

Open `manchen.Rproj` in RStudio, open `index.qmd`, and click **Preview**. Alternatively, run `quarto preview` in a terminal.

If Quarto is not on your Windows PATH, this machine has an RStudio-bundled copy:

```powershell
& 'C:\Program Files\RStudio\resources\app\bin\quarto\bin\quarto.exe' preview
```

The launch website includes Home, Publications, Teaching, Software, Contact, and a CV download. `_quarto.yml` explicitly lists the six pages to render. Unfinished posts, talks, and internal editing guides remain in the repository but are excluded from the website.

## Publish with GitHub Pages

This starter uses Quarto's simple [render-to-docs publishing method](https://quarto.org/docs/publishing/github-pages.html#render-to-docs).

1. Run `quarto render` (or use the full Windows path above with `render` instead of `preview`).
2. Commit and push the source files **and `docs/`** to your GitHub repository using RStudio or GitHub Desktop. Review the changes before committing.
3. In the repository on GitHub, open **Settings > Pages**.
4. Choose **Deploy from a branch**, select **master** (the current branch in this checkout), and choose **/docs**. Save. If you later rename the branch, update this setting.
5. Check the deployment result in GitHub. The expected address is https://manchen07.github.io/manchen/.

After each edit, render again, then commit and push the updated source and `docs/` files. Publishing is not configured merely by creating these local files.

The existing `_config.yml` is an older Jekyll theme setting. Quarto uses `_quarto.yml`; the `.nojekyll` marker is copied into `docs/` to bypass Jekyll processing.

## Add a post

Create `posts/your-post-title/index.qmd` with this content:

```markdown
---
title: "Your post title"
date: 2026-10-22
categories: [Research]
description: "A one-sentence summary."
---

Write your post here.
```

Posts are not enabled in the launch website. Before enabling them, replace the sample welcome post, add the desired pages to `project.render` in `_quarto.yml`, and add navigation links. Keep accompanying images in the same post folder.

Rendering Contact requires R, knitr, rmarkdown, and leaflet. The contact map executes on each render. This project ignores `_freeze/`; GitHub Pages serves the already-rendered `docs/` files and does not execute R. Keep `_extensions/` in Git so the icon shortcodes work when rendering on another computer.
