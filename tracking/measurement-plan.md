# Measurement Plan

You can't make marketing cost-effective without knowing which channel produced each **bound
policy**, not just each click. Set this up before spending on ads.

## 1. Tools (mostly free)

| Tool | Cost | Purpose |
|---|---|---|
| Google Analytics 4 | Free | Website traffic and conversions |
| Google Search Console | Free | SEO queries, rankings, indexing |
| Google Tag Manager | Free | Install tags without editing code |
| Google Ads conversion tracking | Free | Feeds Smart Bidding |
| Call tracking (CallRail, WhatConverts, or similar) | about $30–$50/mo | Which source made the phone ring; recordings for training |
| Your AMS/CRM (e.g. EZLynx, HawkSoft, AMS360, Applied Epic) | Existing | **Lead source field** on every prospect and policy |

## 2. Conversions to track

| Conversion | How | Counts as primary? |
|---|---|---|
| Quote form submit | Thank-you page view (`/thank-you/`) or GTM form event | Yes |
| Call from ads ≥60 seconds | Google forwarding number / call asset | Yes |
| Call from website ≥60 seconds | Call-tracking dynamic number insertion | Yes |
| GBP call / website click | GBP Performance (monthly, manual) | Report only |
| Click on `tel:` link | GTM click trigger | Secondary (observation) |
| Booking link scheduled | Calendly/booking confirmation | Yes |

## 3. Source naming (UTM conventions)

Use lowercase and the same values every time:

| Channel | utm_source | utm_medium | utm_campaign examples |
|---|---|---|---|
| Google Ads | google | cpc | brand, local-agency, commercial, home |
| Google Business Profile | google | organic | gbp, gbp-booking, gbp-post |
| Email newsletter | newsletter | email | 2026-12-newsletter, cross-sell-auto-only |
| Facebook page (organic) | facebook | social | post-{topic} |
| Partner referral links | partner | referral | {partner-name} |
| Print/QR codes | print | qr | business-card, office-sign |

Tip: build links with Google's Campaign URL Builder and log them in a shared sheet.

## 4. Lead source in your AMS (the most important step)

Create a required **Lead Source** dropdown with these values:

`Google Ads` · `Google LSA` · `Google Organic/GBP` · `Website (other)` · `Client referral` ·
`Partner referral` · `Cross-sell (existing client)` · `Walk-in` · `Social` · `Event` · `Other`

Ask every new caller: *"How did you hear about us?"* and check it against the call-tracking source.

## 5. Monthly reporting (30 minutes)

Fill one row per channel in [`monthly-kpi-tracker.csv`](monthly-kpi-tracker.csv):

**Spend → Leads → Quotes → Binds → Premium → Commission**

Then calculate cost per lead, cost per bind, and first-year commission ÷ spend (ROI). Reallocate
budget toward the channels with the lowest **cost per bind**.
