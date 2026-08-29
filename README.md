# Gus & Son Barbershop — unofficial pitch site

A mobile-first one-page website **proposal** for **Gus & Son Barbershop** (also Gus and Son Barber Shop) at 1530 King St E, Hamilton, ON L8K 1S9.

**This is not the shop’s official website.** It is an unofficial sample prepared as a proposal so the owner can see what a simple site could look like. It is not affiliated with Gus & Son Barbershop.

There is no online booking and no online payment. The real shop is walk-in. This page only helps people **call**, **get directions**, or open the shop’s **Facebook** page.

Live URL: [https://kunyi523.github.io/gus-and-son/](https://kunyi523.github.io/gus-and-son/)

## How to open

The whole site is one self-contained file: `index.html` (CSS is inlined). Open that file in a browser, or visit the Pages URL on a phone.

Optional local server, from this folder:

```bash
python3 -m http.server 8080
```

Then visit http://localhost:8080

## GitHub Pages

Static files live at the **repository root**. A workflow at `.github/workflows/pages.yml` deploys from `main` with `actions/checkout`, `configure-pages`, `upload-pages-artifact` (path `.`), and `deploy-pages`.

If that workflow is not in the repo yet (GitHub blocks workflow-file writes without the `workflow` token scope), you can still publish by branch:

1. **Settings → Pages**
2. Build and deployment → Source: **GitHub Actions** (preferred) or **Deploy from a branch** → **main** / **/** (root)
3. Save, then re-run the workflow if using Actions

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
