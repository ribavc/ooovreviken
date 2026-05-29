# Øvreviken Luxury Website

Production-ready bilingual microsite for Øvreviken in Øystese, Norway.

## Run locally

Use the bundled Node runtime in Codex or any Node 20+ install:

```bash
node server.mjs
```

Then open `http://localhost:4173`.

## MongoDB contact form

Install dependencies in a normal Node environment:

```bash
npm install
```

Copy `.env.example` to `.env` and set `MONGODB_URI`. The `/api/contact` route writes validated submissions to `MONGODB_DB.MONGODB_COLLECTION`.

If MongoDB is not configured, local development stores submissions in `data/contact-submissions.jsonl` so the form can still be tested without losing data.

## Custom photography

No stock or AI-generated imagery is included. Add real restaurant imagery to:

- `public/media/hero.jpg`
- `public/media/about-1.jpg`
- `public/media/about-2.jpg`
- `public/media/gallery-1.jpg` through `public/media/gallery-6.jpg`

The layout automatically upgrades from cinematic CSS art direction to the supplied photography when those files exist.

## Menu source files

The provided menu images are copied to `public/source-menu/` for traceability, and the structured interactive menu lives in `menu-data.js`.
