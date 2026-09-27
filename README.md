# Zenex Exports website

Static HTML website for Zenex Exports — Premium Granite Exporters.

## Preview locally

Run `python3 -m http.server 8000` from this directory, then open `http://localhost:8000`.

## Publish with GitHub Pages

1. Create a GitHub repository and upload this project at the repository root.
2. Push to the `main` branch.
3. In GitHub, open **Settings → Pages** and set Source to **GitHub Actions**.
4. The workflow at `.github/workflows/pages.yml` auto-publishes every push to `main`.
5. Your site URL will be `https://YOUR-USERNAME.github.io/REPOSITORY-NAME/`.

Example for your account (`jastiranjeeth-tech`):

- `https://jastiranjeeth-tech.github.io/zenex-exports-github/`

## Custom domain

This repo already includes [CNAME](CNAME) set to:

- `zenex-granite-exports.com`

DNS setup at your domain registrar:

- For apex `zenex-granite-exports.com` add A records to GitHub Pages IPs:
	- `185.199.108.153`
	- `185.199.109.153`
	- `185.199.110.153`
	- `185.199.111.153`
- Add CNAME for `www` pointing to:
	- `jastiranjeeth-tech.github.io`

After DNS propagates, GitHub Pages will serve:

- `https://zenex-granite-exports.com`

## Maintenance

- Main pages:
	- `index.html`
	- `collections/index.html`
	- `about/index.html`
	- `contact/index.html`
- Images and logo are in `assets/`.
- Inventory update flow:
	1. Replace image files in `assets/`.
	2. If file names change, update references in HTML/CSS.
	3. Commit and push to `main`.
	4. GitHub Pages auto-deploys.

### Update inventory images from GitHub website (no local coding needed)

1. Open your repo in browser.
2. Go to `assets/` folder.
3. Click **Add file → Upload files**.
4. Upload new image(s) (use same file names if replacing existing inventory).
5. Add commit message and click **Commit changes** to `main`.
6. Wait ~1 minute for auto-deploy.

## Enquiry form email updates

- Current behavior: the contact form posts to FormSubmit using its standard hosted submission flow. Visitors complete any verification there and see the provider’s confirmation. It does not automatically open an email app.
- Destination email is read from the visible contact email link in [contact/index.html](contact/index.html). If you change that email, enquiries follow it automatically.
- Important first-time setup: submit the contact form from the live website, then check the destination inbox (including Spam) for FormSubmit’s activation email. Approve it to start receiving enquiries. Submit a fresh enquiry afterward and verify receipt; a browser confirmation alone does not verify inbox delivery.

## Recommended enhancement workflow

1. Create a branch for each enhancement.
2. Test locally.
3. Open a pull request to `main`.
4. Merge to publish.
