# Kerbstone Studio — flagship marketing site

Static marketing site for **Kerbstone Studio**: template-led website packages (Spark / Launch / Engine + Care) for local UK service businesses, deployed on Netlify.

## Hard rules (do not break)

- **Prices are PROPOSED** — not live until the owner types `prices accepted` (or equivalent). Every price on the site must stay labelled PROPOSED until then.
- **DEMO portfolio only** — Ashford Drain Co and Hedge & Order are **fictional**. Never present them as real clients or testimonials.
- **No custom domains** on this deploy — `*.netlify.app` only.
- **No invented clients, fake social proof, or unapproved date promises.**

## Packages (PROPOSED)

| Package | Price (PROPOSED) | Notes |
|---------|------------------|-------|
| Spark   | £895             | 1 page, form, analytics, Netlify, 1 revision, 50% deposit |
| Launch  | £2,450           | 4–6 pages, SEO basics, form, 2 revisions, 50% deposit |
| Engine  | £3,950           | Launch + blog/listings + light automation, 2 revisions |
| Care    | £149/mo          | 3 hrs/month capped retainer |

Rate floor: **£50/hr PROPOSED**.

## Local preview

```bash
# any static server, e.g.
npx --yes serve .
# or
python3 -m http.server 8080
```

Publish directory is the repo root (static HTML/CSS/JS).

## Deploy (Netlify CLI)

```bash
netlify deploy --prod --dir . --no-build --site-name kerbstone-studio-flagship --json
```

Do **not** attach a custom domain unless the owner explicitly approves.

## Forms

Enquiry form uses Netlify Forms (`name="enquiry"`) with honeypot `bot-field`. Success redirects to `thanks.html`.

## DEMO live URLs

- https://kerbstone-demo-ashford-drain.netlify.app — Ashford Drain Co (**DEMO fictional**)
- https://kerbstone-demo-hedge-order.netlify.app — Hedge & Order (**DEMO fictional**)

## Stack

Vanilla HTML / CSS / JS. Orbitron via Google Fonts (optional display face). System UI for body. CSS variables, minimal JS, `prefers-reduced-motion` support.
