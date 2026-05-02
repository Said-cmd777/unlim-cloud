# UnlimCloud Desktop App

## Overview
Unofficial desktop application for UnlimCloud — a cloud storage service that uses Telegram IDs as storage identifiers. This is a Tauri-based desktop app, but in the Replit environment it runs as a static web frontend.

## Architecture
- **Frontend**: Plain HTML/CSS/JS in `src/index.html`
- **Assets**: `src/assets/` (logos, payment icons, SVGs)
- **Desktop wrapper**: `src-tauri/` (Rust/Tauri config — not used in Replit)
- **Server**: `server.js` — a minimal Node.js HTTP server serving `src/` on port 5000

## Running
- Workflow: `Start application` runs `node server.js` on port 5000
- The app checks for updates via GitHub API, then redirects to https://unlim-cloud.web.app

## Deployment
- Configured as a **static** deployment with `publicDir: "src"`
- No build step required

## Key Files
- `src/index.html` — main frontend page
- `server.js` — static file server for Replit dev environment
- `src-tauri/tauri.conf.json` — Tauri desktop app configuration (not used in web mode)
