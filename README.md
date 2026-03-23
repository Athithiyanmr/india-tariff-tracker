# India Electricity Tariff Tracker

Live electricity tariff data across all 36 Indian states and UTs — LT + HT, 4 years of history, auto-updating from official SERC orders.

## Live site
[https://athithiyanmr.github.io/india-tariff-tracker](https://athithiyanmr.github.io/india-tariff-tracker)

## Pages
| File | What it does |
|---|---|
| `index.html` | Homepage with links to all tools |
| `tariff_table.html` | Full tariff table — 16 states, filterable and sortable |
| `tariff_validator.html` | Edit, validate (12 rules), year-on-year comparison |
| `tariff_tracker.html` | News feed, SERC map, schema reference |
| `tariff_pipeline.py` | Python scraper + Claude API extractor |
| `all_states_config.py` | 36-state SERC config |
| `google_apps_script_monitor.js` | Google Sheets auto-monitor |

## Setup for auto-updates
1. Fork this repo
2. Go to Settings → Secrets → Actions → add `ANTHROPIC_API_KEY`
3. Go to Settings → Pages → Source: main branch / root
4. GitHub Actions runs daily at 1:00 AM IST automatically

## Local run
```bash
pip install -r requirements.txt
export ANTHROPIC_API_KEY=sk-ant-...
python tariff_pipeline.py --state "Tamil Nadu"
```
