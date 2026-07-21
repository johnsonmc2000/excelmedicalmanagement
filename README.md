# Excel Medical Management — Website

Static site for Excel Medical Management (EMM), a medical billing and revenue cycle management company. Plain HTML/CSS, no build tools, no frameworks — ready to publish directly to GitHub Pages.

## Files

- `index.html` — homepage (hero, services, about, contact)
- `privacy-policy.html` — HIPAA-aware privacy policy
- `terms-of-service.html` — terms of service
- `CNAME` — custom domain file for GitHub Pages (`excelmedicalmanagement.com`)

## Publishing to GitHub Pages

1. Create a new GitHub repository (e.g. `excel-medical-management-site`).
2. Push these files to the repo's default branch (e.g. `main`):
   ```bash
   git init
   git add .
   git commit -m "Initial EMM website"
   git branch -M main
   git remote add origin <your-repo-url>
   git push -u origin main
   ```
3. In the repo, go to **Settings → Pages**.
4. Under **Build and deployment**, set **Source** to `Deploy from a branch`, branch `main`, folder `/ (root)`.
5. Under **Custom domain**, enter `excelmedicalmanagement.com` and save (this matches the included `CNAME` file, so GitHub should detect it automatically).
6. At your domain registrar/DNS provider, point the domain to GitHub Pages:
   - Add an `A` record (or `ALIAS`/`ANAME` for the apex domain) pointing to GitHub Pages' IP addresses (see GitHub's current [Pages custom domain docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site) for the current IPs), **or**
   - If using `www.excelmedicalmanagement.com`, add a `CNAME` record pointing to `<username>.github.io`.
7. Wait for DNS to propagate, then enable **Enforce HTTPS** in the Pages settings once the certificate is issued.

## Placeholders to fill in before launch

Search the HTML for `[BRACKETED]` text — these are the spots that need real information from Mark:

- **Phone number** — homepage contact section (`index.html`)
- **Business address** — homepage contact section (`index.html`)
- **Privacy Policy effective date** (`privacy-policy.html`)
- **Terms of Service effective date and governing-law state** (`terms-of-service.html`)

No other content changes are required to publish.
