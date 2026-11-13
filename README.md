# 🧺 Joint Family Picnic Expense Calculator (PWA)

A progressive web app for logging picnic costs, splitting them fairly between
families, and generating an exact settlement plan (who pays whom).

## Features

- **Three split modes per expense**
  - *Per Person* — divided by adult-equivalent headcount (children can count as
    a fraction, e.g. 0.5, or 0 = free)
  - *Equal Per Family* — divided evenly regardless of size
  - *Custom* — type each family's exact share, with live "assigned vs amount" hints
- **Club / Common fund** — expenses paid from a shared pool are tracked and owed back
- **Instant results** — per-family shares, paid amounts, balances, percentages
- **Settlement plan** — a minimal list of transfers that settles all balances
- **Category breakdown** — bar chart of spending by category
- **Data safety** — all money math in integer cents, plus a live integrity check
  (shares must equal the total; balances must sum to zero)
- **Local persistence** — data is saved automatically in the browser
- **PWA** — installable on home screen / desktop, works fully offline
- **Exports** — copy a text summary, download CSV, print

## Files

| File | Purpose |
|---|---|
| `index.html` | The entire app (markup, styles, logic) |
| `manifest.json` | PWA metadata: name, icons, display mode, theme colors |
| `sw.js` | Service worker: offline caching + install eligibility |
| `icon-192.png`, `icon-512.png` | App icons (install, splash, shortcuts) |
| `apple-touch-icon.png` | iOS home-screen icon |

## Quick start

Service workers require HTTPS (or `localhost`), so open it through any static
server:

```bash
cd picnic-pwa
npx serve .                    # or: python3 -m http.server 8000
```

Then visit the printed URL. Install via the browser's install icon, the new
**Install app** button in the app, or on iOS: Share → "Add to Home Screen".

## Deploying

Upload all 6 files to any static host (GitHub Pages, Netlify, Vercel, Cloudflare
Pages, a shared hosting `public_html` folder, …). No backend or build step needed.

## Updating the app

After changing `index.html`, bump the version string in `sw.js`:

```js
const VERSION = "v1.0.1";
```

This invalidates the old cache so returning users get the new version.

## Data & privacy

Everything is computed and stored locally in the user's browser (`localStorage`).
No data ever leaves the device — there is no server, no tracking, no analytics.
