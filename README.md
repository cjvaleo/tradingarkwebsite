# Trading Ark — Website

Single-page conversion site for Trading Ark Premium community. Funnels traffic to Whop (primary) and Discord (secondary).

## Stack

- Vanilla HTML / CSS / JS (no framework, no build step)
- Single-page, single `index.html` + external `styles.css`
- Hosted as static — Vercel, Netlify, or Cloudflare Pages compatible

## Local dev

Just open `index.html` in a browser, or run any static server:

```
npx serve .
```

## Deploy

- Push to main → connect repo to Vercel/Netlify → auto-deploy
- No env vars needed
- No build command (static site)

## Before launching — replace these placeholders

Search the repo for `TODO` comments. There are 11 things to swap before going live:

| What | Where | How |
|---|---|---|
| Whop URL | All `whop.com/trading-ark` instances | Find/replace with real Whop checkout URL |
| Discord URL | All `discord.gg/tradingark` instances | Find/replace with real invite URL |
| Pricing number | `[TBD]` in `.price-num` | Replace with monthly price |
| Logo SVG | `/assets/img/logo.svg` (referenced in nav + footer) | Drop in real SVG |
| OG share image | `/assets/img/og-image.jpg` (1200×630) | Drop in real image |
| Favicon | `/assets/img/favicon.ico` | Generate from logo |
| Canonical URL | `<link rel="canonical">` in `<head>` | Update to real domain |
| Twitter URL | Footer social link | Real handle |
| Instagram URL | Footer social link | Real handle |
| Real stats | 3 placeholders in Community section (`data-placeholder="true"`) | Replace member count, trades logged, retention % |
| Legal pages | Footer "Terms / Privacy / Disclaimer" hrefs | Link to real legal pages |

## File structure

```
/
├── index.html              ← single page
├── assets/
│   ├── css/
│   │   └── styles.css
│   └── img/                ← drop real assets here
├── README.md
└── .gitignore
```

## Brand reference

See `/docs/handoff.md` for the locked brand system (colors, fonts, voice).
