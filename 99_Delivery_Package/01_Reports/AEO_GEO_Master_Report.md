# AEO + GEO Master Report
## Raleigh Comprehensive & Cosmetic Dentistry

**Date:** October 2, 2026
**Updated:** GA4 + GTM access received — live audits ready to execute

---

# COMPLETED DELIVERABLES

| # | Deliverable | File | Status |
|---|-------------|------|--------|
| 1 | GSC Baseline Analysis | `03_GEO_Data/GSC_Baseline_Analysis.md` | Done |
| 2 | CSV Data Dictionary | `01_CSV_Exports/CSV_Data_Dictionary.md` | Done |
| 3 | Schema Audit | `06_AEO_Schema/current_schema_audit.md` | Done |
| 4 | AEO Change Instructions | `02_AEO_Schema/AEO_Change_Instructions.md` | Done |
| 5 | GBP Data Inventory | `04_GBP/GBP_Data_Inventory.md` | Done |
| 6 | GBP Profile Data | `04_GBP/profile_data.json` | Done |
| 7 | AI Scan — ChatGPT | `07_GEO/ai_answer_scans/chatgpt_scan.md` | Done |
| 8 | AI Scan — Gemini | `07_GEO/ai_answer_scans/gemini_scan.md` | Done |
| 9 | AI Scan — Perplexity | `07_GEO/ai_answer_scans/perplexity_scan.md` | Done |
| 10 | AI Scan — Claude | `07_GEO/ai_answer_scans/claude_scan.md` | Done |
| 11 | AI Comparison Matrix | `07_GEO/ai_answer_scans/consolidated_comparison.md` | Done |
| 12 | Rank Grid Queries | `07_GEO/rank_grid/queries_defined.md` | Done |
| 13 | Rank Grid Spreadsheet | `07_GEO/rank_grid/rank_grid_spreadsheet.csv` | Done |
| 14 | Competitive Dataset | `07_GEO/competitive_dataset/raw_data.json` | Done |
| 15 | **GA4 Live Audit Kit** | `02_GA4_Audit/GA4_Live_Audit_Kit.md` | **Ready to execute** |
| 16 | **GTM Live Audit Kit** | `03_GTM/GTM_Live_Audit_Kit.md` | **Ready to execute** |
| 17 | Bing Setup Guide | `05_BingWebmaster/Bing_Setup_Guide.md` | Done |
| 18 | AEO + GEO Report (for Avi) | `08_Final_Deliverables/AEO_GEO_Report_For_Avi.docx` | Done |
| 19 | Master Report | `08_Final_Deliverables/AEO_GEO_Master_Report.md` | Done |
| 20 | Analytics Dashboard | `99_Delivery_Package/analytics_dashboard.html` | Done |

---

# PART 1: AEO — SCHEMA

## Current State

Two JSON-LD blocks exist on the homepage:

**Block 1 — Valid, one change needed:**
- Contains: WebSite, MedicalClinic, WebPage, BreadcrumbList
- Change: `MedicalClinic` → `Dentist`

**Block 2 — Broken, must be deleted:**
- Contains: Organization, LocalBusiness, WebSite, WebPage
- Issues: broken @id URLs, broken url fields

## Required Changes

| # | Action | Detail |
|---|--------|--------|
| 1 | Delete Block 2 | Entire second `<script type="application/ld+json">` block |
| 2 | Change type | `MedicalClinic` → `Dentist` in Block 1 |
| 3 | Update Friday hours | After Avi confirms schedule |
| 4 | Add social sameAs | After Avi provides URLs |

## Open Items

| Item | Status |
|------|--------|
| Friday hours | Awaiting Avi |
| Treatment packages | Awaiting Avi |
| Social profiles | Avi will add later |

---

# PART 2: GEO — VISIBILITY BASELINE

## 2.1 Google Search (GSC)

### Overall
| Metric | Value |
|--------|-------|
| Total Queries | 1,000 |
| Total Clicks | 259 |
| Total Impressions | 85,713 |
| Overall CTR | 0.30% |
| Avg Position | 16.4 |

### Branded vs Non-Branded
| Type | Queries | Impressions | Clicks | CTR | Position |
|------|---------|-------------|--------|-----|----------|
| Branded | 27 | 2,663 | 207 | 7.77% | 4.8 |
| Non-Branded | 973 | 83,050 | 52 | 0.06% | 16.8 |

### By Device
| Device | Clicks | Impressions | CTR | Position |
|--------|--------|-------------|-----|----------|
| Desktop | 254 | 94,281 | 0.27% | 22.2 |
| Mobile | 216 | 34,871 | 0.62% | 18.8 |
| Tablet | 1 | 720 | 0.14% | 15.5 |

