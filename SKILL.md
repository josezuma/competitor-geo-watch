---
name: competitor-geo-watch
description: Watches a list of competitor URLs and alerts when their GEO readiness score changes. Runs weekly audits via geo-audit-skill and reports changes. Use when tracking competitor AI-search visibility.
license: MIT
---
# Competitor GEO Watch

Monitors competitor AI-search visibility over time.

## Setup
```bash
pip install requests
python scripts/watch.py --competitors competitors.txt
```

## Output
Weekly delta report: who improved, who declined, who added llms.txt.
