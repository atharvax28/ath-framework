# ATH Framework Monorepo

This repository now hosts the ATH Framework source (`ath-framework/`) and the GitHub Pages build artifacts (`docs/`). It replaces the legacy OSINT Framework files entirely.

## Project layout

- `ath-framework/` – editable source (Node tooling, `public/`, data, scripts)
- `docs/` – static site generated via `npm run build`; served by GitHub Pages

## Quick start

```bash
git clone https://github.com/atharvax28/ath-framework.git
cd ath-framework/ath-framework
npm install
npm start   # http://localhost:8000
```

Update `public/data.json`, run `npm run build` to refresh `docs/`, then commit both directories.

## Deploying to GitHub Pages

1. From `ath-framework/ath-framework`, run `npm run build`.
2. Commit the updated `docs/` directory from the repo root.
3. In GitHub → **Settings → Pages**, select `main` / `docs`.

Your site will be available at `https://atharvax28.github.io/ath-framework/`.

