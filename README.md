# EdgeConsults, LLC — Website

Company website for EdgeConsults, LLC built with [Hugo](https://gohugo.io/) and the [Hugo Hero Theme](https://github.com/zerostaticthemes/hugo-hero-theme) by Zerostatic.

## Prerequisites

- [Hugo Extended](https://gohugo.io/installation/) v0.92.0 or later (must be the **extended** version)

### Install Hugo (macOS)
```bash
brew install hugo
```

### Install Hugo (Linux)
```bash
# Download from https://github.com/gohugoio/hugo/releases
# Choose the hugo_extended_*.deb or .tar.gz for your platform
```

## Local Development

```bash
# Clone the repo
git clone https://github.com/edgeconsults/edgeconsults.com.git
cd edgeconsults.com

# Start the dev server
hugo server

# Open http://localhost:1313 in your browser
```

## Build for Production

```bash
hugo --minify
```

Output goes to the `public/` directory.

## Deploy to GitHub Pages

This repo includes a GitHub Actions workflow in `.github/workflows/hugo.yml` that automatically builds and deploys to GitHub Pages on push to `main`.

### Setup:
1. Push this repo to GitHub (e.g., `edgeconsults/edgeconsults.com`)
2. Go to repo Settings → Pages → Source → select "GitHub Actions"
3. Set your custom domain `edgeconsults.com` in Settings → Pages → Custom domain
4. Add DNS records at your registrar:
   - `A` record: `185.199.108.153`
   - `A` record: `185.199.109.153`
   - `A` record: `185.199.110.153`
   - `A` record: `185.199.111.153`
   - `CNAME` for `www`: `edgeconsults.github.io`

## Deploy to Netlify (alternative)

A `netlify.toml` is included. Just connect your GitHub repo to Netlify.

## Deploy to GCP Cloud Storage (alternative)

```bash
hugo --minify
gsutil -m rsync -r -d public/ gs://edgeconsults.com/
```

## Contact Form

The contact form uses [Formspree](https://formspree.io/). To activate:

1. Sign up at formspree.io
2. Create a new form
3. Copy your form ID
4. Replace `YOUR_FORMSPREE_ID` in `layouts/contact/contact.html`

## Customization

- **Content:** Edit markdown files in `content/`
- **Config:** Edit `config.toml` for site title, menus, meta tags
- **Contact info:** Edit `data/contact.yaml`
- **Social links:** Edit `data/social.json`
- **Logos:** Replace SVGs in `static/images/`
- **Photos:** Add images to `static/images/`

## TODO

- [ ] Replace placeholder Formspree ID
- [ ] Add Google Scholar ID to social.json
- [ ] Replace SVG logos with final brand designs
- [ ] Add hero background images (royalty-free or custom photos)
- [ ] Set up info@edgeconsults.com email
