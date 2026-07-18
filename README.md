<img src="assets/favicon.svg" width="32" height="32" align="left" alt=""> re:wake.org

Landing page for re:wake — small, focused tools that do one thing and do it right. Plain HTML/CSS, no build step, deployed via GitHub Pages.

## Mission

Software that does one thing. And does it right.

Modern tools have gotten crowded. re:wake builds single-purpose, lightweight web utilities designed to solve a single problem efficiently, without the bloat.

## Design principles

- **One job per tool.** Each re:wake project solves a single problem. If a feature doesn't serve that one job, it doesn't ship.
- **No accounts, no lock-in.** Nothing requires sign-up unless the problem itself demands it (e.g. saving user data).
- **Lightweight by default.** No frameworks or dependencies unless they earn their weight. Fast load times over convenience.
- **Get out of the way.** The tool should be obvious to use without a manual, and disappear once the job is done.

## Branding

- **Wordmark:** `re:wake`, always lowercase. The colon is the brand mark — style it in the accent color while `re` and `wake` stay in the body text color.
- **Colors:**
  | Token | Value | Use |
  |---|---|---|
  | `--bg` | `#fafaf9` | Page background |
  | `--fg` | `#1c1c1a` | Body text, wordmark |
  | `--muted` | `#6b6b66` | Secondary text |
  | `--accent` | `#d4552b` | Colon, links, "Visit" links |
  | `--border` | `#e5e4e0` | Card and divider borders |

  Defined as CSS custom properties in `css/style.css` — change the theme in one place.
- **Typography:** system font stack (no web fonts), keeps pages fast and dependency-free.
- **Favicon:** the re:wake colon, rendered as two accent-colored dots on a light rounded tile (`assets/favicon.svg`) — the brand mark distilled to its simplest form, legible even at 16×16.
- **Badge:** `assets/badge.svg` — an "a project of re:wake" badge for individual project READMEs to link back here.

  ![part of: re:wake](assets/badge.svg)
- **Tone:** direct, unfussy, a little wry about software bloat. Short sentences over marketing copy.

## Local preview

Just open `index.html` in a browser, or serve it locally:

```
python -m http.server
```

## Adding a new project

Copy this block into the `.project-grid` in `index.html`, fill in the details, and commit:

```html
<article class="project-card">
  <h3><a href="https://example.rewake.org">Project Name</a></h3>
  <p>One-sentence description of what it does.</p>
  <div class="card-links">
    <a class="visit-link" href="https://example.rewake.org">Visit →</a>
    <a class="source-link" href="https://github.com/Mozzo1000/repo-name">Source</a>
  </div>
</article>
```

## Deployment

GitHub Pages is configured to serve from the root of the `main` branch, using the custom domain in `CNAME` (`rewake.org`). Make sure your DNS points at GitHub Pages if it doesn't already. `.nojekyll` disables Jekyll processing since this site doesn't need it.
