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

## Enquiry form email updates

- Current behavior: enquiry submits are sent directly using FormSubmit (`ajax` endpoint), with `mailto:` fallback if direct send fails.
- Destination email is set to `zenexexports@gmail.com` in `contact/index.html`.
- Important first-time setup: FormSubmit sends an activation/verification email to the destination inbox. Approve it once to start receiving enquiries.

## Recommended enhancement workflow

1. Create a branch for each enhancement.
2. Test locally.
3. Open a pull request to `main`.
4. Merge to publish.
