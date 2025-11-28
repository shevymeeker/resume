# Resume Intake PWA

This project provides a single-page, offline-first intake form that clients can fill out to generate a clean PDF and email it to the resume writer. The AI prompt builder stays hidden unless the page is opened with `?owner=1`.

## How to run a local test
1. Start a lightweight static server from the repo root (for example, Python's built-in HTTP server):
   ```bash
   python -m http.server 8000
   ```
2. Open http://localhost:8000/ in your browser to use the client-facing form.
3. To see the private AI prompt builder, open http://localhost:8000/?owner=1.

## Deploying
- Host the `index.html` on GitHub Pages (or any static host). You can replace your existing `index.html` with the version in this repo; everything is contained in that single file.
- Because all data is stored locally with Dexie/IndexedDB, the form works offline after the first load.
