# GTM Live Audit Kit
## Raleigh Comprehensive & Cosmetic Dentistry

**IMPORTANT:** Use Preview mode ONLY. Do NOT publish any changes.

---

## PRE-AUDIT CHECKLIST

- [ ] Open https://tagmanager.google.com/
- [ ] Select raleighdentistry.com container
- [ ] Note your Container ID (GTM-XXXXXX)
- [ ] Click Preview button (top right)
- [ ] Enter https://www.raleighdentistry.com
- [ ] Wait for Debug pane to load

---

## SECTION 1: Tags

Go to: Tags (left sidebar)

For each tag, note: Name, Type, Trigger(s), Status (Enabled/Disabled)

### Must-Have Tags (check each)
- [ ] GA4 Configuration tag → Tag ID: _______
- [ ] GA4 Event tag for page_view → Name: _______
- [ ] Phone number click tracking → Name: _______ / Not found
- [ ] Contact form submission → Name: _______ / Not found
- [ ] Appointment/consultation button click → Name: _______ / Not found
- [ ] Scroll depth tracking → Name: _______ / Not found
- [ ] Outbound link tracking → Name: _______ / Not found

### Custom Tags
List any custom HTML, custom image, or custom event tags:
1. _______
2. _______

---

## SECTION 2: Triggers

Go to: Triggers (left sidebar)

List each trigger: Name, Type, Configuration

Common triggers to look for:
- [ ] All Pages
- [ ] DOM Ready / Window Loaded
- [ ] Click — All Elements
- [ ] Click — Just Links
- [ ] Click — Specific Elements (phone, buttons)
- [ ] Form Submission
- [ ] Scroll Depth
- [ ] Custom Event
- [ ] Timer

---

## SECTION 3: Variables

Go to: Variables → Configure (top right)

Check each variable as Enabled or Disabled:

### Built-in Variables
- [ ] Page URL
- [ ] Page Path
- [ ] Page Hostname
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

### Custom Variables
List any custom variables you see:
1. _______
2. _______

---

## SECTION 4: Preview Mode — Live Test

With Debug pane open on https://www.raleighdentistry.com:

### Homepage Load
Tags that fired on initial page load:
1. _______
2. _______

### Phone Number Click
- Click the phone number on the page
- Did a tag fire? [Yes/No]
- Tag name: _______
- Event sent to GA4: _______

### Contact Form
- Fill out and submit the contact form
- Did a tag fire? [Yes/No]
- Tag name: _______
- Event sent to GA4: _______

### Scroll
- Scroll down the page
- Did a scroll tag fire? [Yes/No]
- Tag name: _______
- Scroll depth triggered: _______ (25%, 50%, 75%, 100%)

### Outbound Link
- Click any link that goes to another domain
- Did a tag fire? [Yes/No]
- Tag name: _______

---

## SECTION 5: GA4 Integration

### GA4 Configuration
- GA4 Config tag present: [Yes/No]
- Measurement ID: _______
- Connected to GA4 property: _______

### GA4 Events
List all GA4 Event tags:
1. _______
2. _______

### Conversions
Does GTM pass any conversion events to GA4? [Yes/No]
List: _______

---

## SECTION 6: Issues Found

| # | Issue | Severity | Recommendation |
|---|-------|----------|----------------|
| 1 | | | |
| 2 | | | |
| 3 | | | |

---

## SECTION 7: Screenshots to Capture

- [ ] Container overview (all tags listed)
- [ ] Tags page
- [ ] Triggers page
- [ ] Variables → Configure page
- [ ] Preview mode — Debug pane on homepage
- [ ] Preview mode — after clicking phone number
- [ ] Preview mode — after submitting form
- [ ] Preview mode — after scrolling
- [ ] Versions page
