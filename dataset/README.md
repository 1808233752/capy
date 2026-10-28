# Capy Capital Directory — Open Dataset

**A verified, source-linked dataset of investors and their deals, with a focus on Asia.**

Snapshot: **28 October 2026** · Maintained by [Capy](https://ai.capy-ai.workers.dev/space) · License: **CC BY 4.0**

Capy is a capital-intelligence directory covering **1125 investment firms** across six regions — the United States (374), the Hengqin–Macau Greater Bay Area cooperation zone (196), Japan (144), China (172), Hong Kong & Taiwan (114) and Europe (125). Every firm entry is verified against public sources; every deal in the timeline carries a source URL. **615 firms include a publicly listed contact email** (each marked with how it was verified).

Live, searchable version: **https://ai.capy-ai.workers.dev/space**

## Files

| File | Rows | Contents |
|---|---|---|
| `firms.csv` / `firms.json` | 1125 | The investor directory |
| `deals.csv` / `deals.json` | 1376 | Sourced investment deals (the "timeline") |

## Fields — firms

- `name_zh`, `name_en` — firm name (Chinese / English)
- `type`, `type_label`, `subtype` — investor category (VC, family office, CVC, sovereign fund, etc.)
- `region_code`, `region` — primary region (`macau` = Hengqin–Macau cooperation zone incl. Zhuhai; `taiwan` = Hong Kong & Taiwan)
- `public_email`, `email_source` — publicly listed contact email and how it was verified (e.g. official site)
- `website` — official website when known
- `description_zh` — one-paragraph profile (Chinese)
- `web3` — `pure_web3` / `has_web3` / empty
- `sources` — the public sources each entry was verified against
- `deals_in_timeline` — how many of the firm's deals appear in `deals.csv`

## Fields — deals

- `date` (YYYY-MM), `investor`, `project`, `sector_zh`, `category`, `round`, `amount` (as announced)
- `nature` — `equity` (default), `debt`, `mixed`, or `acquisition`; debt-like funding is labelled, never silently counted as equity
- `investor_region`, `investor_in_directory` (`yes`/`no` — 109 deals involve investors outside the 1125-firm directory)
- `source_url` — the public announcement or filing each record is based on

## Citation

If you use this dataset, please cite and link:

> Capy Capital Directory — Open Dataset (October 2026 snapshot). Capy. https://ai.capy-ai.workers.dev/space

Attribution under CC BY 4.0 — a link back to the live directory is appreciated and keeps the data honest.

## Notes

- Amounts are as publicly announced; undisclosed rounds are marked 未披露 (undisclosed).
- This is a snapshot. The live directory is updated continuously and may be ahead of this release.
- Errors: open an issue or write to jeff.nie9104@gmail.com.

---

中文摘要：Capy 资本名录开放数据集（2026 年 10 月 28 日快照）。1125 家投资机构（美国 374／深合区·横琴澳门 196／日本 144／中国 172／港台 114／欧洲 125），615 家带可验证的公开邮箱；1376 条出手记录逐条标注来源，债权类出手单独标注性质。授权 CC BY 4.0，引用请回链线上名录 https://ai.capy-ai.workers.dev/space 。
