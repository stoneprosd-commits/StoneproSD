# StonePro SD — Website

**13-page static HTML site for StoneProSD.com**

## File Structure

```
stoneprosd-site/
├── index.html                          ← Homepage
├── concrete-staining.html              ← Service: Staining & Decorative Finishes
├── concrete-sealing.html               ← Service: Concrete Sealing
├── concrete-restoration.html           ← Service: Concrete Restoration
├── anti-slip-pool-deck-sealing.html    ← Service: Anti-Slip Pool Deck Sealing
├── concrete-encinitas.html             ← City: Encinitas
├── concrete-del-mar.html               ← City: Del Mar
├── concrete-solana-beach.html          ← City: Solana Beach
├── concrete-carlsbad.html              ← City: Carlsbad
├── concrete-carmel-valley.html         ← City: Carmel Valley
├── concrete-la-jolla.html              ← City: La Jolla
└── concrete-rancho-santa-fe.html       ← City: Rancho Santa Fe
```

## Before Going Live — Replace These Placeholders

Search every file for the following and update:

| Placeholder | Replace With |
|---|---|
| `(000) 000-0000` | Your real phone number |
| `quotes@stoneprosd.com` | Your real email address |
| `CA LIC #0000000` | Your CA contractor license number |
| `https://www.stoneprosd.com` | Your real domain (in canonical tags) |

## Pre-Launch Banner

The homepage (`index.html`) has a pre-launch announcement banner at the very top.
When you're ready to launch, delete the block marked:
```
<!-- PRE-LAUNCH BANNER — remove this block (and its CSS) at launch -->
```
...down to and including the closing `</div>` before `<header>`.
Also delete the CSS block above `/* ---------- header ---------- */` that starts with `/* ---------- pre-launch banner ---------- */`.

## Quote Form CRM Hook

Every page has a quote form. When your CRM is set up, find the comment:
```
// TODO: POST form data to your CRM endpoint
```
Replace that line with your actual webhook/fetch call.

## Deploying to GitHub Pages

1. Create a new GitHub repo named `stoneprosd-site` (or your domain name)
2. Upload all files from this folder to the repo root
3. Go to Settings → Pages → Source → Deploy from branch → main / root
4. Your site will be live at `https://yourusername.github.io/stoneprosd-site`

For a custom domain (stoneprosd.com):
- Add a `CNAME` file to the repo root containing just: `stoneprosd.com`
- Point your domain's DNS to GitHub Pages (follow GitHub's custom domain guide)

## Gallery Placeholder Tiles

The homepage gallery and page headers use CSS gradient placeholders.
Swap these for real before/after photos as your first jobs complete.

## Built With

Pure HTML + CSS + vanilla JS. No frameworks, no dependencies, no build step.
Upload the files as-is — they work on any host (GitHub Pages, Netlify, Vercel, etc).
