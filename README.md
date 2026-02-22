# Rangefinder - Hugo Photography Blog

A minimal, dark-themed photography blog built with Hugo. Inspired by rangefinder cameras.

## Quick Start

1. **Install Hugo** (extended version recommended):
   - macOS: `brew install hugo`
   - Windows: `choco install hugo-extended`
   - Or download from https://gohugo.io/installation/

2. **Run the dev server:**
   ```bash
   cd rangefinder-site
   hugo server -D
   ```
   Open http://localhost:1313 in your browser.

3. **Build for production:**
   ```bash
   hugo
   ```
   Output goes to the `public/` folder -- deploy that anywhere.

## Creating a New Post

```bash
hugo new posts/my-new-post.md
```

This creates a post from the template in `archetypes/posts.md`. Edit the front matter:

```yaml
---
title: "My New Post"
date: 2026-02-20
excerpt: "A short description for the gallery card."
cover_image: "/images/my-photo.jpg"
draft: false
exif:
  focal_length: "35mm"
  aperture: "f/2.0"
  shutter_speed: "1/250s"
---

Your post content here in Markdown...
```

## Adding Your Own Photos

Drop images into the `static/images/` folder. Reference them in posts as `/images/filename.jpg`.

For Unsplash or external images, use the full URL in `cover_image`.

## Project Structure

```
rangefinder-site/
  archetypes/       -- Templates for new content
  content/posts/    -- Your blog posts (Markdown)
  layouts/          -- HTML templates
  static/css/       -- Stylesheet
  static/images/    -- Your photos
  hugo.toml         -- Site configuration
```

## Deploying

### GitHub Pages
1. Push this repo to GitHub
2. Add a GitHub Action to build Hugo (see hugo docs for the workflow file)
3. Enable Pages in repo settings

### Netlify
1. Push to GitHub/GitLab
2. Connect repo in Netlify
3. Build command: `hugo`
4. Publish directory: `public`

### Vercel
1. Push to GitHub
2. Import in Vercel
3. Framework preset: Hugo
