# Google Ads Plan (Cost-Effective Local Search)

**Philosophy:** small budget, tight targeting. Only bid where intent is high *and* a local agent has
an edge. Avoid broad national terms ("car insurance", "cheap car insurance") where clicks often cost
$30–$60+ and you compete with GEICO and Progressive budgets.

## 1. Paid search stack and budget split ($1,200/mo paid media)

| Program | Monthly | Notes |
|---|---|---|
| **Local Services Ads** | $500 | Pay per lead, top of page, "Google Screened" badge. See [`local-services-ads.md`](local-services-ads.md) |
| **Search: Brand** | $50 | Protect your name from competitors bidding on it; very cheap clicks |
| **Search: Local Agency / Bundle** | $300 | "insurance agent {city}", "home and auto insurance {city}" |
| **Search: Commercial Lines** | $250 | Business, contractor, and niche terms (higher premium, lower competition) |
| **Search: Home / Landlord** | $100 | Home insurance {city}, landlord insurance |
| **Total** | **$1,200** | about $40/day for Search; LSA billed per lead |

Auto-only keywords are intentionally limited to exact/phrase "{city}" modifiers, because auto CPCs are
the most expensive and lowest-margin. Let the bundle message capture auto shoppers instead.

## 2. Account settings (get these right; they prevent most wasted spend)

| Setting | Value | Why |
|---|---|---|
| Campaign type | Search only | Turn **off** Display Network and Search Partners at launch |
| Locations | Radius of 10–20 miles around office **or** list of ZIPs/cities you serve | Keep it tight |
| Location option | **"Presence: people in or regularly in your targeted locations"** | Default "presence or interest" wastes money on out-of-area clicks |
| Ad schedule | Business hours + 1 hr before/after; reduce bids or pause overnight | Leads that can't reach you go cold |
| Devices | All; watch mobile calls | Many insurance leads call from mobile |
| Bidding (launch) | **Maximize Clicks with a max CPC cap** (e.g. $12–$15) for weeks 1–4 | Gathers data without runaway CPCs |
| Bidding (after 15–30 conversions) | **Maximize Conversions**, then **Target CPA** at about 1.2× actual CPA | Let Google optimize once it has data |
| Match types | Phrase and exact; broad only later with Smart Bidding + strong negatives | Control |
| Auto-applied recommendations | **Turn off** | Prevents Google from adding broad keywords and raising budgets |
| Conversion goals | Calls ≥60s from ads, calls from website ≥60s, form submit (thank-you page), GBP calls | Count only real leads |
| Audiences (observation) | In-market: auto insurance, home insurance, business insurance; Life events: recently moved, purchased home | Observe first, then bid up winners |

## 3. Campaign and ad group structure

```
Campaign: Brand                         ($50/mo)
  └─ {agency name}, {agency name} insurance, {owner name} insurance

Campaign: Local Agency + Bundle         ($300/mo)
  ├─ Insurance Agent {City}             "insurance agent {city}", "insurance agency near me"
  ├─ Independent Agent                  "independent insurance agent {city}", "insurance broker {city}"
  └─ Home + Auto Bundle                 "home and auto insurance {city}", "bundle home and auto insurance"

Campaign: Commercial Lines              ($250/mo)
  ├─ Business Insurance {City}          "business insurance {city}", "small business insurance {city}"
  ├─ General Liability                  "general liability insurance {city}"
  ├─ Contractor (niche #1)              "contractor insurance {state}", "handyman insurance"
  └─ Workers Comp / Commercial Auto     "workers comp insurance {state}"

Campaign: Home / Landlord               ($100/mo)
  ├─ Home Insurance {City}              "home insurance {city}", "homeowners insurance {city}"
  └─ Landlord                           "landlord insurance {city}", "rental property insurance"
```

Ready-to-import keywords: [`google-ads-editor-import.csv`](google-ads-editor-import.csv).
Ad copy: [`ad-copy.md`](ad-copy.md). Negatives: [`negative-keywords.txt`](negative-keywords.txt).

**Landing pages:** send each ad group to its matching local page (built from
[`../seo/local-landing-page-template.html`](../seo/local-landing-page-template.html)), never to the homepage.

**Final URL tracking template** (account level):
```
{lpurl}?utm_source=google&utm_medium=cpc&utm_campaign={_campaign}&utm_term={keyword}&utm_content={creative}
```
Set custom parameter `{_campaign}` per campaign (e.g. `commercial`). Enable auto-tagging (gclid).

## 4. Assets (ad extensions), all free to add

- **Call asset:** Google forwarding number, call reporting on, scheduled to business hours
- **Location asset:** link GBP (shows address and distance)
- **Sitelinks (4+):** Get a Quote · Home Insurance · Business Insurance · Reviews · About Our Agents
- **Callouts:** Local {CITY} Agents · {N}+ Carriers Compared · Free Coverage Review · Claims Help · Bundle & Save
- **Structured snippets (Types):** Home, Auto, Business, Life, Umbrella, Landlord
- **Image assets:** office/team photos (not stock)
- **Lead form asset (optional test):** only if you can follow up within 5 minutes

## 5. Optimization routine

**Weekly (30 min)**
1. **Search terms report:** add irrelevant queries to the negative list (jobs, cheap/free, claims numbers, specific carriers you don't write, out-of-area towns)
2. Check that calls were real leads; mark junk
3. Pause keywords with spend > 2× target CPL and 0 conversions
4. Check impression share lost to budget on your best campaign; move money there from the weakest

**Monthly (1 hr)**
1. Compare cost per lead and **cost per bound policy** by campaign (requires lead source in your AMS/CRM)
2. Reallocate budget toward the lowest cost per *bound* policy, not just per lead
3. Test one new RSA headline set per ad group; remove assets rated "Low"
4. Review geographic report: exclude ZIPs with spend and no leads; raise bids in ZIPs that convert
5. Check the ad schedule report; lower bids in hours that never convert

**Quarterly**
- Once each campaign has 30+ conversions/month, test Target CPA
- Consider adding a small **remarketing** or **Performance Max** campaign only after Search is profitable

## 6. Benchmarks to judge results (local agency, 2026 rough ranges)

| Metric | Healthy range | Action if off |
|---|---|---|
| CTR | 6–12% | Below 4%: rewrite ads, tighten keywords |
| Avg CPC (local/commercial) | $6–$20 | Above $25: switch to exact match, add negatives, lower cap |
| Landing page conversion rate | 8–15% | Below 5%: shorten form, add phone and reviews above the fold |
| Cost per lead | $35–$75 | Above $100 for 30 days: pause that ad group |
| Lead-to-bind | 20–35% | Below 15%: fix speed-to-lead and follow-up cadence |

These vary heavily by state and line of business. Your own first 60 days of data replace them.

## 7. Policy and compliance notes

- Google treats insurance as a sensitive financial category in some regions. Verify any financial
  services verification requirement in your Ads account for your country/state.
- Don't make unsubstantiated claims ("lowest rates", "save 40%"). Use "compare", "shop", "could save".
- Include required state disclosures (some states require agency name and license number in ads).
- Don't use carrier trademarks in ad text unless your agency agreement allows it.
