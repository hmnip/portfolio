# Deploying to GitHub Pages

The site is static HTML, CSS, and JS with no build step. GitHub Pages serves it straight from the root of the `main` branch. `.nojekyll` in the root tells Pages to skip Jekyll and serve files as they are.

All commands are for **PowerShell**, run from the portfolio folder. Replace `<USER>` with your GitHub username and `<REPO>` with the repository name.

## 0. Pick a repository name

| Repo name | Site URL | Notes |
|---|---|---|
| `<USER>.github.io` | `https://<USER>.github.io/` | Your main personal site. Only one per account. |
| anything else, e.g. `portfolio` | `https://<USER>.github.io/portfolio/` | Works the same. All links are relative, and `404.html` detects the `/portfolio/` prefix. |

GitHub Pages is free for **public** repositories. Private repos need a paid plan.

## 1. Check the tools

```powershell
git --version
gh --version
gh auth status
```

If `gh auth status` says you're not logged in, run `gh auth login`, choose GitHub.com, HTTPS, and log in with a web browser.

## 2. First commit

```powershell
git add -A
git status
git commit -m "Initial portfolio site"
```

Read the `git status` output before committing. Nothing private should be in the list.

## 3. Create the repository and push

```powershell
gh repo create <REPO> --public --source . --remote origin --push --description "Engineering portfolio"
```

This creates the repo on your account, adds it as `origin`, and pushes `main`.

## 4. Turn on GitHub Pages (main branch, root folder)

```powershell
gh api -X POST "repos/<USER>/<REPO>/pages" -f "source[branch]=main" -f "source[path]=/"
```

Or in the browser: repo **Settings > Pages > Build and deployment > Deploy from a branch**, branch `main`, folder `/ (root)`, **Save**.

## 5. Check that it's live

```powershell
gh api "repos/<USER>/<REPO>/pages" --jq ".html_url, .status"
gh api "repos/<USER>/<REPO>/pages/builds/latest" --jq ".status"
```

The first build takes 1 to 3 minutes. When the build says `built`, open the URL.

## 6. After the first deploy

Sharing previews (LinkedIn, Slack, iMessage) need full URLs. Once you know the live URL:

1. In every page's `<head>`, change `og:image` and `twitter:image` from `assets/img/share.png` (or `../assets/img/share.png`) to `https://<your-site>/assets/img/share.png`.
2. Add `<meta property="og:url" content="https://<your-site>/<page>">` to each page.
3. In `index.html`, add `"url": "https://<your-site>/"` to the JSON-LD block, and your GitHub profile to `"sameAs"`.

Then commit and push (step 7). You can check a preview with LinkedIn's Post Inspector: https://www.linkedin.com/post-inspector/

## 7. Updating the site later

```powershell
git add -A
git commit -m "Describe the change"
git push
```

Pages rebuilds on every push to `main`, usually within a minute or two.

## 8. Optional: custom domain

Buy a domain from any registrar, for example `phoenixp.dev`.

**DNS records** (at your registrar):

| Type | Host | Value |
|---|---|---|
| A | `@` | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |
| AAAA | `@` | `2606:50c0:8000::153` |
| AAAA | `@` | `2606:50c0:8001::153` |
| AAAA | `@` | `2606:50c0:8002::153` |
| AAAA | `@` | `2606:50c0:8003::153` |
| CNAME | `www` | `<USER>.github.io` |

**Tell GitHub about the domain:**

```powershell
Set-Content -Path CNAME -Value "phoenixp.dev" -NoNewline -Encoding ascii
git add CNAME
git commit -m "Add custom domain"
git push
gh api -X PUT "repos/<USER>/<REPO>/pages" -f "cname=phoenixp.dev"
```

DNS can take up to 24 hours. When the certificate is ready, turn on HTTPS:

```powershell
gh api -X PUT "repos/<USER>/<REPO>/pages" -F "https_enforced=true"
```

Also verify the domain under your GitHub account's **Settings > Pages > Verified domains**, so nobody else can claim it.

Then update the absolute URLs from step 6 to the new domain.

## Troubleshooting

| Symptom | Fix |
|---|---|
| 404 right after enabling Pages | Wait a few minutes for the first build, then hard-refresh (Ctrl+F5). |
| A page works locally but 404s online | File names are case-sensitive on Pages. `Bear-Den.html` and `bear-den.html` are different files. |
| Styles missing online | A path probably starts with `/`. Keep paths relative (`assets/...` or `../assets/...`). |
| Old version still showing | Hard-refresh, or wait for the build: `gh api "repos/<USER>/<REPO>/pages/builds/latest" --jq ".status"`. |
| Build fails | Check the repo's **Actions** tab for the "pages build and deployment" run. |

## Note on public files

Everything in the repo is public, including `docs/` (this file, the media checklist, and the style guide). The style guide has `noindex`, so search engines skip it, but anyone with the link can open it.
