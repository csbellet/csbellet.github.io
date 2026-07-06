# clementbellet.com — source

A minimal static site (plain HTML/CSS, no build step, no framework). Content was drafted from the existing Google Sites page (sites.google.com/site/clementbellet) — review the wording before publishing.

## Structure

```
index.html          Home / bio / research focus / selected publications
publications.html   Full list of published papers + working papers
cv.html              CV summary + link to a downloadable PDF
teaching.html        Teaching history
media.html           Press mentions, op-eds, talks
contact.html         Contact details
assets/css/style.css Shared stylesheet (light + automatic dark mode)
assets/img/          Images (placeholder headshot included)
assets/cv/           Put your CV PDF here
```

## Before you publish — things to fill in

1. **Headshot**: done — `assets/img/headshot.jpg` is in place and linked from `index.html`.
2. **CV PDF**: done — `assets/cv/detailed_resume.pdf` is in place and linked from `cv.html`.
3. **Proofread bio/abstracts**: the text was drafted from your current Google Site; tweak tone/wording as you like.
4. **Working papers without links**: "Emotional Labor...", the meat-gender-gap paper, and the redistribution paper are marked "draft available upon request" — add SSRN/PDF links once available.

## Preview locally

No server needed — just open `index.html` directly in a browser, or run a tiny local server from this folder:

```bash
python3 -m http.server 8000
```

Then visit http://localhost:8000

## Deploying to GitHub Pages (once you have a GitHub account)

1. Create a GitHub account at github.com if you haven't already.
2. Create a new repository, e.g. `clementbellet.github.io` (using this exact `<username>.github.io` naming gives you a root URL) or any other name (e.g. `personal-site`, which will be served at `<username>.github.io/personal-site/`).
3. From this folder, initialize and push:
   ```bash
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/<username>/<repo-name>.git
   git push -u origin main
   ```
4. In the repo on GitHub: Settings → Pages → Source → Deploy from branch → `main` / `/ (root)`.
5. Your site will be live at `https://<username>.github.io/` (or `/<repo-name>/`) within a minute or two.
6. Optional: add a custom domain later via Settings → Pages → Custom domain (needs a domain you own, plus a DNS record pointing to GitHub Pages).

Come back to me when you've created the GitHub account/repo and I'll walk through the push and Pages setup with you.
