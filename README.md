# Gus & Son Barbershop — unofficial pitch site

A mobile-first one-page website **proposal** for **Gus & Son Barbershop** (also Gus and Son Barber Shop) at 1530 King St E, Hamilton, ON L8K 1S9.

**This is not the shop’s official website.** It is an unofficial sample prepared as a proposal so the owner can see what a simple site could look like. It is not affiliated with Gus & Son Barbershop.

There is no online booking and no online payment. The real shop is walk-in. This page only helps people **call**, **get directions**, or open the shop’s **Facebook** page.

Live URL (after Pages is on): [https://kunyi523.github.io/gus-and-son/](https://kunyi523.github.io/gus-and-son/)

## How to open

The whole site is one self-contained file: `index.html` (CSS is inlined). Open that file in a browser, or visit the Pages URL on a phone.

Optional local server, from this folder:

```bash
python3 -m http.server 8080
```

Then visit http://localhost:8080

## GitHub Pages

Static files live at the **repository root**. Preferred path: add `.github/workflows/pages.yml` (GitHub currently blocks this token from writing workflow files; paste the YAML below on a machine with `workflow` scope).

```yaml
name: Deploy GitHub Pages

on:
  push:
    branches: [main]
  workflow_dispatch:

permissions:
  contents: read
  pages: write
  id-token: write

concurrency:
  group: pages
  cancel-in-progress: false

jobs:
  deploy:
    runs-on: ubuntu-latest
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    steps:
      - name: Checkout
        uses: actions/checkout@v4
      - name: Configure Pages
        uses: actions/configure-pages@v5
      - name: Upload static files
        uses: actions/upload-pages-artifact@v3
        with:
          path: '.'
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v4
```

Then enable Pages once:

1. **Settings → Pages**
2. Build and deployment → Source: **GitHub Actions**
3. Re-run the **Deploy GitHub Pages** workflow

Until that workflow exists, you can also use Source: **Deploy from a branch** → **main** / **/** (root).

GitHub will serve the site at `https://kunyi523.github.io/gus-and-son/`.

## What’s on the page

- Shop name, King Street East address, click-to-call (`tel:+19055451945`)
- Thumb-sized **Call** and **Directions** buttons
- Hours (closed Monday, Tuesday, Sunday)
- Licensed Unsplash / Pexels atmosphere photos — **not** photos of this shop
- Real customer quotes from public listings (no invented names, stars, or dates)
- Google Map embed and Get directions
- Facebook link
- A discreet footer stating this is an unofficial proposal

Built as a simple HTML one-pager (a small script only highlights today’s hours in the America/Toronto timezone).
