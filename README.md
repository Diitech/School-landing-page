# School-landing-page

A responsive static school landing page template.

## Local preview

```bash
python3 -m http.server 4173
```

Open `http://localhost:4173`.

## Deployment (GitHub Pages)

This repository includes a GitHub Actions workflow at `.github/workflows/deploy.yml`.

### One-time setup
1. Push this repository to GitHub.
2. In GitHub, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to **GitHub Actions**.

### Automatic deploys
- Every push to `main`, `master`, or `work` triggers deployment.
- You can also run deployment manually from the **Actions** tab via **workflow_dispatch**.

After a successful run, your site will be available at your Pages URL.
