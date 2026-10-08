# Changelog

Alle noemenswaardige wijzigingen aan dit project. Nieuwste bovenaan.
Format gebaseerd op [Keep a Changelog](https://keepachangelog.com/nl/1.1.0/).
Eerdere wijzigingen (vóór oktober 2026) staan alleen in de git-geschiedenis.

Categorieën: **Toegevoegd**, **Gewijzigd**, **Opgelost**, **Verwijderd**, **Beveiliging**, **Onderhoud**.

## [Unreleased]

### Gewijzigd
- Deploy-workflow volgens `_standards/DEPLOY.md`: features via PR naar `staging`, gebundelde releases naar `main`. Branch protection op `staging`.
- `netlify.toml` (nieuw): geen build bij commits met alleen documentatie.

### Onderhoud
- `.github/dependabot.yml`: wekelijkse updates naar `staging` voor de site en `studio/`, gegroepeerd (Astro, Sanity, minor/patch).
- `AGENTS.md`, `CLAUDE.md` en `CHANGELOG.md` toegevoegd volgens `~/Code/_standards`.
