# Agamos website

Plain HTML/CSS, no build step. Open `index.html` in a browser to preview.

## Files
- `index.html` — home: hero, featured episode, Season 1 episode grid, about teaser, casting call
- `about.html` — about the show and the team (look for `EDIT ME` comments)
- `styles.css` — all styling
- `assets/` — logo and episode thumbnails

## Editing
- New episode: copy one `<li class="ep">` block in `index.html`, change the video ID, title, and duration, and drop a thumbnail in `assets/` (`https://i.ytimg.com/vi/VIDEO_ID/hqdefault.jpg`).
- Casting link: search for `Apply on Instagram` and swap the href for your Google Form or Typeform URL.
- Team bios: `about.html`, the "people behind it" section.

## Deploy (GitHub Pages, free)
1. Create a GitHub account if you don't have one, then create a new **public** repo called `agamos-site`.
2. In this folder:
   ```
   git add -A
   git commit -m "Agamos site"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/agamos-site.git
   git push -u origin main
   ```
3. On GitHub: repo → Settings → Pages → Source: "Deploy from a branch" → Branch: `main` / root → Save.
4. In a minute the site is live at `https://YOUR_USERNAME.github.io/agamos-site/`.

## Custom domain (agamos.tv)
1. Buy the domain (Cloudflare Registrar or Namecheap; .tv is roughly $30–40/yr).
2. Create a file named `CNAME` in this folder containing one line: `agamos.tv`, commit and push.
3. At your registrar add DNS records:
   - `A` records for `@` → `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - `CNAME` for `www` → `YOUR_USERNAME.github.io`
4. GitHub → Settings → Pages → Custom domain: `agamos.tv` → check "Enforce HTTPS" once it verifies.
