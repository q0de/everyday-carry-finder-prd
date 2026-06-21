# Hermes Review and PRD v5 Additions

Reviewed: June 20, 2026

## Executive Verdict

The repo is useful and directionally strong, but it currently contains a strategic conflict that should be resolved before build:

- `PRD.md` says the product should be broad practical EDC, with 10 launch pages and the quiz later.
- `README.md` says the MVP wedge is a smaller beginner/budget/keychain cluster plus the Carry Builder quiz.
- `docs/keyword-serp-validation-no-knife-tsa-edc.md` validates an 8-page no-knife/TSA cluster that no longer matches the broader v4 positioning.

The right next move is not to build the full site yet. The right next move is a **validation-first v5 PRD** that chooses one launch wedge, defines the build gates, and prevents the project from becoming a generic affiliate gear site.

## Recommended Reconciled MVP

Use this as the v5 default unless new keyword/SERP validation disproves it.

### Phase A: Static SEO MVP

Launch 6 pages first, not 10:

1. `/edc-checklist/` — **Everyday Carry Checklist**
2. `/best-edc-gear-for-beginners/` — **Best EDC Gear for Beginners**
3. `/best-edc-kit-under-100/` — **Best EDC Kit Under $100**
4. `/tsa-friendly-edc-kit/` — **TSA-Friendly EDC Kit**
5. `/best-keychain-edc/` — **Best Keychain EDC**
6. `/best-edc-without-a-knife/` — **Best EDC Without a Knife**

Why these six:

- They preserve the broader beginner/budget positioning.
- They keep the validated no-knife/TSA insight without making it the whole brand.
- They create a hub/spoke structure quickly.
- They are enough to test indexing, impressions, and affiliate click behavior without overproducing pages.

### Phase B: Add Only If Phase A Shows Signal

Add these after GSC impressions or outbound clicks identify the winning lane:

- `/best-office-edc/`
- `/best-travel-edc/`
- `/best-minimalist-edc/`
- `/best-edc-kit-under-50/`
- `/pocket-edc-vs-pouch-edc/`

### Phase C: Carry Builder Quiz

The Carry Builder quiz should not be a launch blocker.

Build it only after at least one of these is true:

- 3+ pages are indexed and getting repeated impressions.
- At least 50 tracked affiliate/product outbound clicks have occurred.
- A clear winning cluster emerges from Search Console.
- The quiz can be built as a lightweight deterministic mapper to existing product sets, not a full recommendation engine.

## Highest-Risk Assumptions

1. **Broad EDC pages may be too competitive.** The repo validates the no-knife/TSA wedge better than the broader beginner/budget pages.
2. **Amazon-only economics may be weak.** Low AOV plus low commission can make the project uninteresting unless traffic is large or direct programs improve rates.
3. **The quiz may become product theater.** It is only valuable if it routes users to better product clicks or captures clear intent data.
4. **Trust is expensive.** A gear affiliate site without original photos, handling notes, and honest tradeoffs will look like AI commodity content.
5. **Freshness ops can overbuild the MVP.** Daily/weekly monitoring is useful, but first launch only needs link tracking, last-checked fields, and a manual review queue.

## Build Gates

### Gate 1: Before Writing Pages

Required:

- Final 6-page launch list chosen.
- Keyword/SERP validation table completed for all 6 pages.
- Product seed sheet contains at least 35 candidate products across launch categories.
- Amazon/direct affiliate eligibility checked.
- Page template approved.
- Disclosure blocks approved.

Do not write full articles before this gate passes.

### Gate 2: Before Publishing

Each published page must have:

- Named author/editor.
- Affiliate disclosure near top and before product links where appropriate.
- Last updated date.
- Last product verification date.
- At least 5 product/category recommendations.
- Clear tested/handled/researched labels.
- At least 3 internal links.
- Tracked outbound links.
- Schema plan applied where appropriate.
- No absolute TSA/legal/workplace claims.

### Gate 3: Before Quiz Build

Required:

- Existing pages have enough products to power deterministic results.
- Product data has stable IDs/tags.
- Analytics can attribute quiz result clicks to product/page.
- Quiz scope is capped to 6-8 steps and maps to existing pages/product sets.

## Launch Sitemap v5 Draft

| Priority | URL | Page | Role | Status |
|---:|---|---|---|---|
| 1 | `/edc-checklist/` | Everyday Carry Checklist | Hub/trust/internal links | Build after SERP validation |
| 2 | `/best-edc-gear-for-beginners/` | Best EDC Gear for Beginners | Buyer/trust | Validate competition first |
| 3 | `/best-edc-kit-under-100/` | Best EDC Kit Under $100 | Buyer/commercial | Validate; likely better than under-$50 |
| 4 | `/tsa-friendly-edc-kit/` | TSA-Friendly EDC Kit | Constraint buyer | Build; already directionally validated |
| 5 | `/best-keychain-edc/` | Best Keychain EDC | Buyer/category | Validate SERP shape |
| 6 | `/best-edc-without-a-knife/` | Best EDC Without a Knife | Constraint buyer | Build; already directionally validated |
| 7 | `/best-office-edc/` | Best Office EDC | Lifestyle buyer | Defer unless validation strong |
| 8 | `/best-travel-edc/` | Best Travel EDC | Travel buyer | Defer or merge with TSA first |
| 9 | `/best-minimalist-edc/` | Best Minimalist EDC | Competitive lifestyle | Defer |
| 10 | `/best-edc-kit-under-50/` | Best EDC Kit Under $50 | Budget buyer | Defer unless product quality credible |

