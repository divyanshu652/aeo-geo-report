# GA4 + GTM Live Audit Kit
## Raleigh Comprehensive & Cosmetic Dentistry

**IMPORTANT:** You already have GA4 and GTM access. This kit gets you through both audits in one focused session (~30-40 min total).

---

# PART 1: GA4 AUDIT (15-20 min)

## Step 1: Open GA4
**URL:** https://analytics.google.com/analytics/web/
- Select the property for raleighdentistry.com
- Property ID should be in the format: 3XXXXXXXXX

## Step 2: Copy This Info

### Property Info
| Field | Where to Find | Your Value |
|------|--------------|-----------|
| Property Name | Admin (bottom left gear) → Property Settings | [fill] |
| Property ID | Admin → Property Settings | [fill — 3XXXXXXXXX] |
| Measurement ID | Admin → Data Streams → Web → select your stream → Measurement ID | [fill — G-XXXXXXXXXX] |
| Data Stream URL | Same page | https://www.raleighdentistry.com |
| Enhanced Measurement | Same page → Enhanced Measurement section | Enabled / Disabled |
| Data Retention | Admin → Data Settings → Data Retention | [fill] |
| Google Signals | Admin → Data Settings → Data Collection → Google Signals | On / Off |

### Reports → Overview (Home)
Copy these numbers from the date range selector (set to Last 30 Days):
| Metric | Value |
|--------|-------|
| Users | [fill] |
| New Users | [fill] |
| Sessions | [fill] |
| Average Session Duration | [fill] (e.g., 1m 23s) |
| Pages per Session | [fill] (e.g., 2.4) |
| Bounce Rate | [fill]% |

### Reports → Acquisition → Traffic Acquisition
Set date range: Last 30 Days. Then:
| Source/Medium | Users | Sessions | % of Total |
|--------------|-------|----------|-----------|
| Organic Search | [fill] | [fill] | [fill]% |
| Direct | [fill] | [fill] | [fill]% |
| Referral | [fill] | [fill] | [fill]% |
| Social | [fill] | [fill] | [fill]% |
| Paid Search | [fill] | [fill] | [fill]% |
| Email | [fill] | [fill] | [fill]% |
| Other | [fill] | [fill] | [fill]% |

### Reports → Engagement → Pages and Screens
| Page Path | Page Title | Views | Average Engagement Time | Bounce Rate |
|-----------|-----------|-------|------------------------|-------------|
| / | [fill] | [fill] | [fill] | [fill] |
| /about | [fill] | [fill] | [fill] | [fill] |
| /services | [fill] | [fill] | [fill] | [fill] |
| /contact | [fill] | [fill] | [fill] | [fill] |
| [other pages] | [fill] | [fill] | [fill] | [fill] |

### Reports → Engagement → Events
List ALL events shown (copy the table):
| Event Name | Count (30d) |
|-----------|-------------|
| [fill] | [fill] |
| [fill] | [fill] |

Standard events to check for: page_view, scroll, user_engagement, session_start, first_visit, file_download, outbound_click, view_search_results, video_start, video_progress, video_complete

### Reports → Engagement → Conversions
| Conversion Event | Count (30d) | Count (Previous 30d) |
|-----------------|-------------|---------------------|
| [fill] | [fill] | [fill] |
| [fill] | [fill] | [fill] |

### Configure → Events (left sidebar)
Screenshot this page. It shows ALL configured events including custom ones.
List any custom events you see:
1. [fill]
2. [fill]

### Configure → Conversions (left sidebar)
Screenshot this page. List all conversion events:
1. [fill]
2. [fill]

### Configure → Custom Definitions
Screenshot if anything is here. List custom dimensions/metrics:
| Name | Type | Scope |
|------|------|-------|
| [fill] | [fill] | [fill] |

### Admin → Data Streams → Web Stream → Enhanced Measurement
Check what's enabled:
- Page views: [On/Off]
- Scrolls: [On/Off]
- Outbound clicks: [On/Off]
- Site search: [On/Off]
- Video engagement: [On/Off]
- File downloads: [On/Off]

### Admin → Data Streams → Web Stream → More tagging settings
- Google Signals: [On/Off]
- Advertising features: [On/Off]
- List of defined events: [screenshot/list]

### Admin → Data Settings → Data Retention
- [fill] months

### Admin → Data Settings → Data Collection
- Google Signals: [On/Off]
- Ads Personalization: [On/Off]

### Admin → Data Collection and Modification → Data Filters
Any filters configured? [Yes/No] — list if yes:
| Filter Name | Type | Status |
|------------|------|--------|
| [fill] | [fill] | [fill] |

### Demographics (if available)
Reports → Demographics → Overview
- Country distribution: [fill top 3]
- City distribution: [fill top 3]
- Gender: [fill]
- Age: [fill]

---

# PART 2: GTM AUDIT (15-20 min)

## Step 1: Open GTM
**URL:** https://tagmanager.google.com/
- Select the container for raleighdentistry.com
- Container ID format: GTM-XXXXXX

## Step 2: IMPORTANT — Use Preview Mode Only
DO NOT publish any changes. Use Preview mode to see what's firing.

### Container Info
| Field | Value |
|-------|-------|
| Container ID | [fill] |
| Container Name | [fill] |
| Workspace | [fill] |
| Last Published | [fill] |
| Pending Changes | Yes / No |

