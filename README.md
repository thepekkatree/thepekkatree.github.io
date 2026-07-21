# Deepak Khatri — Portfolio

A single-file, zero-build personal portfolio. Just HTML/CSS/JS — nothing to compile, nothing to install.

## Files
- `index.html` — the entire site (styles + scripts inline).
- `.nojekyll` — tells GitHub Pages to serve files as-is (no Jekyll processing).
- `resume.pdf` — **add this yourself** (see below). The "Résumé" button links to it.
- `profile.png` — **add this yourself.** Your circular headshot (transparent background works best). Shown in the hero; the page hides it gracefully if missing.

## Add your résumé
Export your Overleaf resume as a PDF, rename it `resume.pdf`, and drop it in this folder next to `index.html`. The hero "📄 Résumé" button already points to `resume.pdf`.

## Deploy on GitHub Pages (2 minutes)

### Option A — user site (lives at `https://<username>.github.io`)
1. Create a **new public repo** named exactly `thepekkatree.github.io` (your GitHub username + `.github.io`).
2. Push these files to it:
   ```bash
   cd portfolio
   git init
   git add .
   git commit -m "Add portfolio"
   git branch -M main
   git remote add origin https://github.com/thepekkatree/thepekkatree.github.io.git
   git push -u origin main
   ```
3. Live in ~1 minute at **https://thepekkatree.github.io**.

### Option B — project site (lives at `https://thepekkatree.github.io/portfolio`)
1. Create any public repo (e.g. `portfolio`) and push these files (same commands as above, using remote `https://github.com/thepekkatree/portfolio.git`).
2. On GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: `main` / `root` → Save.**
3. Live in ~1 minute at the URL GitHub shows on that page.

## Customize
Everything is in `index.html`. Common edits:
- **Text/links** — search for the section (e.g. `<!-- EXPERIENCE -->`) and edit inline.
- **Colors** — the `:root { ... }` block at the top holds every color variable (`--teal`, `--turq`, `--accent`, backgrounds).
- **Sections** — each `<section>` is self-contained; delete or reorder freely.

## Custom domain (optional)
If you want it on a domain you own, add a `CNAME` file containing just the domain (e.g. `deepakkhatri.com`) and configure DNS per GitHub's Pages docs.
