# Tabular Lab

A browser-based, local-first analytics prototype inspired by Redash. This repository folder documents the staged milestone prototype and current capabilities.

## Status

**Prototype — not a production-ready, fully integrated Redash alternative yet.** Milestone source packages were developed incrementally. The milestone bundles are focused prototypes and are not guaranteed to compose into a single, complete working application. The SQL editor and dashboard widgets are not yet fully connected to DuckDB-WASM execution and live query results.

## Current prototype direction

- React + TypeScript + Vite
- Local-first browser workspace
- Saved-query organization, tags, favorites, SQL snippets, version snapshots
- Dashboard widgets and JSON dashboard configuration
- Intended next steps: integrate CSV/Excel import, DuckDB-WASM queries, query-backed dashboards, export paths, and automated end-to-end tests

## Run a milestone bundle

Download one of the milestone ZIP files from the project handoff, extract it, then run:

```bash
npm install
npm run dev
npm test
npm run build
```

Build/test results should be verified locally before deployment.

## Privacy

The target architecture processes uploaded tabular data locally in the browser. This folder does not itself contain a verified, integrated source implementation, and external resources such as web fonts or image URLs can make network requests. Review network use before putting sensitive data in any build.

## Roadmap

1. Unify the milestones into one app with upload, schema catalog, and persistent DuckDB-WASM database restoration.
2. Complete SQL execution, parameter substitution, and virtualized query results.
3. Connect visualizations and dashboard filters to saved query results.
4. Add CSV/XLSX/JSON exports, workspace import/export, alerting, and accessibility polish.
5. Add CI build/test verification and Playwright upload → query → chart → dashboard tests.
6. Consider optional server features only if needed: auth, collaboration, cloud scheduling, and database connectors.
