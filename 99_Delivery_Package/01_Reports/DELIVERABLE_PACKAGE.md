# AEO + GEO Deliverable Package
## Raleigh Comprehensive & Cosmetic Dentistry

**Prepared by:** [Your name]
**Date:** October 2, 2026
**Project Location:** `AviSanghavi_AEO_GEO/`

---

## THIS IS WHAT YOU DELIVER TO THE CLIENT/TEAM

### Deliverable 1: AEO Change Instructions (for the agency)
**File:** `08_Final_Deliverables/AEO_Change_Instructions.md`
**Format:** Markdown → PDF or send as-is to agency
**Recipient:** The agency that holds the website
**Contains:**
- Current schema state (2 blocks found)
- Exact code changes (delete Block 2, change MedicalClinic → Dentist)
- Open items that need Avi's confirmation before finalizing
- Schema validation steps after implementation

**How to deliver:**
1. Copy the content from `AEO_Change_Instructions.md`
2. Paste into an email or document
3. Send to the agency contact
4. Subject: "Schema update instructions — Raleigh Comprehensive & Cosmetic Dentistry"

---

### Deliverable 2: GEO Visibility Baseline (for internal team)
**File:** `08_Final_Deliverables/GEO_Visibility_Baseline.md`
**Format:** Markdown → PDF for presentation
**Recipient:** Internal team / Avi (with context that this is for planning, not guarantees)
**Contains:**
- Search visibility summary (GSC data)
- AI engine visibility (3 of 4 scans complete)
- Competitive landscape
- Opportunity queries
- Owned channel status

**How to deliver:**
1. Export as PDF (use any markdown-to-PDF tool)
2. Present as "current visibility baseline" — not a ranking promise

---

### Deliverable 3: AEO + GEO Combined Report (master document)
**File:** `08_Final_Deliverables/AEO_GEO_Combined_Report.md`
**Format:** Markdown → PDF (this is the main report)
**Recipient:** Internal team
**Contains:**
- Executive summary
- Part 1: AEO schema baseline & fix plan
- Part 2: GEO visibility baseline
- Part 3: Opportunities & action plan
- Appendices with all file references

---

### Deliverable 4: AI Scan Results
**Files:**
- `07_GEO/ai_answer_scans/consolidated_comparison.md`
- `07_GEO/ai_answer_scans/chatgpt_scan.md`
- `07_GEO/ai_answer_scans/gemini_scan.md`
- `07_GEO/ai_answer_scans/perplexity_scan.md`
- `07_GEO/ai_answer_scans/claude_scan.md` (pending)

**Format:** Individual markdown files + combined comparison
**Recipient:** Internal team
**Contains:**
- Full AI responses for each query
- Whether client was mentioned
- Competitors mentioned
- Sources cited
- Cross-tool comparison

---

### Deliverable 5: GSC Baseline Analysis
**File:** `02_GSC_Analytics/GSC_Baseline_Analysis.md`
**Format:** Markdown → PDF or internal document
**Recipient:** Internal team
**Contains:**
- 10-section analysis of search performance
- 1,000 queries analyzed
- Branded vs non-branded split
- Top opportunity queries
- Page-level analysis

---

## PDF CONVERSION OPTIONS

### Option 1: Free Online
- https://www.markdowntopdf.com/ — paste markdown, get PDF
- https://stackedit.io/ — editor with PDF export
- https://dillinger.io/ — markdown editor with export

### Option 2: VS Code Extension
1. Install "Markdown PDF" extension
2. Open the .md file
3. Ctrl+Shift+P → "Markdown PDF: Export (pdf)"

### Option 3: Command Line
```bash
# If you have pandoc installed:
pandoc AEO_GEO_Combined_Report.md -o AEO_GEO_Report.pdf
pandoc AEO_Change_Instructions.md -o AEO_Change_Instructions.pdf
pandoc GEO_Visibility_Baseline.md -o GEO_Visibility_Baseline.pdf
```

### Option 4: Print to PDF from Browser
1. Open the markdown file in a markdown viewer
2. Ctrl+P → "Save as PDF"

---

## WHAT TO SEND TO WHO

| Document | Recipient | Format | When |
|----------|-----------|--------|------|
| AEO_Change_Instructions | Agency | Email with markdown body | After Avi confirms open items |
| AEO_GEO_Combined_Report | Internal team | PDF | Now (baseline) |
| GEO_Visibility_Baseline | Internal team | PDF | After rank grid complete |
| AI Scan Results | Internal team | PDF | After Claude scan complete |
| GSC Baseline Analysis | Internal team | PDF | Now (already done) |

---

## DELIVERY CHECKLIST

```
AEO TRACK:
  ☐ Send 4 questions to Avi
  ☐ Avi replies with: Friday hours, weekends, social profiles, priceRange, packages
  ☐ Finalize AEO_Change_Instructions.md with confirmed data
  ☐ Send to agency
  ☐ Agency implements
  ☐ Validate schema live

GEO TRACK:
  ☐ Run rank grid (55 queries)
  ☐ Run Claude AI scan
  ☐ Import 119-practice dataset
  ☐ Complete GBP audit (screenshots + inventory)
  ☐ Complete GA4 audit (screenshots only)
  ☐ Complete GTM audit (preview mode only)
  ☐ Set up Bing Webmaster + Bing Places
  ☐ Compile final GEO Visibility Baseline PDF
  ☐ Compile final AEO+GEO Combined Report PDF
```

---

## FILES TO DELIVER (PDF OUTPUTS)

| # | PDF Document | Source File | Status |
|---|-------------|-------------|--------|
| 1 | AEO Change Instructions | `08_Final_Deliverables/AEO_Change_Instructions.md` | ✅ Ready (pending Avi data) |
| 2 | AEO + GEO Combined Report | `08_Final_Deliverables/AEO_GEO_Combined_Report.md` | ✅ Ready (partial GEO) |
| 3 | GEO Visibility Baseline | `08_Final_Deliverables/GEO_Visibility_Baseline.md` | ⏳ After rank grid + Claude scan |
| 4 | GSC Baseline Analysis | `02_GSC_Analytics/GSC_Baseline_Analysis.md` | ✅ Ready |
| 5 | AI Scans Comparison | `07_GEO/ai_answer_scans/consolidated_comparison.md` | ⏳ After Claude scan |
| 6 | ChatGPT Scan Detail | `07_GEO/ai_answer_scans/chatgpt_scan.md` | ✅ Ready |
| 7 | Gemini Scan Detail | `07_GEO/ai_answer_scans/gemini_scan.md` | ✅ Ready |
| 8 | Perplexity Scan Detail | `07_GEO/ai_answer_scans/perplexity_scan.md` | ✅ Ready |
| 9 | Claude Scan Detail | `07_GEO/ai_answer_scans/claude_scan.md` | ⏳ Pending |
| 10 | Bing Setup Guide | `05_BingWebmaster/Bing_Setup_Guide.md` | ✅ Ready |

**Ready to convert:** 6 files
**Pending data:** 4 files (need Claude scan, rank grid, competitive dataset, account audits)
