# Marius Varhaugvik — static site

Pre-built portfolio for Netlify. Push this folder to GitHub and connect the repo in Netlify.

## Deploy

1. Create a new empty repo on GitHub (no README/license — keeps first push simple).
2. From this folder:

```bash
git init
git add .
git commit -m "Initial static export"
git branch -M main
git remote add origin git@github.com:YOUR_USER/YOUR_REPO.git
git push -u origin main
```

3. In [Netlify](https://app.netlify.com): **Add new site → Import from Git** → pick the repo.
4. Netlify should detect `netlify.toml` automatically:
   - **Publish directory:** `.` (repo root)
   - **Build command:** leave empty (site is pre-built)
5. Deploy.

## Contents

- 48 static pages (home, about, 42 projects)
- 343 media files in `uploads/` (images + audio)
- Hover audio preview on project grid (desktop)

## Updating the site

When content changes in the CMS source project:

1. Re-run `npm run build:static` in `marius-website/marius-web` (Strapi must be running).
2. Copy the new `out/` folder into this repo and commit.

Built from `marius-website` on 2026-08-19.
