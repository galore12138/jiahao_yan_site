# Updating the website

Most updates can be made directly on GitHub by opening a file, clicking the pencil icon, and committing the change.

## Add or update a paper

Edit `data/papers.yaml`. Copy an existing entry and update its fields:

```yaml
- title: "Paper title"
  authors: "Jiahao Yan and Coauthor Name"
  year: 2026
  status: "working paper"
  venue: ""
  description: "One-sentence description."
  pdf: "files/paper-name.pdf"
  link: ""
```

Upload the PDF to `static/files/`. Use one of these status values: `working paper`, `under review`, `published`, or `conference paper`.

To mark a paper as published, change `status` to `published` and add the journal or book information to `venue`.

## Update the bio

Edit `content/_index.md`. The text below the front matter is the About section.

The short tagline, role, institution, and email are in `hugo.yaml`.

## Add experience or education

Edit `data/teaching.yaml` for student-support or teaching experience. Edit `data/education.yaml` for degrees.

## Add an award

Edit `data/awards.yaml` and copy an existing entry.

## Replace the CV

Replace `static/files/jiahao-yan-cv.pdf` with the new PDF and keep the same filename.

## Change the photo

Replace `static/images/photo.jpg` with the new image and keep the same filename.

## Add a blog later

Create `content/blog/your-post-name/index.md`:

```markdown
---
title: "Post title"
date: 2026-06-23
description: "One-sentence summary."
tags: ["research"]
---

Write the post here.
```

Blog templates and navigation can then be enabled when there is a first post.

## Preview before publishing

Run:

```powershell
.\.tools\hugo\hugo.exe server --disableFastRender
```

Open <http://localhost:1313/jiahao_yan_site/>. Stop the preview with `Ctrl+C`.

## Publishing

Pushing to `main` triggers the GitHub Actions workflow. GitHub Pages must be set to use **GitHub Actions** under repository **Settings → Pages**. After that, updates usually appear within a few minutes.

