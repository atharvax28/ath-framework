# ATH Framework

This repository is a simple two-part layout for the ATH Framework site:

- `ath-framework/` – editable source for the site. It contains the npm project, the `public/` assets (HTML/CSS/JS/data), and scripts for copying the build output into the Pages folder.
- `docs/` – the static files that get published via GitHub Pages. Running `npm run build` from `ath-framework/` refreshes everything inside this directory, including the `.nojekyll` marker so GitHub serves the files without Jekyll processing.
- `LICENSE` – licensing information for the project.

The GitHub Actions workflow in `.github/workflows/deploy.yml` now follows GitHub's official Pages deployment flow: it builds the site, uploads the `docs/` directory as an artifact, and then publishes that artifact to the repository's Pages site. No manual branch selection is required—once the workflow runs, the site becomes available at `https://<your-username>.github.io/<this-repo>/`.

## Updating the site
1. `cd ath-framework`
2. `npm install`
3. Edit any files under `public/` (for example `public/data.json` to change the tree data or `public/css/arf.css` to adjust styles).
4. Run `npm run build` – this copies the current `public/` contents into the top-level `docs/` directory so it is ready for deployment.
5. Commit both `ath-framework/` and `docs/` changes and push.

> The repo intentionally keeps the generated `docs/` directory in version control so you can preview the static files locally, but production deployments are handled by the workflow which publishes the exact same files to the Pages site.
The repo intentionally keeps the generated `docs/` directory in version control so GitHub Pages can deploy straight from the `docs` folder with no extra tooling.
