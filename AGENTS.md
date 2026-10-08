# AGENTS.md: mier.as

Instructies voor AI-agents (Claude Code, Cursor, Codex) en ontwikkelaars die aan dit project werken.
Lees eerst `README.md` voor context en `CHANGELOG.md` voor recente wijzigingen.

## Project
- Klant: eigen site · Bedrijf: MIERAS · SLA: n.v.t.
- Stack: Astro 5 (`output: 'server'`, Netlify-adapter), Sanity 4 (Studio op `/studio`, losse studio in `studio/`), Node 20.19 (zie `.nvmrc`)

## Werkwijze
- Werk nooit direct op `main`. Branch vanaf `staging` → PR naar `staging` → deploy preview → merge. Naar `main` alleen gebundelde releases en hotfixes, volgens `~/Code/_standards/DEPLOY.md` (elke productiedeploy kost Netlify-credits).
- Branchnamen: `feat/…`, `fix/…`, `chore/…`, `docs/…`.
- Commit nooit `.env`-bestanden of tokens. Nieuwe variabelen: naam toevoegen aan `.env.example` en de README-tabel.
- Variabelen met `PUBLIC_` komen in de browser terecht: nooit voor tokens.

## Documentatie bijhouden (verplicht)
- Elke wijziging die je commit: voeg een regel toe onder `## [Unreleased]` in `CHANGELOG.md`.
- Bij een release (`staging → main`): zet `[Unreleased]` om naar een datumkop.
- Verandert setup, env, stack of deploy? Werk `README.md` bij.

## Conventies
- Moderne CSS: custom properties, OKLCH-kleuren, logical properties, container queries waar zinvol.
- Toegankelijkheid: WCAG 2.2 AA. Semantische HTML, focus-states, `prefers-reduced-motion` respecteren (ook bij GSAP).
- AVG: geen tracking of third-party embeds zonder consent.
- Animaties (GSAP): leg in een comment kort de logica uit (timeline, trigger, cleanup).
- Sanity: site-instellingen, SEO-velden en Visual Editing volgens `~/Code/_standards/SANITY.md`.
- Afbeeldingen: profiel `TODO (Portfolio / Website / Performance-first)` volgens `~/Code/_standards/IMAGES.md`.
- SEO en AI readiness (meta, JSON-LD, sitemap, robots, `llms.txt`) volgens `~/Code/_standards/SEO.md`.

## Projectspecifiek
- De site is SSR (`output: 'server'`): Sanity-content staat direct live, een Netlify build hook vanuit Sanity is overbodig.
- TODO: welke Netlify-site deze repo bouwt en of `mier.as` nog live moet (het domein heeft nu geen DNS-record).
