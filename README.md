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

> Note: The workflow uses `actions/configure-pages@v5` with `enablement: true` to auto-enable Pages when possible. If your org/repo policy blocks automatic enablement, enable Pages once in repository settings and rerun the workflow.

### Automatic deploys
- Every push to `main`, `master`, or `work` triggers deployment.
- You can also run deployment manually from the **Actions** tab via **workflow_dispatch**.

After a successful run, your site will be available at your Pages URL.


## Deployment to other platforms

In addition to GitHub Pages, this repo now includes workflows for:
- **Netlify**: `.github/workflows/deploy-netlify.yml`
- **Vercel**: `.github/workflows/deploy-vercel.yml`
- **Cloudflare Pages**: `.github/workflows/deploy-cloudflare-pages.yml`

Each workflow triggers on push to `main`, `master`, or `work`, and also supports manual runs via `workflow_dispatch`.

### Required GitHub Secrets

Set only the secrets for the platform(s) you want to use:

#### Netlify
- `NETLIFY_AUTH_TOKEN`
- `NETLIFY_SITE_ID`

#### Vercel
- `VERCEL_TOKEN`
- `VERCEL_ORG_ID`
- `VERCEL_PROJECT_ID`

#### Cloudflare Pages
- `CLOUDFLARE_API_TOKEN`
- `CLOUDFLARE_ACCOUNT_ID`
- `CLOUDFLARE_PAGES_PROJECT_NAME`

> If a platform's secrets are missing, that platform's workflow will fail. You can disable unused workflows in the Actions tab or remove the workflow file.
