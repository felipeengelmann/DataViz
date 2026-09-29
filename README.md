# Data Viz Color Guide

Color palettes, chart rules and audit tools for the product's Highcharts dashboards.

## Open it
- **Quick view:** `dist/Data Viz Color Guide.html` — a single self-contained file (the Chart gallery loads Highcharts from a CDN).
- **Source:** serve this folder with any static server (for example `npx serve .`) and open `Start Here.dc.html`. Pages load `support.js`, `palette-data.js` and `tokens/` by relative path, so opening the files straight from disk won't work.

## Pages
| File | Purpose |
|---|---|
| `Start Here.dc.html` | Landing page: the four-step path from metric to chart, and the page map |
| `Guidelines.dc.html` | Choosing a palette, status vocabulary, rules, accessibility, Highcharts notes |
| `Palettes.dc.html` | Every v1 palette in light and dark, with contrast and label tokens |
| `Chart Gallery.dc.html` | 10 Highcharts types previewed across palettes and category counts |
| `Audit Kit.dc.html` | Review process, "Which chart?" flow, checklist, metric registry, before/after fixes |
| `Swatch Sheet.dc.html` | All tokens on one page, plus the tokens.json download |
| `Palette Proposal.dc.html` | Record of the v1 palette decision (option A) |

## Data
- `tokens/dataviz.tokens.json` — design tokens in DTCG format, with light and dark values. Groups marked `"$extensions": {"com.dataviz": {"status": "held"}}` are not for new charts.
- `palette-data.js` — computed contrast values used by the pages.
- `audit/dashboard-inventory.csv` — one row per chart in the product.
- `audit/metric-registry.csv` — one row per metric: chart type, palette, color key, sort order.

## v1 palette scope
Categorical, Status, Sequential and Diverging (Diverging entries must name their midpoint), plus Emphasis as a technique. Multi-hue and Heatmap severity are held.

## Rebuilding `dist/`
The single-file build is generated from the pages above. After editing any page, regenerate it so the two stay in sync.
