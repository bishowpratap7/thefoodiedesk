# The Foodie Desk 🍜

The eternal question — what should we eat? This desk answers it daily with a rotating spread of recipes from kitchens around the world, from slow comfort food to fifteen-minute lifesavers, plus the kitchen and grocery deals worth grabbing while they last.

- Live page: https://bishowpratap7.github.io/thefoodiedesk/
- Run by **Bishow Pandey** — follow on X: https://x.com/bishowppandey
- Sister desks: The Dev Desk (developer news), Scroll Patrol (trending posts & memes), The World Desk (world news), The Stock Desk (stock deep dives), plus The Shopping Desk, The Cozy Desk, The Foodie Desk and The Style Desk

## What's on the desk
- **🍽️ On the Menu**
- **🍰 Something Sweet**
- **🛒 Kitchen & Grocery Deals**

A daily rotating menu of recipes from TheMealDB's public collection (photos and dishes link to the full recipe at the source), plus kitchen & grocery deals from community feeds.

## How it works
- `tools/scan.py` reads the public sources above (no API keys), writes `data/feed.json`, bakes an SEO summary of every item into `index.html`, and regenerates `feed.xml` and `sitemap.xml`. If a source fails, the desk keeps its last good data and flags it stale.
- A GitHub Actions loop (`.github/workflows/loop-scan.yml`) re-runs the scanner every 30 minutes around the clock and commits only when something changed; each loop job hands off to its successor, so the desk stays current on its own.
- The page is a single static file — no backend, no build step, no tracking.

## Repos
- `thefoodiedesk` (public) — the live site, served by GitHub Pages
- `the-foodie-desk` (private) — the archive twin

## Good to know
Recipes are provided by TheMealDB's community database and linked at the source; check ingredients for allergies and follow the full method and food-safety guidance there. Deal prices change quickly — confirm at the store.
