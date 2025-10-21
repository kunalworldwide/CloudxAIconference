This repository contains a minimal static frontend for a tech conference called CloudxAI.

Files added for the demo site:

- `site/` — the static site to publish (contains `index.html` and `css/style.css`).
- `.github/workflows/gh-pages.yml` — GitHub Actions workflow to publish `site/` to the `gh-pages` branch.

Run locally
-----------

You can serve the `site/` folder locally using Python's simple HTTP server (Python 3):

```bash
cd site
python3 -m http.server 8000
# then open http://localhost:8000 in a browser
```

Deploy to GitHub Pages
---------------------

1. Commit and push to the `main` branch. The Action will build and publish `site/` to the `gh-pages` branch.

```bash
git add site .github README.md
git commit -m "Add demo CloudxAI static site and Pages workflow"
git push origin main
```

2. After the Action runs (check Actions tab), go to your repository Settings → Pages and ensure the site is served from the `gh-pages` branch (root). The URL will be `https://<your-username>.github.io/<repo-name>/` unless you set a custom domain.

Notes
-----

- The workflow uses the default `GITHUB_TOKEN` so no secrets are needed.
- If you'd like the site at the repository root URL without `/repo-name`, enable GitHub Pages on the `gh-pages` branch or add a custom domain and CNAME.
# CloudxAIconference