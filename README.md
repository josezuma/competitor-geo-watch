<div align=center>
  <h1>👁️ Competitor GEO Watch</h1>
  <p><em>Agent skill that watches a list of competitors and alerts when their GEO readiness score changes.</em></p>
  <p><a href=LICENSE><img src="https://img.shields.io/badge/license-MIT-blue.svg" alt=License></a>
  <p>by <a href=https://brandvirality.com>BrandVirality</a><br>
  <strong>Author:</strong> <a href=https://github.com/josezuma>Jose Zuma</a></p>
</div>

## Quick Start

```bash
pip install requests
python3 scripts/watch.py --competitors competitors.txt
```

Competitors file format:
```
BrandVirality,https://brandvirality.com
CompetitorA,https://competitor-a.com
```

## Output
Weekly delta report: who improved, who declined, who added llms.txt.

## Related
geo-audit-skill, geo-prompts, awesome-ai-visibility
