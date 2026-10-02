# AEO Change Instructions — Avi Sanghavi Dental
### Final Deliverable for Agency Implementation

**Prepared for:** Site Agency
**Date:** October 2, 2026
**Priority:** High
**Website:** raleighdentistry.com

---

## EXECUTIVE SUMMARY

The website has 2 JSON-LD blocks on the homepage. Block 1 uses `MedicalClinic` type — needs to change to `Dentist`. Block 2 is completely broken (malformed URLs, broken entity references) — must be deleted entirely.

**Implementation time: ~10 minutes**

---

## CHANGE 1: Delete Block 2 (Broken)

**Action:** Remove the second JSON-LD block from the homepage.

**How to identify Block 2:**
- Starts with `[` (it's an array, not a single object)
- Contains `"@type": "Organization"` with `"@id": "https://#org"` (broken URL)
- Has broken fields: `"url": "https://"` and `"image": "https:///_cache/..."`
- Contains nested entities with `"@id": "https://#site"` and `"https:///locations#loc-0"`

**How to implement:**
1. Find the template/header file where JSON-LD is injected
2. Remove the entire second `<script type="application/ld+json">` block
3. Verify: only 1 JSON-LD block remains

---

## CHANGE 2: Change MedicalClinic to Dentist

**In the remaining Block 1 (@graph), change one line:**

FIND:
```json
"@type": "MedicalClinic",
```

REPLACE WITH:
```json
"@type": "Dentist",
```

Everything else in Block 1 is valid and should remain unchanged.

---

## FULL CORRECT BLOCK 1 (After Changes)

For reference, here's what Block 1 should look like after the fix:

```json
{
  "@context": "https://schema.org",
  "@graph": [
    {
      "@type": "WebSite",
      "@id": "https://www.raleighdentistry.com/#website",
      "url": "https://www.raleighdentistry.com/",
      "name": "Raleigh Comprehensive & Cosmetic Dentistry"
    },
    {
      "@type": "Dentist",
      "@id": "https://www.raleighdentistry.com/#practice",
      "name": "Raleigh Comprehensive & Cosmetic Dentistry",
      "description": "Raleigh Comprehensive & Cosmetic Dentistry is a dental practice with an office in Raleigh, NC.",
      "url": "https://www.raleighdentistry.com/",
      "telephone": "(919) 828-3775",
      "image": "https://einstein-clients.imgix.net/8112/494844/original.svg?1767899842",
      "logo": "https://einstein-clients.imgix.net/8112/494844/original.svg?1767899842",
      "priceRange": "$$$",
      "address": {
        "@type": "PostalAddress",
        "streetAddress": "119 North Boylan Avenue",
        "addressLocality": "Raleigh",
        "addressRegion": "NC",
        "postalCode": "27603",
        "addressCountry": "US"
      },
      "geo": {
        "@type": "GeoCoordinates",
        "latitude": 35.782684,
        "longitude": -78.6494414
      },
      "openingHoursSpecification": [
        {
          "@type": "OpeningHoursSpecification",
          "dayOfWeek": ["Monday", "Tuesday", "Wednesday", "Thursday"],
          "opens": "08:00",
          "closes": "17:00"
        },
        {
          "@type": "OpeningHoursSpecification",
          "dayOfWeek": ["Friday"],
          "opens": "08:00",
          "closes": "17:00"
        }
      ],
      "sameAs": [
        "https://www.google.com/maps?cid=15003956664647858033"
      ]
    },
    {
      "@type": "WebPage",
      "@id": "https://www.raleighdentistry.com/#webpage",
      "url": "https://www.raleighdentistry.com/",
      "name": "Dentist in Raleigh, NC | Raleigh Comprehensive & Cosmetic Dentistry",
      "description": "Looking for expert dental care in Raleigh? Our trusted team offers general, cosmetic, and restorative services with advanced technology and a personalized touch.",
      "isPartOf": {
        "@id": "https://www.raleighdentistry.com/#website"
      },
      "about": {
        "@id": "https://www.raleighdentistry.com/#practice"
      }
    },
    {
      "@type": "BreadcrumbList",
      "@id": "https://www.raleighdentistry.com/#breadcrumbs",
      "itemListElement": [
        {
          "@type": "ListItem",
          "position": 1,
          "name": "Home",
          "item": {
            "@id": "https://www.raleighdentistry.com/#webpage"
          }
        }
      ]
    }
  ]
}
```

---

## ⚠️ OPTIONAL ITEMS (Pending Avi Confirmation)

| Item | Current Value | What to Do After Confirmation |
|------|--------------|-------------------------------|
| Friday hours | 08:00-17:00 | Confirm with Avi — site mentions "every other Friday" |
| Saturday/Sunday | Not specified | Add or mark as closed |
| Social sameAs | Only Google Maps | Add LinkedIn, Facebook, Instagram, X after Avi confirms |
| priceRange | $$$ | Confirm accuracy |
| aggregateRating | Not present | Add from GBP after GBP audit |

---

## VALIDATION (After Implementation)

1. **Chrome Console:**
```javascript
const scripts = document.querySelectorAll('script[type="application/ld+json"]');
scripts.forEach((script, i) => {
  try {
    const data = JSON.parse(script.textContent);
    console.log(`Block ${i+1}:`, data['@graph']?.map(e => e['@type']) || data['@type']);
  } catch(e) { console.log(`Block ${i+1}: ERROR`); }
});
```
Expected: 1 block, types include "Dentist", no errors.

2. **Page Source:** Confirm no `MedicalClinic`, no `Organization`, no `https://#org`
3. **Schema.org Validator:** https://validator.schema.org/ → 0 errors
4. **Google Rich Results Test:** https://search.google.com/test/rich-results → 0 errors
