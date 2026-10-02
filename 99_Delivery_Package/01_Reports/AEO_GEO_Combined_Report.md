# AEO + GEO Baseline Report — Avi Sanghavi Dental Practice

**Website:** raleighdentistry.com  
**Market:** Raleigh, NC  
**Date:** October 2, 2026  
**Prepared for:** Internal team / Agency coordination  
**Scope:** AEO (Answer Engine Optimization) + GEO (Generative Engine Optimization)  
**Excludes:** SEO (agency's responsibility), client contact, Dentrix advice, migration, calendar integration, performance guarantees

---

## EXECUTIVE SUMMARY

This report establishes the baseline for AEO and GEO work for Avi Sanghavi's dental practice in Raleigh, NC. The analysis covers GSC search data (last 3 months), 119-practice competitive dataset, schema audit requirements, and AI engine visibility measurement plan.

### Key Findings (3 bullets)

1. **Branded search dependency is critical:** 80% of all clicks (207 out of 259) come from just 27 branded queries. Non-branded discovery — where new patients find the practice — generates 96.9% of impressions but only 20% of clicks with a 0.06% CTR.

2. **AI visibility is very low:** Across 4 AI engines (ChatGPT, Gemini, Perplexity, Claude) and 7 patient-intent queries, the practice appears in only 1.25 queries on average (17.9% mention rate). Only appears for brand queries and emergency (ChatGPT only). Completely absent from discovery queries in all 4 tools.

3. **GBP has strong engagement but wrong visibility drivers:** 26,918 profile views and 216 phone calls in 6 months with 4.7/5 stars — but the top search queries driving GBP visibility are competitor names ("lane and associates", "riccobene associates") rather than the practice's own name. 91 reviews is healthy but competitors have 200-800+.

### Recommended Next Actions

1. **Immediate (AEO):** Send Avi 2 questions (Friday hours + treatment packages), then send AEO change instructions to agency
2. **Short-term (GEO):** Complete GBP fixes (NAAP, categories, services, photos, posts), run rank grid (55 queries), finish Claude scan
3. **Ongoing:** GA4 audit, GTM audit, Bing setup, import 119-practice dataset

---

## PART 1: AEO — SCHEMA BASELINE & FIX PLAN

### Current State (from live inspection)
- **Block 1 (@graph):** WebSite + MedicalClinic + WebPage + BreadcrumbList
  - MedicalClinic type → needs to change to Dentist
  - All other properties are valid and well-structured
- **Block 2 (array):** Organization + LocalBusiness + WebSite + WebPage
  - **BROKEN** — malformed @id URLs (`https://#org`, `https://#site`, `https:///locations#loc-0`)
  - Broken url fields (`https://` with no domain)
  - **Action: DELETE entirely**

### Confirmed Data
| Field | Value |
|-------|-------|
| Practice Name | Raleigh Comprehensive & Cosmetic Dentistry |
| Phone | (919) 828-3775 |
| Address | 119 North Boylan Avenue, Raleigh, NC 27603 |
| Geo | 35.782684, -78.6494414 |
| Mon-Thu Hours | 08:00-17:00 |
| Friday Hours | 08:00-17:00 (⚠️ site says "every other Friday") |
| priceRange | $$$ |
| sameAs | Google Maps only |
| Logo | https://einstein-clients.imgix.net/8112/494844/original.svg?1767899842 |

### Recommended Changes
1. Delete Block 2 entirely (broken Organization array)
2. Change Block 1: `"@type": "MedicalClinic"` → `"@type": "Dentist"`
3. Fix Friday hours after Avi confirms
4. Add Saturday/Sunday hours
5. Add social sameAs profiles after Avi confirms

**Full instructions:** See `08_Final_Deliverables/AEO_Change_Instructions.md`

### Open Items (DO NOT implement until confirmed)

| Item | Issue | Who Confirms |
|------|-------|-------------|
| Friday hours | Site says 8-5 but also "every other Friday" | Avi / practice manager |
| Social sameAs profiles | Unknown which profiles exist | Avi |
| Practice name | Need exact registered name | Avi |
| Phone/address/ZIP | Need NAP data | Avi |
| Services list | Partial — need confirmation | Avi |

---

## PART 2: GEO — VISIBILITY BASELINE

### 2.1 Google Search Visibility

| Metric | Value |
|--------|-------|
| Total Queries | 1,000 |
| Total Clicks | 259 |
| Total Impressions | 85,713 |
| Overall CTR | 0.30% |
| Avg Position | 16.4 |
| Queries with clicks | 38 |
| Queries with 0 clicks | 962 |

### Branded vs Non-Branded

| Type | Impressions | Clicks | CTR | Position |
|------|-------------|--------|-----|----------|
| Branded | 2,663 | 207 | 7.77% | 4.8 |
| Non-Branded | 83,050 | 52 | 0.06% | 16.8 |

### Top 10 Queries by Clicks
1. raleigh comprehensive dentistry — 86 clicks, pos 1.1
2. raleigh comprehensive and cosmetic dentistry — 75 clicks, pos 1.3
3. raleigh comprehensive & cosmetic dentistry — 23 clicks, pos 1.2
4. dentist raleigh nc — 8 clicks, pos 8.4
5. raleigh cosmetic dentistry — 8 clicks, pos 18.9
6. dr gajjar dentist — 5 clicks, pos 5.2
7. courtney thompson dds — 5 clicks, pos 1.8
8. raleigh dentist — 4 clicks, pos 7.3
9. raleigh comprehensive dentistry reviews — 4 clicks, pos 2.9
10. raleigh dentistry — 3 clicks, pos 3.0

### Top 10 Opportunity Queries (High Impressions, 0 Clicks)
1. dental implants raleigh nc — 1,528 imp, pos 20.0
2. cosmetic dentist raleigh — 1,208 imp, pos 8.0
3. emergency dentist raleigh nc — 1,204 imp, pos 13.3
4. emergency dentist — 1,081 imp, pos 15.4
5. comprehensive dental care — 1,044 imp, pos 17.8
6. cosmetic dentistry raleigh nc — 1,027 imp, pos 14.0
7. cosmetic dentist near me — 832 imp, pos 13.6
8. dentists raleigh — 690 imp, pos 13.7
9. raleigh dentists — 641 imp, pos 12.9
10. family dentist near me — 678 imp, pos 28.9

### 2.2 AI Engine Visibility

**Status:** Complete — 4 of 4 scans (ChatGPT, Gemini, Perplexity, Claude).

| Tool | Queries Run | Mentions | Mention Rate |
|------|------------|----------|-------------|
| ChatGPT | 7/7 | 2 | 28.6% |
| Gemini | 7/7 | 1 | 14.3% |
| Perplexity | 7/7 | 1 | 14.3% |
| Claude | 7/7 | 1 | 14.3% |
| **Average** | — | **1.25** | **17.9%** |

**Where client appears:**
- ✅ Q7 (brand query) — all 4 tools
- ✅ Q3 (emergency) — ChatGPT only
- ⚠️ Q2 (implants) — ChatGPT only (weak)
- ⚠️ Q5 (cosmetic) — ChatGPT only (weak)
- ❌ Q1, Q4, Q6 — not mentioned in any tool

**Key insight:** Claude surfaces the most competitor names per query (20+ per query) from directory sources (ADA, Lantern, Birdeye, WebMD). Client's "Cosmetic" in name didn't help for cosmetic-intent queries. ZIP mismatch (27603 vs 27606) confirmed as a factor by Perplexity.

**See:** `07_GEO/ai_answer_scans/consolidated_comparison.md` for full details

### 2.3 Competitive Position

**Status:** Partial — 119-practice dataset template ready, awaiting import.

**Competitors identified from all sources (GSC + AI scans):**

| Competitor | Source | Notable Data |
|-----------|--------|-------------|
| Lane & Associates | GSC (top query), AI | 943 GBP impressions for "lane and associates" |
| Riccobene Associates | GSC | 559 GBP impressions |
| Raleigh Periodontics | GSC | 347 GBP impressions |
| Raleigh Dental Arts | ChatGPT, Claude | 8304 Creedmoor Rd |
| Smiles at Glenwood | All 4 AI tools | 601 Tucker St |
| City of Oaks Dental | All 4 AI tools | Invisalign, veneers, CEREC |
| Raleigh Dental Loft (Dr. Kashyap) | ChatGPT, Gemini, Perplexity | 1601 Jones Franklin Rd, 27606 |
| University Dental Associates | ChatGPT, Perplexity | 801 Jones Franklin Rd |
| Raleigh Implant & Family Dentistry | Claude, Perplexity | 4.9/197 Birdeye |
| Sedation Dental Care at Raleigh Smile Center | Claude, Perplexity | 5.0/421 Birdeye |
| Gentle Smiles of Raleigh | Claude, Perplexity | 5.0/510 reviews |
| Koneru Family Dentistry | ChatGPT | 4.9/746 reviews, 4703 Western Blvd |
| Russo Dentistry (Justin Russo) | ChatGPT, Gemini, Perplexity | AACD member |
| Tryon Family Dentistry | Claude, Perplexity | 4.55/62 reviews, 2720 Lake Wheeler Rd |
| Village Dental North Raleigh | Claude, Perplexity | 4.8/87 reviews |
| Wells Family Dental Group | ChatGPT, Gemini | — |
| Fusion Dental Care | ChatGPT, Claude | — |
| Sebastian & Spaulding | ChatGPT | 7722 Chapel Hill Rd |
| Jenny Su DMD | ChatGPT, Claude, Perplexity | Family & Cosmetic |
| ClearChoice Raleigh | GSC | Implant center |
| Courtney Thompson DDS | GSC | — |

**Most persistent competitors across AI tools:** Smiles at Glenwood, City of Oaks Dental (all 4 tools each)

### 2.4 Owned Channel Baseline

| Channel | Status | Data |
|---------|--------|------|
| GSC | ✅ Complete | 1,000 queries, 259 clicks, 85,713 impressions |
| GBP | ✅ Audited | 91 reviews, 4.7/5, 26,918 views, 216 calls, 341 clicks |
| GA4 | ⏳ Pending | Manual audit required |
| GTM | ⏳ Pending | Manual audit required |
| Bing Webmaster | ⏳ Not set up | Held for Avi verification |
| Bing Places | ⏳ Not set up | Held for Avi verification |

**GBP Key Metrics:**
- 26,918 profile views (6 months)
- 66% from mobile Google Search
- 216 phone calls, 341 website clicks
- Top queries: competitor names dominate ("lane and associates", "riccobene")
- 4.7/5 stars, 91 reviews

---

## PART 3: OPPORTUNITIES & ACTION PLAN

### Immediate (AEO — Week 2)

| # | Action | Owner | Blocker |
|---|--------|-------|---------|
| 1 | Send Avi 2 questions (Friday hours + treatment packages) | You | — |
| 2 | Avi replies with confirmed data | Avi | #1 |
| 3 | Finalize AEO_Change_Instructions.md with confirmed data | You | #2 |
| 4 | Agency implements schema changes (delete Block 2, change MedicalClinic → Dentist) | Agency | #3 |
| 5 | Validate schema after implementation | Agency / You | #4 |

### Short-term (GEO — Weeks 2–4)

| # | Action | Owner | Time | Blocker |
|---|--------|-------|------|---------|
| 6 | Fix GBP: categories, services, photos, description, hours, NAP | You | 60 min | Avi confirms Friday hours |
| 7 | Fix external directories: Yelp, WebMD, ADA, Lantern, DentaScore | You | 30 min | — |
| 8 | Run rank grid (55 queries, desktop + mobile, incognito) | You | 2-3 hrs | None |
| 9 | Complete GA4 audit (screenshots, fill inventory) | You | 30 min | GA4 access |
| 10 | Complete GTM audit (preview mode, fill inventory) | You | 30 min | GTM access |
| 11 | Import 119-practice competitive dataset | You | 30 min | Dataset file |
| 12 | Set up Bing Webmaster + Bing Places | You | 15 min | Avi verification |

### Ongoing (Measurement Cadence)

| Activity | Frequency | Owner |
|----------|-----------|-------|
| GBP posts | Weekly | You |
| Review monitoring & responses | Weekly | You |
| AI answer scan | Monthly | You |
| Rank grid refresh | Monthly | You |
| GA4 review | Monthly | You |
| GTM tag audit | Quarterly | You |
| Schema validation | After each site change | Agency |

---

## APPENDIX

### A. File Locations

| Document | Path |
|----------|------|
| CSV Data Dictionary | `01_CSV_Exports/CSV_Data_Dictionary.md` |
| GSC Baseline Analysis | `02_GSC_Analytics/GSC_Baseline_Analysis.md` |
| GTM Inventory | `03_GTM/GTM_Tag_Inventory.md` |
| GBP Inventory | `04_GBP/GBP_Data_Inventory.md` |
| GBP Profile Data | `04_GBP/profile_data.json` |
| Bing Inventory | `05_BingWebmaster/Bing_Data_Inventory.md` |
| Schema Audit | `06_AEO_Schema/current_schema_audit.md` |
| Recommended Schema | `06_AEO_Schema/recommended_jsonld.md` |
| Schema Change Instructions | `06_AEO_Schema/schema_change_instructions.md` |
| Competitive Raw Data | `07_GEO/competitive_dataset/raw_data.json` |
| Competitive Analysis | `07_GEO/competitive_dataset/competitive_analysis.md` |
| Rank Grid Queries | `07_GEO/rank_grid/queries_defined.md` |
| Rank Grid Results | `07_GEO/rank_grid/rank_grid_results.md` |
| AI Scan: ChatGPT | `07_GEO/ai_answer_scans/chatgpt_scan.md` |
| AI Scan: Gemini | `07_GEO/ai_answer_scans/gemini_scan.md` |
| AI Scan: Perplexity | `07_GEO/ai_answer_scans/perplexity_scan.md` |
| AI Scan: Claude | `07_GEO/ai_answer_scans/claude_scan.md` |
| AEO Change Instructions (Final) | `08_Final_Deliverables/AEO_Change_Instructions.md` |
| GEO Visibility Baseline | `08_Final_Deliverables/GEO_Visibility_Baseline.md` |

### B. Constraints

- No client contact from the team
- No Dentrix upgrade advice
- No migration pitch
- No shared-calendar ask
- No new desk habits
- No absolute performance claims in client-facing materials
- No touching agency's SEO work
- No modifying GA4/GTM/GBP settings (document only)
