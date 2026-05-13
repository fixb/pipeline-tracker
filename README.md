# Pipeline Tracker

A self-contained, single-file HTML pipeline tracker for fundraising / sales pipelines.

**All data stays in your browser.** Nothing is sent to a server — prospects, history, and probability adjustments live in your browser's `localStorage`. The app is one static HTML file with no backend.

## Features

- Pipeline table with inline edit (estimate, stage, manual probability override per prospect)
- Customizable stages: add, rename, reorder, recolor, edit default probability, delete (with auto-downgrade of affected prospects)
- Funnel view with drill-down (click any stage to expand)
- Closings view with optimistic / base / conservative / stress scenarios
- Velocity analytics: average time per stage, full-cycle duration, stuck-prospect detection
- Probability Monitor with snapshots and sensitivity analysis
- Activity history with type filters
- CSV import (overwrite) and CSV export
- History export

## Usage

1. Open `index.html` in a browser, or visit the GitHub Pages URL.
2. Click `+ Prospect` to add manually, or `↑ Import` to load a CSV.
3. Use `⚙ Stages` to customize stages to your workflow.

### CSV import format

```
Name,Estimate ($m),Stage,Status,Region,Proba,Manual Proba,EV ($m)
"ACME CORP",100,"3","Met Founder/IC","Europe",35%,,35.0
"BETA LP",250,"2","Met","Canada",20%,60%,150.0
```

The `Status`, `Proba`, and `EV` columns are derived and ignored on import. `Manual Proba` is optional — if present, it sets a per-prospect probability override.

### Privacy

Your data is stored only in your browser's `localStorage` for the origin where you load the app. Switching browsers, clearing site data, or visiting from a different origin will not show your data. Use `↓ CSV` and `↓ History` to back up regularly.

## License

MIT
