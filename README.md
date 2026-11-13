# Phoenix Pitaknarongphorn: Engineering Portfolio

Static portfolio site. Plain HTML, CSS, and vanilla JavaScript. No build step and no dependencies.
It deploys to GitHub Pages from the root of the `main` branch.

## Structure

```
index.html                 Home
404.html                   Custom 404
projects/<slug>.html       Case studies (one per project)
assets/css/style.css       Design tokens and all components
assets/js/main.js          Theme toggle, mobile nav, scroll reveal
assets/img/<project>/      WebP images
assets/video/<project>/    Short muted looping MP4s
assets/cad/<project>/      CAD renders
docs/styleguide.html       Component reference (not linked from the site, set to noindex)
docs/MEDIA_CHECKLIST.md    Every media placeholder and the shot it needs
docs/DEPLOY.md             How to publish
```

## Preview locally (PowerShell)

Any static server works. With Node installed:

```powershell
npx --yes serve .
```

Then open the URL it prints.

## Editing rules

- All colors, fonts, and spacing are CSS custom properties at the top of `assets/css/style.css`.
- Use relative paths everywhere so the site works at `username.github.io/repo` and on a custom domain.
- Missing facts are marked `[TODO: ...]` in the page. Search the repo for `TODO` to find them all.
