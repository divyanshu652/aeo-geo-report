# Current Schema Audit — Avi Sanghavi Dental

**Website:** raleighdentistry.com  
**Audit Date:** October 2, 2026  
**Auditor:** Manual inspection via Chrome DevTools Console

---

## How Schema Was Inspected

1. Opened raleighdentistry.com in Chrome
2. F12 → Console tab
3. Ran JavaScript to extract all JSON-LD blocks
4. Found 2 `<script type="application/ld+json">` blocks

---

## BLOCK 1: @graph Schema (Homepage)

**Page:** Homepage (raleighdentistry.com/)  
**Structure:** Single JSON-LD block using `@graph` to contain 4 entities

### Entities within @graph:

**Entity 1: WebSite**
- @type: WebSite
- @id: https://www.raleighdentistry.com/#website
- url: https://www.raleighdentistry.com/
- name: Raleigh Comprehensive & Cosmetic Dentistry
- Status: ✅ Valid

**Entity 2: MedicalClinic** ← NEEDS REPLACEMENT
- @type: MedicalClinic
- @id: https://www.raleighdentistry.com/#practice
- name: Raleigh Comprehensive & Cosmetic Dentistry
- description: "Raleigh Comprehensive & Cosmetic Dentistry is a medical practice with an office in Raleigh, NC."
- url: https://www.raleighdentistry.com/
- telephone: (919) 828-3775
- image: https://einstein-clients.imgix.net/8112/494844/original.svg?1767899842
- logo: https://einstein-clients.imgix.net/8112/494844/original.svg?1767899842
- priceRange: $$$
- address: 119 North Boylan Avenue, Raleigh, NC 27603, US
- geo: latitude 35.782684, longitude -78.6494414
- openingHoursSpecification: Mon-Thu 08:00-17:00, Fri 08:00-17:00
- sameAs: [https://www.google.com/maps?cid=15003956664647858033]
- Status: ⚠️ Well-structured but WRONG TYPE — MedicalClinic should be Dentist

**Entity 3: WebPage**
- @type: WebPage
- @id: https://www.raleighdentistry.com/#webpage
- url: https://www.raleighdentistry.com/
- name: Dentist in Raleigh, NC | Raleigh Comprehensive & Cosmetic Dentistry
- description: [full description text]
- isPartOf: https://www.raleighdentistry.com/#website
- about: https://www.raleighdentistry.com/#practice
- Status: ✅ Valid

**Entity 4: BreadcrumbList**
- @type: BreadcrumbList
- @id: https://www.raleighdentistry.com/#breadcrumbs
- Status: ✅ Valid

### Block 1 Issues:
1. **MedicalClinic type** — Should be `Dentist` (or `["Dentist", "LocalBusiness"]`)
2. **Friday hours** — Listed as 08:00-17:00 but site also says "Open Every Other Friday" — needs confirmation
3. **No Saturday/Sunday hours** — May need to be added if closed (specify as `"closed": true` or omit)
4. **sameAs** — Only has Google Maps link. No social profiles detected.
5. **priceRange** — Currently "$$$" — confirm if accurate
6. **No aggregateRating** — Could add from GBP data

---

## BLOCK 2: Organization + WebSite + WebPage (BROKEN)

**Page:** Homepage (raleighdentistry.com/)  
**Status:** ❌ BROKEN — Multiple critical errors

### Entity 1: Organization (BROKEN)
- @type: Organization
- @id: `https://#org` ← ❌ BROKEN URL — missing domain name
- name: Raleigh Comprehensive & Cosmetic Dentistry
- url: `https://` ← ❌ BROKEN — empty URL
- logo: [image object with valid imgix URL]
- location: [array containing LocalBusiness]
  - @type: LocalBusiness
  - @id: `https:///locations#loc-0` ← ❌ BROKEN — malformed URL (triple slash, no domain)
  - name: Raleigh Office
  - image: https:///_cache/static_map_... ← ❌ BROKEN — missing domain
  - priceRange: $$$
  - address: [same as Block 1]
  - openingHours: mo-fr 08:00-17:00
  - telephone: (919) 828-3775
- sameAs: [Google Maps link — same as Block 1]

### Entity 2: WebSite (BROKEN)
- @type: WebSite
- @id: `https://#site` ← ❌ BROKEN URL
- name: Raleigh Comprehensive & Cosmetic Dentistry

### Entity 3: WebPage (BROKEN)
- @type: WebPage
- url: `https:///` ← ❌ BROKEN
- isPartOf: { @id: `https://#site` } ← ❌ BROKEN reference

### Block 2 Issues (CRITICAL):
1. **@id URLs are malformed** — `https://#org`, `https:///locations#loc-0`, `https://#site` — all missing proper domain
2. **url field is broken** — `https://` with no domain/path
3. **image URL broken** — `https:///_cache/...` missing domain
4. **Entity references broken** — WebPage references `https://#site` which doesn't resolve
5. **Conflicts with Block 1** — Duplicate practice entity with different @id
6. **Should be removed entirely** — Block 1 already covers all needed entities properly

---

## SUMMARY TABLE

| Block | Page | Types | Valid? | Recommendation |
|-------|------|-------|--------|----------------|
| Block 1 (@graph) | Homepage | WebSite, MedicalClinic, WebPage, BreadcrumbList | ⚠️ Partial | REPLACE MedicalClinic type with Dentist |
| Block 2 (array) | Homepage | Organization, LocalBusiness, WebSite, WebPage | ❌ Broken | DELETE entirely |

---

## ISSUES BY SEVERITY

### Critical (must fix)
1. Block 2 has broken @id URLs (`https://#org`, `https://#site`, `https:///locations#loc-0`)
2. Block 2 has broken url fields (`https://` with no domain)
3. Block 2 entity references don't resolve (WebPage → https://#site)
4. Duplicate practice entity across Block 1 and Block 2

### Warning (should fix)
1. Block 1 uses `MedicalClinic` type — should be `Dentist` for dental practices
2. Friday hours may be inaccurate ("every other Friday" mentioned on site)
3. No Saturday/Sunday hours specified (closed days not explicitly marked)
4. Only one sameAs profile (Google Maps) — no social profiles

### Info (nice to have)
1. No aggregateRating in schema (could pull from GBP)
2. priceRange is "$$$" — confirm accuracy
3. No hasOfferCatalog for services
4. Image/logo uses imgix CDN with cache-busting query param

---

## RECOMMENDATION

**Simplest fix:** Change Block 1's `MedicalClinic` to `Dentist` (keeping everything else), and DELETE Block 2 entirely.

This is a minimal change that fixes the core issue without restructuring the entire schema.

**Alternative (more thorough):** Consolidate everything into a single clean LocalBusiness/Dentist @graph block, removing the broken Block 2 and updating Block 1's type.
