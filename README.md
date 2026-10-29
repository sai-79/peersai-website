# PeersAI website

A responsive, static landing page for `peersai.dev`, built with plain HTML, CSS, and JavaScript. No build step or framework is required.

## Before publishing

Please review the copy so it accurately reflects what you are building. The current page explicitly describes PeersAI as an early-stage project in development and does not claim that features, users, integrations, or services already exist.

Before adding public contact details, configure an email service for your domain. A public GitHub repository link is intentionally not included yet because one has not been supplied.

## Preview locally

Open `index.html` in a browser. For a local development server, run this from the project directory:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Deploy with GitHub Pages

1. Create a GitHub repository, for example `peersai-website`.
2. Add `index.html`, `styles.css`, `script.js`, and `README.md` to the repository root.
3. In the repository, open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select the `main` branch and `/ (root)`, then save.
6. Wait for GitHub Pages to publish the site. The default URL will look like `https://YOUR-USERNAME.github.io/peersai-website/`.

### Connect `peersai.dev`

1. In **Settings → Pages → Custom domain**, enter `peersai.dev` and save.
2. At the domain registrar's DNS settings, add the DNS records GitHub Pages currently recommends for an apex domain. GitHub commonly uses four A records for the apex and an optional `www` CNAME; copy the current values from GitHub's documentation rather than relying on old instructions.
3. Wait for DNS to propagate. Return to Pages settings and enable **Enforce HTTPS** when available.
4. Optionally add `www.peersai.dev` as a second custom domain/redirect after configuring its CNAME according to GitHub's current instructions.

Official guide: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site

## Alternative: deploy on Vercel

1. Import the repository into https://vercel.com/.
2. Deploy it as a static site; no framework or build command is needed.
3. Open the project's **Settings → Domains** and add `peersai.dev`.
4. Add the DNS records Vercel displays at your registrar.
5. Wait for verification and HTTPS provisioning.

## Project structure

```text
peersai-website/
├── index.html
├── styles.css
├── script.js
├── README.md
└── .gitignore
```

## Editing the page

- Change page text in `index.html`.
- Change colors, spacing, typography, and layout in `styles.css`.
- Mobile navigation and the copyright year are handled in `script.js`.
- Google Fonts are loaded remotely; system-font fallbacks are included.
