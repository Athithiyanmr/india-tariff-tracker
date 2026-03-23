# India Electricity Tariff Tracker

A comprehensive tracker for electricity tariffs across all Indian states and UTs — with live data, year-on-year comparison, and validation tools.

## Live Site
After publishing: https://YOUR-USERNAME.github.io/india-tariff-tracker

## What's Inside

| File | Description |
|---|---|
| `index.html` | Landing page with links to all tools |
| `tariff_table.html` | Main tariff table — 16 states, all LT/HT categories |
| `tariff_validator.html` | Edit + validate + year-on-year comparison (2022–2025) |
| `tariff_tracker.html` | News feed, latest updates, policy changes |
| `tariff_pipeline.py` | Python auto-scraper for 36 SERC websites |
| `all_states_config.py` | Full 36-state SERC config |
| `google_apps_script_monitor.js` | Google Sheets auto-monitor script |
| `requirements.txt` | Python dependencies |

## Features
- 16 states with real tariff data (LT + HT, all consumer categories)
- 4-year history (FY 2022-23 to FY 2025-26)
- 12-rule validation engine
- Year-on-year comparison with % change
- Full change log / audit trail
- Auto-monitoring pipeline with Claude API extraction

## Running the Pipeline Locally

```bash
pip install -r requirements.txt
export ANTHROPIC_API_KEY=sk-ant-...
python tariff_pipeline.py --run-all
python tariff_pipeline.py --export --latest-only
```

## Auto-Update via GitHub Actions
Add ANTHROPIC_API_KEY in: GitHub repo Settings > Secrets > Actions
The workflow in .github/workflows/tariff_monitor.yml runs daily at 1 AM IST.

## Data Sources
Official SERC tariff orders: TNERC, MERC, KERC, APERC, TSERC, GERC, RERC, HERC, WBERC, OERC, PSERC, MPERC, UPERC, BERC, DERC, KSERC

## License
MIT