## Product Seed Requirements

Minimum before publishing Phase A:

- 6-8 wallets/card holders
- 6-8 compact flashlights
- 6-8 pens
- 5-7 key organizers/keychain tools
- 5-7 pouches/organizers
- 4-6 chargers/cables/power accessories
- 4-6 TSA-friendly/no-knife tools
- 4-6 optional knives for non-TSA pages if the broader pages need them

Each product row must include:

```text
product_id
product_name
brand
category
price_band
merchant
affiliate_program
affiliate_url
canonical_url
launch_page_fit
tags
tested_status: tested | handled | researched
best_for
avoid_if
pros
cons
last_price_checked_at
last_availability_checked_at
recommendation_status
```

## Analytics Event Spec

Use these names consistently from day one:

- `affiliate_click`
- `product_card_click`
- `comparison_table_click`
- `internal_related_page_click`
- `page_cta_click`
- `quiz_start`
- `quiz_complete`
- `quiz_product_click`

Required properties:

```text
page_slug
page_type
product_id
product_category
merchant
affiliate_program
price_band
position_on_page
cta_label
recommendation_context
is_affiliate
```

## Compliance Blocks To Add To v5

### Standard Affiliate Disclosure

> Some links on this page may be affiliate links. If you buy through them, we may earn a commission at no extra cost to you. We only recommend items that fit the use case described on this page, and we label recommendations based on whether they were tested, handled, or researched.

### Amazon Disclosure

> As an Amazon Associate, Everyday Carry Finder earns from qualifying purchases.

### TSA Disclaimer

> TSA rules can change, and final decisions at the checkpoint rest with TSA officers. This page is a conservative guide, not a guarantee that an item will be allowed through security. Always check the latest TSA guidance before you travel.

### Knife / Local Law Disclaimer

> Knife and tool laws vary by location, workplace, school, venue, and travel context. Check your local rules and policies before carrying a knife or tool.

## 30-Day Execution Plan

### Week 1: Validation and Data

- Finalize 6-page Phase A list.
- Complete keyword/SERP table for each page.
- Build product seed sheet with 35+ candidates.
- Choose affiliate/tracking approach.
- Approve page template and disclosure blocks.

### Week 2: First Hub + Buyer Page

- Draft `/edc-checklist/`.
- Draft `/best-edc-gear-for-beginners/` or `/tsa-friendly-edc-kit/` depending on validation.
- Add internal links and product cards.
- Add analytics/tracked outbound links.

### Week 3: Remaining Phase A Pages

- Draft the next 3-4 pages.
- Apply consistent product-card format.
- Add schema, related links, and disclosures.
- QA all affiliate URLs and non-affiliate fallbacks.

### Week 4: Publish and Indexing

- Publish Phase A pages.
- Submit sitemap in Google Search Console.
- Verify analytics events.
- Record baseline GSC/indexing state.
- Start manual weekly review log.

## 120-180 Day Decision Criteria

### Continue

Continue if at least two are true:

- 3+ pages get repeated Search Console impressions.
- 1+ pages get organic clicks.
- Outbound product clicks occur from multiple pages.
- One cluster clearly outperforms the rest.
- Direct affiliate opportunities become realistic.

### Pivot

Pivot if:

- Broad EDC pages fail but TSA/no-knife pages show impressions.
- Informational pages get impressions but buyer pages do not.
- Keychain/budget pages get clicks but low monetization.
- The quiz gets usage but product clicks remain weak.

### Kill / Park

Park the project if:

- Pages do not index after technical fixes.
- SERPs are unwinnable across all launch topics.
- There are no outbound clicks after meaningful impressions.
- Content freshness and product testing burden exceeds expected upside.

## What I Would Add To `PRD.md`

Add a short v5 reconciliation section:

> The MVP should be validation-first. The repo previously considered a 10-page broad EDC launch and an 8-page no-knife/TSA launch. v5 reconciles these into a smaller 6-page Phase A that combines broad beginner/budget positioning with the validated TSA/no-knife wedge. The Carry Builder quiz is a Phase C conversion layer, not a launch dependency. No page should be written until its keyword/SERP table, product seed list, affiliate fit, and compliance notes are complete.

## Blunt Final Note

This is worth testing only if it stays cheap and evidence-driven. The fastest way to waste time is to build the quiz and freshness automation before the site proves that Google will send any qualified traffic. The fastest useful path is: validate 6 pages, publish clean static pages, track outbound clicks, then let the data choose the next cluster.
