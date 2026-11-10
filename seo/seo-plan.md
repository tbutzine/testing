# Local SEO Plan

**Objective:** rank in the map pack and the top 5 organic results for "[product] insurance {CITY}" and
"insurance agent/agency near me" within 6–9 months, then expand to neighbor towns and niches.

## 1. Site structure (target architecture)

```
/                              Home: "Independent Insurance Agency in {CITY}, {STATE}"
/auto-insurance-{city}/        Auto Insurance {CITY}
/home-insurance-{city}/        Home Insurance {CITY}
/business-insurance-{city}/    Business Insurance {CITY}
    /contractor-insurance/     Niche #1 (example)
    /restaurant-insurance/     Niche #2 (example)
/life-insurance-{city}/        Life Insurance {CITY}
/renters-insurance/  /condo-insurance/  /umbrella-insurance/  /landlord-insurance/
/areas-we-serve/
    /{neighbor-town-1}/        "Insurance Agency Serving {TOWN}" (unique content per town)
/about/                        Team bios, licenses, community involvement
/reviews/                      Embedded Google reviews + testimonials
/carriers/                     Companies we represent
/blog/                         Local guides and FAQs
/get-a-quote/                  Short form + phone + scheduler
```

**Build order:** Home → Auto → Home insurance → Business → Niche #1 → Life → Niche #2 → town pages.
The keyword-to-page mapping is in [`keyword-map.csv`](keyword-map.csv).

## 2. On-page rules (every page)

| Element | Rule | Example |
|---|---|---|
| Title tag (≤60 chars) | Primary keyword + city + brand | `Home Insurance in {CITY}, {STATE} \| {AGENCY}` |
| Meta description (≤155) | Benefit + proof + CTA | `Compare {N}+ carriers with a local {CITY} agent. 4.9★ from 120+ neighbors. Get a free quote today.` |
| H1 | One per page, matches intent | `Home Insurance in {CITY}` |
| URL | short, hyphenated | `/home-insurance-{city}/` |
| Content | 800–1,500 words, **genuinely local**: local risks (weather, flood zones, home age), neighborhoods, state minimums, FAQs | |
| Proof | 2–3 reviews, carrier logos (if permitted), agent photo | |
| CTA | Above the fold + after every major section; click-to-call on mobile | |
| Internal links | Link to 2–3 related product pages + quote page | |
| Schema | `InsuranceAgency` (site-wide) + `FAQPage` on product pages | See template |
| Images | Compressed WebP, descriptive alt text | `alt="{AGENCY} agent meeting with {CITY} homeowner"` |

**Avoid** duplicate "city swap" pages (identical text with only the town name changed). Google
treats them as thin content. Each town page needs unique details: local landmarks, the risks
specific to that town, a client story from that town, and driving directions.

## 3. Technical checklist

- [ ] Google Search Console verified; XML sitemap submitted
- [ ] HTTPS; mobile-friendly; Core Web Vitals passing (test at pagespeed.web.dev)
- [ ] Page load under 2.5s on mobile (compress images, avoid heavy page builders/sliders)
- [ ] One canonical version of the domain (www or not) with redirects
- [ ] NAP in the footer exactly matching GBP
- [ ] Embed a Google Map on the contact page
- [ ] No "noindex" on important pages; fix 404s monthly

## 4. Content calendar (2 pieces per month)

Content should answer questions local buyers actually ask. Each piece targets one question and links
to a product page.

| Month | Piece 1 (product/niche page) | Piece 2 (helpful local article) |
|---|---|---|
| 1 | Home Insurance {CITY} | "How much is home insurance in {CITY}? (2026 guide)" |
| 2 | Auto Insurance {CITY} | "{STATE} minimum car insurance requirements explained" |
| 3 | Business Insurance {CITY} | "What insurance does a contractor need in {STATE}?" |
| 4 | Niche #1 page | "Does homeowners insurance cover {local peril: hail/flood/wildfire}?" |
| 5 | Life Insurance {CITY} | "Bundling home and auto: when it saves money and when it doesn't" |
| 6 | {Neighbor town 1} page | "New to {CITY}? Insurance checklist for new homeowners" |
| 7 | Niche #2 page | "Why did my insurance go up? (and what to do about it)" |
| 8 | {Neighbor town 2} page | "Independent agent vs. captive agent vs. buying online" |
| 9 | Umbrella / landlord page | "Insurance for {CITY} landlords and short-term rentals" |

"How much does X cost in {CITY}" posts attract high-intent traffic. Use real ranges from your own
quoting data (anonymized). That's content national sites can't copy.

## 5. Local link building (cost-effective)

Quality over quantity. Aim for 2–4 local links per month.

1. **Carrier "find an agent" pages:** ask every carrier rep to list you with a link
2. **Chamber of commerce and business associations:** member directory links
3. **Sponsorships:** youth sports, school fundraisers, 5Ks, charity events ($100–$500, and they usually link to sponsors)
4. **Partner pages:** realtors, mortgage lenders, auto dealers, body shops, contractors, and property managers you refer to and from ("trusted partners" pages)
5. **Local press:** offer yourself as a source for local stories (storm prep, rate increases)
6. **Scholarship:** a small annual "{AGENCY} Community Scholarship" earns links from school sites
7. **Guest content:** write a "home insurance checklist" for a realtor's or HOA's newsletter or site

## 6. Measuring SEO

Monthly, from Search Console and GA4:

- Impressions/clicks for "{CITY}" queries
- Rankings for the 15 priority keywords (spot check in an incognito window, or a local rank tracker
  such as BrightLocal or Local Falcon, about $30–$50/mo, optional)
- Organic leads (form fills + calls from organic)
