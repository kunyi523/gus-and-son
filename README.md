# Gus & Son Barbershop — unofficial pitch site

A mobile-first one-page website **proposal** for **Gus & Son Barbershop** (also Gus and Son Barber Shop) at 1530 King St E, Hamilton, ON L8K 1S9.

**This is not the shop’s official website.** It is an unofficial sample prepared as a proposal so the owner can see what a simple site could look like. It is not affiliated with Gus & Son Barbershop.

There is no online booking and no online payment. The real shop is walk-in. This page only helps people **call**, **get directions**, or open the shop’s **Facebook** page.

Live URL (once GitHub Pages is on): [https://kunyi523.github.io/gus-and-son/](https://kunyi523.github.io/gus-and-son/)

## How to open

Open `index.html` in a browser (double-click it, or drag it into a tab).

Optional local server, from this folder:

```bash
python3 -m http.server 8080
```

Then visit http://localhost:8080

## GitHub Pages

The site is static files at the **repository root** (`index.html`, `styles.css`).

To publish:

1. Repo **Settings → Pages**
2. Build and deployment → Source: **Deploy from a branch**
3. Branch: **main**, folder: **/ (root)**
4. Save

GitHub will serve the site at `https://kunyi523.github.io/gus-and-son/`.

## What’s on the page

- Shop name, King Street East address, click-to-call (`tel:+19055451945`)
- Hours (closed Monday, Tuesday, Sunday)
- Licensed Unsplash / Pexels atmosphere photos — **not** photos of this shop
- Real customer quotes from public listings (no invented names, stars, or dates)
- Google Map embed and Get directions
- Facebook link
- A discreet footer stating this is an unofficial proposal

Built as a simple HTML + CSS one-pager (a small script only highlights today’s hours in the America/Toronto timezone).
