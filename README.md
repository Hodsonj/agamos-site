# agamos.tv

Single-page static site, no build step. Open `index.html` in a browser to preview.

- `index.html` — the whole site: animated colonnade intro, seasons rail, Season 1 episodes, Season 2 casting
- `assets/` — logo vectors (`wordmark.svg`, `mark.svg`), episode thumbnails, photos
- `CNAME` — custom domain for GitHub Pages

## Editing
- Episode: copy an `<a class="ep">` block, change the video ID, title, duration, and add a thumbnail (`https://i.ytimg.com/vi/VIDEO_ID/hqdefault.jpg`).
- Casting link: search for `Apply on Instagram` and swap the href.
- Intro timing: the animation variables at the top of the stylesheet (`--cd`, `--vd`, `--gd`, `--j`).

## Deploy
```
git add -A && git commit -m "update" && git push
```
GitHub Pages serves `main` at https://agamos.tv within about a minute.