### By Country (Top 5)
| Country | Clicks | Impressions | CTR | Position |
|---------|--------|-------------|-----|----------|
| United States | 453 | 126,294 | 0.36% | 21.2 |
| India | 4 | 418 | 0.96% | 31.6 |
| Pakistan | 3 | 79 | 3.80% | 15.2 |
| Philippines | 2 | 90 | 2.22% | 22.3 |
| Nigeria | 2 | 25 | 8.00% | 17.5 |

### Top 10 Queries by Clicks
| # | Query | Clicks | Position |
|---|-------|--------|----------|
| 1 | raleigh comprehensive dentistry | 86 | #1 |
| 2 | raleigh comprehensive and cosmetic dentistry | 75 | #1 |
| 3 | raleigh comprehensive & cosmetic dentistry | 23 | #1 |
| 4 | dentist raleigh nc | 8 | #8 |
| 5 | raleigh cosmetic dentistry | 8 | #19 |
| 6 | dr gajjar dentist | 5 | #5 |
| 7 | courtney thompson dds | 5 | #1 |
| 8 | raleigh dentist | 4 | #7 |
| 9 | raleigh comprehensive dentistry reviews | 4 | #3 |
| 10 | raleigh dentistry | 3 | #3 |

### Top 10 Opportunity Queries
| # | Query | Impressions | Position | Opportunity |
|---|-------|-------------|----------|-------------|
| 1 | dental implants raleigh nc | 1,528 | #20 | HIGH |
| 2 | cosmetic dentist raleigh | 1,208 | #8 | MEDIUM |
| 3 | emergency dentist raleigh nc | 1,204 | #13 | MEDIUM |
| 4 | emergency dentist | 1,081 | #15 | MEDIUM |
| 5 | comprehensive dental care | 1,044 | #18 | MEDIUM |
| 6 | cosmetic dentistry raleigh nc | 1,027 | #14 | MEDIUM |
| 7 | cosmetic dentist near me | 832 | #14 | MEDIUM |
| 8 | dentists raleigh | 690 | #14 | MEDIUM |
| 9 | raleigh dentists | 641 | #13 | MEDIUM |
| 10 | family dentist near me | 678 | #29 | HIGH |

---

## 2.2 AI Engine Visibility

### Results Matrix
| Query | ChatGPT | Gemini | Perplexity | Claude |
|-------|---------|--------|-----------|--------|
| Dentists near 27606 | ❌ | ❌ | ❌ | ❌ |
| Best dentist for implants near 27606 | ⚠️ | ❌ | ❌ | ❌ |
| Emergency dentist near 27606 | ✅ | ❌ | ❌ | ❌ |
| Good family dentist in Raleigh | ❌ | ❌ | ❌ | ❌ |
| Best cosmetic dentist near 27606 | ⚠️ | ❌ | ❌ | ❌ |
| Dentist with good reviews in Raleigh | ❌ | ❌ | ❌ | ❌ |
| What do patients say about Raleigh Comprehensive... | ✅ | ✅ | ✅ mixed | ✅ mixed |

**Average: 1.25 / 7 = 17.9% mention rate**

### Key Findings
- All 4 AI engines know the practice by name
- 0% mention rate for discovery queries (dentists near me, family dentist, etc.)
- ChatGPT is the most visible engine (28.6%)
- All 4 tools pull from same directory sources (ADA, Lantern, Birdeye, WebMD)

---

## 2.3 GBP Performance

| Metric | Value |
|--------|-------|
| Total Views (6 months) | 26,918 |
| Search Views | 6,312 |
| Map Views | 1,493 |
| Website Clicks | 341 |
| Phone Calls | 216 |
| Avg Rating | 4.7 / 5 |
| Total Reviews | 91 |

### Top GBP Queries
| # | Query | Appearances |
|---|-------|------------|
| 1 | lane and associates | 943 |
| 2 | lane and associates raleigh | 573 |
| 3 | riccobene associates family dentistry | 559 |
| 4 | dentist near me | 544 |
| 5 | raleigh periodontics | 347 |

---

## 2.4 Competitors

| Competitor | AI Mentions | Notable |
|-----------|-------------|---------|
| Smiles at Glenwood | 4/4 | 601 Tucker St |
| City of Oaks Dental | 4/4 | Invisalign, veneers, CEREC |
| Raleigh Dental Loft | 3/4 | 1601 Jones Franklin Rd |
| Russo Dentistry | 3/4 | AACD member |
| Koneru Family Dentistry | 1/4 | 4.9/746 reviews |
| Gentle Smiles of Raleigh | 2/4 | 5.0/510 reviews |

---

# PART 3: GA4 + GTM — READY TO EXECUTE

## GA4 Audit

**Status:** Access granted, audit kit ready

**What we'll capture:**
- Property info (ID, measurement ID, data stream settings)
- Traffic overview (users, sessions, engagement, bounce rate)
- Traffic acquisition (organic vs direct vs referral vs social)
- Top landing pages (which pages bring patients)
- All events (standard + custom)
- All conversions
- Demographics (country, city, device, language)
- Enhanced measurement settings
- Data filters, data retention, Google Signals

