# Sara Academy

## Overview
Static single-page HTML site (no backend, no build step). Served by Vite dev server for live reload.

## Setup
- Runtime: `node:22-slim` via `docker-compose.base44.yml`
- Dev server: `npm run dev` → Vite on port 3000, bind 0.0.0.0
- Dependencies installed on container startup via `npm install` (no lockfile on first boot; one is generated automatically)
- No secrets or external services required

## Verification
- `curl -s http://localhost:3000/` should return the HTML with `<h1>Hello Sara Academy</h1>`
- Healthcheck: node fetch to `http://localhost:3000/`
