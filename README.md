# TT Arena Docs

This is a [Mintlify](https://mintlify.com) documentation site for TT Arena, covering the organizer web app (play.ttarena.app) and the TT Arena Player app. Modeled on the structure of docs.matchr.in. The referee app is intentionally out of scope.

## Previewing locally

```
npm i -g mintlify
mintlify dev
```

This serves the site at `http://localhost:3000` from this folder.

## Structure

- `index.mdx` — Introduction
- `getting-started/` — first-run guides for organizers and players
- `organizer-guide/` — tournament settings, registrations, draws & scoring
- `player-app/` — installing, logging in, and using the Player app
- `faq.mdx`, `changelog.mdx`
- `images/brand/` — real TT Arena logo and favicon assets, copied from the main repo
- `images/screenshots/` — mockup screenshots built from fictional sample data ("Sample Open 2026"), not real tournaments or players. Source HTML for each mockup lives in `.mockups/` if they ever need editing or regenerating.
- `docs.json` — Mintlify site config (nav, theme, logo)

## Going live

This repo has no git remote yet. To publish:

1. Create a Mintlify account at [mintlify.com](https://mintlify.com) and start a new project.
2. Either let Mintlify's onboarding auto-create a GitHub repo for you, or create an empty one yourself (e.g. `ttarena-docs` under the `ttarenaapp-a11y` GitHub account) and push this folder to it:
   ```
   git remote add origin <your-new-repo-url>
   git push -u origin main
   ```
3. Connect that repo in the Mintlify dashboard.
4. Once live, add a custom domain (e.g. `docs.ttarena.app`) from Mintlify's domain settings, and point a CNAME at it from your DNS provider.
5. Submit the new domain as a property in [Google Search Console](https://search.google.com/search-console) and submit `sitemap.xml` (Mintlify generates this automatically) so it gets indexed.
