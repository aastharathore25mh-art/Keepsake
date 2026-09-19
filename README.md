Keepsake
A single-file website: landing page, an interactive try-on app prototype, and a brand dashboard page. No build step, no dependencies — it's one self-contained `index.html`.
Run it locally
Just double-click `index.html`, or:
```
open index.html        # Mac
start index.html        # Windows
```
Put it on GitHub Pages (free hosting, real URL)
Create a new GitHub repo (e.g. `keepsake`).
Add `index.html` to the root of the repo and commit/push.
On GitHub: Settings → Pages → Source → Deploy from a branch, pick `main` and `/ (root)`, save.
Your live link appears at `https://<your-username>.github.io/<repo-name>/` within a minute or two.
Turn on real signups (brand + customer waitlist forms)
The site has two working forms — a customer waitlist on the Home page, and a "Request a pilot" form on the For Brands page — but they need a real inbox to send to, since GitHub Pages can't run backend code.
Go to formspree.io and create a free account.
Create a new form (name it anything, e.g. "Keepsake signups").
Formspree gives you an endpoint that looks like `https://formspree.io/f/abcd1234`. Copy it.
Open `index.html`, find the line near the bottom of the `<script>` that says:
```js
   const FORMSPREE\\\_ENDPOINT = "[https://formspree.io/f/YOUR\\\_FORM\\\_ID](https://formspree.io/f/xoevjqqo)";
   ```
and replace `YOUR\\\_FORM\\\_ID` with your real endpoint.
Commit and push the change — GitHub Pages redeploys automatically.
Submit the form once yourself to test it; Formspree will email you to confirm the form the first time.
Both forms post to the same endpoint — each submission includes a hidden `audience` field (`customer` or `brand`) so you can tell them apart in your Formspree inbox/dashboard. Free tier includes 50 submissions/month, which is enough to validate early interest before you need anything fancier.
Note on Google Colab
Colab runs Python notebooks, not static websites — it won't host or serve this file as a live page. Use GitHub Pages (above), or another static host like Netlify/Vercel, if you want a shareable link.
Structure
Everything — HTML, CSS, and JavaScript — lives in `index.html`. There's no backend: brand data, the try-on flow, the collection state, and the dashboard numbers are all defined in the `<script>` at the bottom of the file, so it's easy to edit brand names, colors, or copy directly in that one file.
