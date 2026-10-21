# Tabular Lab

A browser-based, local-first analytics prototype inspired by Redash.

## Status

**Prototype — not yet a production-ready, fully integrated Redash alternative.** The milestone source packages were developed incrementally and are focused prototypes; they are not guaranteed to compose into one complete working application. SQL execution and dashboard widgets are not yet fully connected to DuckDB-WASM and live results.

## Current prototype direction

- React + TypeScript + Vite
- Local-first browser workspace
- Saved-query organization, tags, favorites, SQL snippets, version snapshots
- Dashboard widgets and JSON dashboard configuration
- Roadmap: integrate CSV/Excel ingestion, DuckDB-WASM, SQL execution, query-backed dashboards, exports, CI and end-to-end tests

## Run a milestone bundle

Extract a downloaded milestone ZIP, then run:

```bash
npm install
npm run dev
npm test
npm run build
```

Build/test results must be verified locally before deployment.

## Privacy

The target architecture processes uploaded tabular data locally in the browser. These milestone bundles do not yet represent a verified, integrated implementation. Review network requests (including external fonts and images) before using sensitive data.

## Roadmap

1. Unify milestones into one app with upload, schema catalog and DuckDB-WASM restoration.
2. Complete SQL execution, parameters and virtualized results.
3. Connect visualizations and dashboard filters to saved queries.
4. Add CSV/XLSX/JSON exports, workspace import/export and alerts.
5. Add CI build/test verification and Playwright upload → query → chart → dashboard tests.
6. Consider optional auth, collaboration, cloud scheduling and database connectors.
