<div align=center>
  <h1>👁️ Competitor GEO Watch</h1>
  <p><em>Agent skill that watches a list of competitors and alerts when their GEO readiness score changes. Runs weekly, reports deltas.</em></p>
  <p><a href=LICENSE><img src="https://img.shields.io/badge/license-MIT-blue.svg" alt=License></a>
  <a href=https://github.com/josezuma/competitor-geo-watch/actions/workflows/ci.yml><img src="https://img.shields.io/badge/CI-passing-green.svg"></a></p>
  <p>by <a href=https://brandvirality.com>BrandVirality</a> — <strong>SaaS for AI visibility.</strong><br>
  <strong>Author:</strong> <a href=https://github.com/josezuma>Jose Zuma</a></p>
</div>

---

## Quick Start

```bash
pip install requests
python3 scripts/watch.py --competitors competitors.csv
```

## Competitors File Format

```csv
name,url
BrandVirality,https://brandvirality.com
CompetitorA,https://competitor-a.com
CompetitorB,https://competitor-b.com
```

## Output: Weekly Delta Report

```
Competitor GEO Watch — Week 28, 2026
=====================================

IMPROVED:
  + CompetitorA: 45 → 62 (+17 pts)
    Added llms.txt, improved schema coverage

DECLINED:
  - CompetitorB: 78 → 72 (-6 pts)
    Removed FAQ schema, no changes to llms.txt

UNCHANGED:
  BrandVirality: 45/100 (needs work)
    Still missing llms.txt and author EEAT signals
```

## How It Works

1. Reads competitor list from CSV
2. For each competitor, runs a GEO audit (llms.txt, robots.txt, schema, citability)
3. Compares scores against previous run (stored in data/history.json)
4. Generates delta report showing who improved, declined, or stayed same
5. Can be scheduled via cron for weekly monitoring

## Why Track Competitors

AI search visibility changes fast. A competitor who adds llms.txt today could beat you in AI citations tomorrow. This tool helps you:

- See exactly when competitors improve their GEO readiness
- Identify what specific changes they made (llms.txt, schema, EEAT)
- Measure your relative position in the market
- Get alerted when you're falling behind

## Related

- [geo-audit-skill](https://github.com/josezuma/geo-audit-skill) — Individual URL audits
- [geo-prompts](https://github.com/josezuma/geo-prompts) — Benchmark prompt sets
- [awesome-ai-visibility](https://github.com/josezuma/awesome-ai-visibility)
- [ai-search-share-of-voice](https://github.com/josezuma/ai-search-share-of-voice)
- [+15 more AI visibility repos](https://github.com/josezuma?tab=repositories)

## License

[MIT](LICENSE) © 2026 [Jose Zuma](https://github.com/josezuma) / [BrandVirality](https://brandvirality.com)