### Tags (left sidebar → Tags)
List EVERY tag:
| # | Tag Name | Type | Trigger(s) | Status |
|---|----------|------|-----------|--------|
| 1 | [fill] | [fill] | [fill] | Enabled/Disabled |
| 2 | [fill] | [fill] | [fill] | Enabled/Disabled |

Critical checks:
- [ ] GA4 Configuration tag present? → Tag ID: [fill]
- [ ] Phone click tracking? → Tag name: [fill]
- [ ] Form submission tracking? → Tag name: [fill]
- [ ] Appointment/CTA click tracking? → Tag name: [fill]
- [ ] Scroll depth tracking? → Tag name: [fill]
- [ ] Outbound link tracking? → Tag name: [fill]
- [ ] Custom HTML tags? → List: [fill]

### Triggers (left sidebar → Triggers)
List EVERY trigger:
| # | Trigger Name | Type | Fires On |
|---|-------------|------|---------|
| 1 | [fill] | [fill] | [fill] |
| 2 | [fill] | [fill] | [fill] |

### Variables (left sidebar → Variables)
Check Variables → Configure (top right). Mark each:

Built-in Variables:
- [ ] Page URL
- [ ] Page Hostname
- [ ] Page Path
- [ ] Page Referrer
- [ ] Click Text
- [ ] Click URL
- [ ] Click Classes
- [ ] Click ID
- [ ] Click Target
- [ ] Form ID
- [ ] Form Classes
- [ ] Form Element
- [ ] Error Message
- [ ] Error URL
- [ ] Error Line

Other variable types:
- [ ] 1st Party Cookie
- [ ] 1st Party JS Variable
- [ ] Google Analytics Settings
- [ ] Constant
- [ ] Custom JavaScript
- [ ] Data Layer Variable
- [ ] DOM Element

### Preview Mode Test
1. Click "Preview" button (top right)
2. Enter https://www.raleighdentistry.com
3. On the homepage, check Debug pane:
   - Which tags fire on page load?
   - List them: [fill]
4. Click the phone number on the page — does a phone-click tag fire?
   - [ ] Yes — Tag: [fill]
   - [ ] No
5. Submit the contact form — does a form-submit tag fire?
   - [ ] Yes — Tag: [fill]
   - [ ] No
6. Scroll down the page — does a scroll tag fire?
   - [ ] Yes — Tag: [fill]
   - [ ] No

### GA4 Integration
| Check | Status | Details |
|-------|--------|---------|
| GA4 Config tag connected | Yes/No | Measurement ID: [fill] |
| GA4 Event tags | Count: [fill] | [list] |
| Custom Events | Count: [fill] | [list] |
| Conversions mapped from GA4 | Yes/No | [list] |

### Custom Code / Custom HTML
Any custom HTML or JS tags? [Yes/No]
List if yes:
| # | Name | Description |
|---|------|-------------|
| 1 | [fill] | [fill] |

### Folders
Any folders organizing tags? [Yes/No]
List: [fill]

---

# PART 3: GA4 DATA WE ALREADY HAVE

From your existing GSC + CSV data, here's what we can already tell:

## Traffic by Device (GSC data)
| Device | Clicks | Impressions | CTR | Avg Position |
|--------|--------|-------------|-----|-------------|
| Desktop | 254 | 94,281 | 0.27% | 22.2 |
| Mobile | 216 | 34,871 | 0.62% | 18.8 |
| Tablet | 1 | 720 | 0.14% | 15.5 |

**Key insight:** Mobile has higher CTR (0.62%) despite lower impressions. Desktop drives most impressions but lowest CTR.

## Traffic by Country (GSC data)
| Country | Clicks | Impressions | CTR | Avg Position |
|---------|--------|-------------|-----|-------------|
| United States | 453 | 126,294 | 0.36% | 21.2 |
| India | 4 | 418 | 0.96% | 31.6 |
| Pakistan | 3 | 79 | 3.80% | 15.2 |
| Philippines | 2 | 90 | 2.22% | 22.3 |

**Key insight:** US dominates (96.9% of clicks). International traffic is minimal but has higher CTR — likely from dental researchers or industry.

## Daily Trend (GSC data — last available)
| Date Range | Trend |
|-----------|-------|
| July 2026 | Clicks range 0-10/day, averaging ~4.5/day |
| CTR range | 0% to 1.19% |
| Position range | 11.4 to 18.2 |

## What We'll Cross-Check with GA4
| Metric | GSC Value | GA4 Value (fill) | Match? |
|--------|-----------|-----------------|--------|
| Users (30d) | N/A | [fill] | — |
| Sessions (30d) | N/A | [fill] | — |
| Organic traffic % | N/A | [fill]% | — |
| Top landing pages | From GSC | [fill] | — |
| Mobile vs Desktop | 46%/54% | [fill]/[fill] | — |
| Conversion events | None tracked | [fill] | — |
| Phone click events | None tracked | [fill] | — |
| Form submit events | None tracked | [fill] | — |

---

# PART 4: WHAT TO DO WITH THE DATA

After you fill in the GA4 + GTM audit:

1. Save both filled documents
2. Send to me — I'll integrate into the master report
3. Any issues found (missing tags, wrong configs, untracked conversions) get added to the action items list

**Expected findings for a typical dental practice:**
- GA4 probably has page_view + default events but may be missing phone-click and form-submit custom events
- GTM probably has GA4 config tag + maybe a few others
- Most likely gap: no call tracking, no form tracking, no appointment click tracking

These are exactly the events that matter for a dental practice — every missed phone click is a lost patient.
