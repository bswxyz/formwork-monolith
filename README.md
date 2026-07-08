# Design studio / agency template — kinetic typography

**Live demo → https://bswxyz.github.io/fable-monolith/** · [How it was built](https://bswxyz.github.io/fable-monolith/guide/)

> A brutalist studio site carried entirely by type in motion: scrambling headlines, scroll-velocity skew, magnetic buttons.

A free, MIT-licensed website template. Good for: **design studios, motion agencies, freelancers with strong portfolios**.
The demo brand ("MONOLITH") is fictional — every word and colour is meant to be replaced with yours.

## The signature technique

- Text-scramble decoder effect on headlines (no plugins, ~20 lines)
- Scroll-velocity skew — the page tilts with fast scrolling and settles back
- Full-bleed hover wipe on the work list; magnetic CTA buttons

## Use this as your own site

This repo is a **template** — everything is plain HTML/CSS/JS with **relative paths**, so it
works under *any* repo name with zero configuration.

1. Click **Use this template → Create a new repository** (top of this page).
   **Name it whatever you like** — `my-site`, `portfolio`, anything.
2. In your new repo: **Settings → Pages → Build and deployment → Deploy from a branch**,
   then pick `main` / `/ (root)` and save. (CLI: see below.)
3. Wait ~1 minute. Your site is live at `https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/`.

<details>
<summary>Prefer the command line?</summary>

```bash
gh repo create my-site --template bswxyz/fable-monolith --public --clone
cd my-site
gh api --method POST /repos/YOUR-USERNAME/my-site/pages \
  -f 'source[branch]=main' -f 'source[path]=/'
```
</details>

No build step, no dependencies to install — edit the files, push, done.
The only external requests are Google Fonts and (where used) pinned CDN copies of GSAP/three.js.

## Customize it

- Accent colour: change `--accent` in `styles.css` (ships acid green `#c8ff00`)
- Headlines: edit the `data-scramble` lines in `index.html` — the effect adapts automatically
- Work list: each row is a simple `<li class="work-row">` — add yours

The `/guide/` page documents the signature technique in depth (with code) — keep it, rewrite it,
or delete the folder entirely.

## Files

```
index.html        the page
styles.css        all styling (design tokens in :root at the top)
main.js           the signature effect + motion
guide/index.html  how-it-works write-up (optional — yours to keep or delete)
```

## Built-in quality

- Works with JS disabled or a CDN failure (content is never permanently hidden)
- Respects `prefers-reduced-motion`; keyboard focus styles throughout
- Canvas/WebGL feature-detected with graceful fallbacks; devicePixelRatio capped for performance
- Responsive at phone / tablet / desktop widths

## License & credit

[MIT](LICENSE) — free for personal and commercial use, no attribution required
(a link back is always appreciated). Originally designed & built by **Fable**
(Anthropic's Claude) as part of a 25-template collection:
**[the full gallery →](https://bswxyz.github.io/fable-showcase/)**
