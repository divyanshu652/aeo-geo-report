# Bing Webmaster Tools — Setup Guide

**Status:** Not yet set up for raleighdentistry.com
**Date:** October 2, 2026
**Action:** Create Bing Webmaster Tools account and verify site

---

## WHY BING WEBMASTER MATTERS

- Bing powers ~30-40% of US desktop search
- Bing data provides additional visibility into search performance
- Bing and Google data can differ — useful for cross-validation
- Bing Webmaster is free and takes ~10 minutes to set up

---

## SETUP STEP-BY-STEP

### Step 1: Create Account

1. Go to https://www.bing.com/webmasters
2. Sign in with Microsoft account (or create one)
3. Click "Import from Google Search Console" (easiest method)

### Step 2: Import from GSC

1. Click "Import from Google Search Console"
2. Sign in to the Google account that has access to raleighdentistry.com GSC
3. Select raleighdentistry.com property
4. Authorize Bing to access GSC data
5. Bing will import:
   - Verified site ownership
   - Sitemap data
   - Search performance history
   - Crawl data

### Step 3: Verify Site Ownership (if not auto-verified)

If import doesn't auto-verify, choose one method:

**Option A: XML File Verification (Recommended)**
1. Download the Bing verification XML file
2. Upload to root of raleighdentistry.com (via FTP/cPanel/hosting)
3. Click "Verify" in Bing Webmaster

**Option B: Meta Tag Verification**
1. Copy the meta tag Bing provides
2. Add to homepage `<head>` section
3. Click "Verify"

**Option C: CNAME Record Verification**
1. Add CNAME record to DNS
2. Click "Verify"

### Step 4: Submit Sitemap

1. In Bing Webmaster, go to "Sitemaps"
2. Submit sitemap URL: `https://www.raleighdentistry.com/sitemap.xml`
3. Or use GSC sitemap if already submitted there
4. Bing will pull sitemap from GSC if imported

### Step 5: Configure Basic Settings

1. **Crawl Settings:**
   - Set crawl rate to "Let Bing decide" (default)
   - Check "Crawl as Googlebot" for comparison data

2. **URL Inspection:**
   - Submit homepage URL for indexing
   - Submit key pages: /contact, /services, /services/emergency-dentistry/

3. **Robots.txt:**
   - Review robots.txt for any blocked pages
   - Ensure no important pages are blocked

---

## WHAT TO DOCUMENT (After Setup)

Once Bing Webmaster is set up, document:

| Metric | Where to Find | What to Record |
|--------|--------------|----------------|
| Verified sites | Site list | Confirm raleighdentistry.com shows as verified |
| Sitemap status | Sitemaps section | Submitted? Indexed? Errors? |
| Crawl data | Crawl section | Pages crawled, crawl errors |
| Search performance | Reports → Search performance | Impressions, clicks, CTR, position |
| Top queries | Queries section | Top 10 queries |
| Top pages | Pages section | Top 10 pages |
| Index status | Index section | Indexed pages, removed pages, blocked pages |

---

## COMPARISON: Bing vs Google Data

After setup, compare:

| Metric | Google (GSC) | Bing (if available) | Notes |
|--------|-------------|---------------------|-------|
| Total Impressions | 85,713 | [Bing value] | May differ significantly |
| Total Clicks | 259 | [Bing value] | |
| Avg Position | 16.4 | [Bing value] | |
| Top Queries | [list] | [list] | May show different queries |
| Indexed Pages | [check] | [Bing value] | Bing may have different index |

---

## ONGOING BING MONITORING

| Activity | Frequency | What to Check |
|----------|-----------|---------------|
| Crawl errors | Weekly | Any new crawl errors in Bing |
| Index status | Monthly | Pages indexed, removed |
| Search performance | Monthly | Compare with GSC trends |
| Sitemap status | After each site change | Re-submit sitemap after major updates |

---

## BING-SPECIFIC SEO CONSIDERATIONS

1. **Bing values different signals than Google:**
   - Social signals may carry more weight
   - Exact match domains may have different impact
   - Page authority metrics may differ

2. **Bing Local:**
   - Similar to Google Local Pack
   - Ensure NAP consistency
   - Claim/verify Bing Places for Business

3. **Bing Webmaster vs Bing Places:**
   - Bing Webmaster Tools = search performance data
   - Bing Places for Business = local business listing (like GBP)

---

## BING PLACES FOR BUSINESS

Consider also setting up Bing Places:
1. Go to https://www.bingplaces.com/
2. Sign in with Microsoft account
3. Search for "Raleigh Comprehensive & Cosmetic Dentistry"
4. Claim the listing or create new
5. Fill in: business name, address, phone, hours, services, photos
6. Verify via phone, email, or mail

This ensures Avi's practice appears in Bing's local search results.
