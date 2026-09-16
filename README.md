# Keepsake

A single-file website: landing page, an interactive try-on app prototype, and a brand dashboard page. No build step, no dependencies — it's one self-contained `index.html`.

## Run it locally
Just double-click `index.html`, or:
```
open index.html        # Mac
start index.html        # Windows
```

## Put it on GitHub Pages (free hosting, real URL)
1. Create a new GitHub repo (e.g. `keepsake`).
2. Add `index.html` to the root of the repo and commit/push.
3. On GitHub: **Settings → Pages → Source → Deploy from a branch**, pick `main` and `/ (root)`, save.
4. Your live link appears at `https://<your-username>.github.io/<repo-name>/` within a minute or two.

## Note on Google Colab
Colab runs Python notebooks, not static websites — it won't host or serve this file as a live page. Use GitHub Pages (above), or another static host like Netlify/Vercel, if you want a shareable link.

## Structure
Everything — HTML, CSS, and JavaScript — lives in `index.html`. There's no backend: brand data, the try-on flow, the collection state, and the dashboard numbers are all defined in the `<script>` at the bottom of the file, so it's easy to edit brand names, colors, or copy directly in that one file.
