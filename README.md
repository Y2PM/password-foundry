# Password Foundry

Offline password / UUID / passphrase generator with a retro “hacker” UI, live clock, and a tiny robot cowboy with a tumbleweed.

## Run locally
Just open `index.html` in any modern browser. Everything runs offline.

## Deploy to GitHub Pages
1. Create a new repository on GitHub (any name, e.g. `password-foundry`).
2. Add the single file `index.html` (this file) at the repository root.
3. (Optional) add `README.md` — this very file.
4. Push to `main`.
5. In **Settings → Pages**, set: **Source = Deploy from a branch**, **Branch = main**, **Folder = / (root)**, then **Save**.
6. Wait ~1 minute; your site will be live at `https://<username>.github.io/<repo>/`.

### Using the Git CLI
```bash
git init
git add index.html README.md
git commit -m "Initial commit: Password Foundry"
git branch -M main
git remote add origin https://github.com/<username>/<repo>.git
git push -u origin main
```

### Custom domain (optional)
1. Buy / configure your domain’s DNS to add a CNAME record pointing `www.yourdomain.com` to `<username>.github.io`.
2. In **Settings → Pages → Custom domain**, enter `www.yourdomain.com` and enable **Enforce HTTPS**.
3. Add a `CNAME` file at the repo root containing exactly your domain (e.g., `www.yourdomain.com`) so the domain persists across redeploys.

## Notes
- No build step or frameworks required; one static HTML file is enough.
- Works offline; uses `crypto.getRandomValues` where available.
- Mobile optimisations included: larger tap targets, full‑width sliders, sticky header, and scaled animations.
