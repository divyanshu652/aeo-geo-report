# CSV Data Dictionary — Avi Sanghavi Dental

**Data Source:** Google Search Console (GSC)  
**Date Range Covered:** Last 3 months (2026-06-29 to 2026-09-28)  
**Filter:** Web search only  
**Files in this folder:**

---

## Files Overview

| File | Source | Records | Description |
|------|--------|---------|-------------|
| Queries.csv | GSC | 1,000 queries | Top queries with clicks, impressions, CTR, position |
| Pages.csv.xlsx | GSC | 15 pages | Top pages with clicks, impressions, CTR, position |
| Chart.csv | GSC | 93 rows | Daily performance trend (Jun 29 – Sep 28) |
| Search appearance.csv | GSC | 1 row | Header only (no search appearance features detected) |
| Filters.csv | GSC | 2 rows | Metadata: Search type=Web, Date=Last 3 months |
| Countries.csv | GSC | 132 countries | Geographic breakdown of impressions/clicks |
| Devices.csv | GSC | 3 rows | Desktop, Mobile, Tablet breakdown |

---

## Key Findings Summary

### Queries.csv (1,000 queries)
- **Total Clicks:** 259
- **Total Impressions:** 85,713
- **Overall CTR:** 0.30%
- **Queries with at least 1 click:** 38
- **Queries with 0 clicks (impressions only):** 962
- **Avg weighted position:** 16.4
- **Website:** raleighdentistry.com
- **Primary Market:** Raleigh, NC

### Branded vs Non-Branded
- **Branded queries (27):** 2,663 impressions, 207 clicks (80% of all clicks)
- **Non-branded queries (973):** 83,050 impressions, 52 clicks (20% of all clicks)
- **Insight:** Site is almost entirely dependent on branded search. Non-branded visibility is minimal.

### Position Buckets (by impressions)
| Position Range | Impressions | Queries |
|----------------|-------------|---------|
| 1–3 | 1,712 | 33 |
| 4–10 | 31,217 | 185 |
| 11–20 | 31,978 | 240 |
| 20+ | 20,806 | 542 |

### Devices
| Device | Clicks | Impressions | CTR | Avg Position |
|--------|--------|-------------|-----|--------------|
| Desktop | 254 | 94,281 | 0.27% | 22.22 |
| Mobile | 216 | 34,871 | 0.62% | 18.83 |
| Tablet | 1 | 720 | 0.14% | 15.54 |

### Countries
- **United States:** 453 clicks, 126,294 impressions (99.6% of impressions)
- 131 other countries with negligible traffic (0.4%)

### Pages.csv.xlsx (Top Pages)
| Page | Clicks | Impressions | Position |
|------|--------|-------------|----------|
| Homepage (raleighdentistry.com/) | 348 | 101,973 | 22.14 |
| Dr Vraj Gajjar profile | 39 | 945 | 7.31 |
| Dr Courtney Thompson profile | 22 | 572 | 6.14 |
| Meet the Team page | 21 | 1,846 | 43.52 |
| Dr Janaki Barot Gajjar profile | 19 | 385 | 5.95 |
| Contact page | 11 | 2,529 | 45.50 |
| Emergency Dentistry service | 9 | 12,771 | 14.57 |
| Services page | 5 | 1,170 | 19.51 |
| Dental Implants service | 2 | 6,978 | 19.17 |

### Chart.csv (Daily Trend)
- **Date range:** Jun 29, 2026 to Sep 28, 2026 (93 days)
- **Total clicks (Chart):** 471
- **Total impressions (Chart):** 129,872
- **Note:** Chart.csv shows higher totals than Queries.csv — likely different metric definitions or includes broader data
- **Trend:** Avg position worsened from 13.8 (Jun–Sep 15) to 33.9 (Sep 16–Sep 28)

---

## Critical Observations

1. **Branded dominance:** 80% of clicks come from branded queries. Non-branded discovery is nearly zero.
2. **High impressions, zero clicks:** 962 queries have impressions but zero clicks — massive opportunity gap.
3. **Position problem:** Weighted avg position is 16.4 — most visibility is on page 2 of Google.
4. **Position 1-3 queries are all branded:** Only 1,712 impressions are in top 3, and they're all branded.
5. **Homepage dominates:** 101,973 impressions on homepage, but 22.14 avg position — not ranking well for the traffic it gets.
6. **Service pages underperform:** Emergency Dentistry gets 12,771 impressions at pos 14.57 with only 9 clicks. Implants: 6,978 imp at pos 19.17.
7. **Spike in Sep 16+:** Position average jumped from 13.8 to 33.9 — need to investigate what changed.
