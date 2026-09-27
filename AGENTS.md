# Base44 Dev Environment

## Project Overview
Simple static HTML/CSS website (Norwegian university course project). No build tools, no backend, no package manager — just plain `.html` and `.css` files served directly.

## Running the app
```bash
docker compose -f docker-compose.base44.yml up -d
```
- nginx serves the repo root on host port 3000.
- Files are bind-mounted read-only, so edits appear on browser refresh (no live reload / HMR — call `reload_preview` after changes).
- Healthcheck: `wget --spider http://localhost:80/index.html`

## Structure
- `index.html` — home page
- `om-oss.html`, `tjenester.html`, `kontaktoss.html` — subpages
- `style.css` — main stylesheet
- `kontaktoss/` — member vCard pages (subdirectory with its own `style.css`)
- `logo.png`, `elonmusk.jpg` — images

## No secrets needed
This project has no external service dependencies.