**File:** `02_GA4_Audit/GA4_Live_Audit_Kit.md` — step-by-step guide with copy-paste tables

**Time required:** 15-20 minutes

## GTM Audit

**Status:** Access granted, audit kit ready

**What we'll capture:**
- Container info (ID, workspace, last published)
- All tags (GA4 config, event tags, custom tags)
- All triggers (page view, click, form, scroll, custom)
- All variables (built-in + custom)
- Preview mode test: phone click, form submit, scroll, outbound links
- GA4 integration status
- Custom HTML/JS code
- Folders and organization

**File:** `03_GTM/GTM_Live_Audit_Kit.md` — step-by-step guide with checklists

**Time required:** 15-20 minutes

## How to Execute

1. Open `02_GA4_Audit/GA4_Live_Audit_Kit.md` in one tab
2. Open `03_GTM/GTM_Live_Audit_Kit.md` in another tab
3. Open GA4 in one browser window
4. Open GTM in another browser window
5. Follow each section, fill in the tables
6. Send both filled files back

---

# PART 4: WHAT REMAINS

| # | Task | Status | Blocker |
|---|------|--------|---------|
| 1 | Schema fix sent to agency | Ready, waiting for Avi's Friday hours + packages | Avi |
| 2 | GBP fixes (categories, services, photos, posts) | Ready to execute | Friday hours |
| 3 | External directories (Yelp, WebMD, ADA, Lantern) | Ready to execute | — |
| 4 | **GA4 live audit** | **Kit ready, access granted** | — |
| 5 | **GTM live audit** | **Kit ready, access granted** | — |
| 6 | Rank grid (55 queries, 9 locations, 2 devices) | Spreadsheet ready, in progress | — |
| 7 | Bing Webmaster + Bing Places | Guide ready | Avi verification |
| 8 | Competitive dataset compilation | Template ready | 119-practice CSV |
| 9 | llms.txt implementation | Recommended | — |
| 10 | FAQ page | Recommended | — |
| 11 | Service-specific landing pages | Recommended | — |

---

# PART 5: RECOMMENDATIONS

## AEO Improvements
1. Add llms.txt to website root
2. Add llms-full.txt (comprehensive version)
3. Create FAQ page with common patient questions
4. Add service-specific landing pages
5. Optimize website content for AI
6. Ensure consistent NAP across all pages
7. Implement schema.org on all pages

## GEO Improvements
1. Claim and optimize all directory listings (ADA, Lantern, Birdeye, DentaScore, etc.)
2. Increase review count to 150+ at 4.5+ stars
3. Start weekly GBP posts (2-3 per week)
4. Add GBP Products for key services
5. Add GBP Q&A content
6. Add service area ZIP codes to GBP
7. Set up Bing Webmaster + Bing Places
8. Create and submit XML sitemap

---

# PART 6: PROJECT STRUCTURE

```
AviSanghavi_AEO_GEO/
├── 01_CSV_Exports/
│   ├── Chart.csv              — Daily GSC data
│   ├── Countries.csv          — GSC by country
│   ├── Devices.csv            — GSC by device
│   ├── Filters.csv            — GSC filters
│   ├── Queries.csv            — GSC queries
│   ├── Search appearance.csv  — GSC search features
│   └── CSV_Data_Dictionary.md — Analysis
│
├── 02_GA4_Audit/
│   ├── GA4_Data_Inventory.md      — Template (blank)
│   └── GA4_Live_Audit_Kit.md      ← ACTIVE — fill this with live data
│
├── 02_GSC_Analytics/
│   └── GSC_Baseline_Analysis.md   — Full GSC analysis
│
├── 03_GTM/
│   ├── GTM_Tag_Inventory.md       — Template (blank)
│   └── GTM_Live_Audit_Kit.md      ← ACTIVE — fill this with live data
│
├── 04_GBP/
│   ├── GBP_Data_Inventory.md      — GBP audit with real data
│   └── profile_data.json          — GBP data JSON
│
├── 05_BingWebmaster/
│   └── Bing_Setup_Guide.md        — Bing setup instructions
│
├── 06_AEO_Schema/
│   ├── current_schema_audit.md    — Schema inspection results
│   └── AEO_Change_Instructions.md — For agency (after Avi replies)
│
├── 07_GEO/
│   ├── ai_answer_scans/           — ChatGPT, Gemini, Perplexity, Claude
│   ├── competitive_dataset/       — 119 practices, 6,138 reviews
│   └── rank_grid/                 — 55 queries, 990 rows
│
├── 08_Final_Deliverables/
│   ├── AEO_GEO_Report_For_Avi.docx — Client report (Word)
│   ├── AEO_GEO_Master_Report.md    — This file
│   └── AEO_GEO_Combined_Report.md  — Combined analysis
│
└── 99_Delivery_Package/
    ├── README.txt
    ├── analytics_dashboard.html    — Visual dashboard
    └── [organized folders with all deliverables]
```
