# Product Requirements Document: Everyday Carry Finder v4

Updated: June 20, 2026

## 1. Executive Summary

Everyday Carry Finder is a practical recommendation site for people who want to build an everyday carry setup that fits their real life: budget, pocket space, work rules, travel needs, style, and comfort level.

The product should not be positioned as a "no-knife EDC" brand. That is too narrow and would make the site feel timid, repetitive, and less useful to the broader EDC audience.

The better product thesis is:

> Find the right everyday carry setup for your life, budget, and constraints.

No-knife and TSA-friendly carry remain important, but they are lanes inside the broader product. The TSA-friendly lane should be explicitly knife-free because that is the core constraint. Other pages should treat knives as optional depending on the use case.

## 2. Product Thesis

Generic EDC content is crowded, but most of it is organized around gear categories instead of user situations.

Everyday Carry Finder wins by organizing recommendations around practical constraints:

- Budget
- Travel
- Office/workplace rules
- Pocket space
- Beginner friendliness
- Minimalism
- Style preference
- Knife optionality
- TSA restrictions
- Bag vs pocket carry

This creates a more useful experience than another generic "best EDC gear" list because users can find a setup that matches their actual use case.

The site should feel practical, edited, and trustworthy, not tactical, survivalist, or overbuilt.

## 3. Positioning

Working name: Everyday Carry Finder

Positioning statement:

> Everyday Carry Finder helps people build practical carry setups by budget, lifestyle, pocket space, and travel/work constraints.

Avoid positioning the whole brand around:

- No-knife carry
- TSA-only carry
- Tactical gear
- Survival gear
- Knife-first enthusiast culture
- Generic gear dumping

The site can include knife content where it makes sense, but it should not become a knife review site. Knives are one possible EDC category, not the center of the product.

## 4. Target Users

### Primary Launch Users

1. EDC beginners
   - Want a useful setup without learning the entire category
   - Need clear explanations and starter kits
   - Care about price, usefulness, and avoiding dumb purchases

2. Budget-conscious buyers
   - Search for kits under $50 or $100
   - Want practical recommendations from familiar retailers
   - Need tradeoffs explained clearly

3. Office and urban carriers
   - Want compact, non-tactical gear
   - May or may not want a knife
   - Care about looking normal in work and public settings

4. Travelers
   - Need different guidance for air travel vs road/hotel travel
   - TSA-friendly air travel pages should exclude knives
   - General travel EDC can include a knife when appropriate

### Secondary Users

- Minimalists
- Students
- Gift buyers
- Parents
- Commuters
- Bag/pouch carriers
- Keychain EDC users

### Deferred Users

- Knife collectors
- Premium flashlight enthusiasts
- Tactical/survival-prepper audiences
- Trade-specific users like electricians or EMTs

These can become future content clusters only after the broad beginner/budget/travel/office foundation proves traction.

## 5. User Problem

Most EDC content assumes the reader already understands the category. It also often defaults to tactical-looking gear, knives, premium flashlights, and large lists of products without explaining what a normal person should actually carry.

Users need answers like:

- What should I carry every day as a beginner?
- What EDC gear is actually worth buying under $50 or $100?
- What belongs in a minimalist pocket setup?
- What can I bring through TSA?
- Do I need a knife, or are there better alternatives?
- What is useful for office carry without looking tactical?
- Should I carry items in my pockets, on my keys, or in a pouch?

The site should reduce the research burden from "learn the whole EDC world" to "pick the right setup for your situation."

## 6. MVP Scope

### Included In MVP

- 10-page static SEO/content launch
- Curated recommendation pages
- Beginner-first editorial framework
- Product spreadsheet or Airtable
- Affiliate link tracking
- Affiliate disclosure
- Basic analytics
- Google Search Console
- Keyword/SERP validation before writing
- E-E-A-T/authorship plan
- Amazon Associates and direct affiliate application tracking

### Not Included In MVP

- Full interactive quiz
- User accounts
- Community loadouts
- Large product database
- Price scraping
- Automated recommendations
- Paid ads
- Knife review database
- Broad multi-persona content engine

The quiz should come later as a conversion layer after pages start getting impressions and clicks.

## 7. Launch Content Cluster

Launch with a broader beginner/budget/practical EDC cluster. Use TSA/no-knife as a specific lane, not as the entire site identity.

Recommended launch pages:

1. Everyday Carry Checklist
2. Best EDC Gear for Beginners
3. Best EDC Kit Under $50
4. Best EDC Kit Under $100
5. TSA-Friendly EDC Kit
6. Best EDC Without a Knife
7. Best Office EDC
8. Best Travel EDC
9. Best Minimalist EDC
10. Best Keychain EDC

Page rules:

- "TSA-Friendly EDC Kit" should be knife-free and cite TSA guidance conservatively.
- "Best EDC Without a Knife" should exist as one focused no-knife page.
- "Best Office EDC" should be workplace-safe and knife-optional, with alternatives.
- "Best Travel EDC" should split air travel vs road/hotel travel.
- Budget pages should not force no-knife. They should include knife and no-knife options where useful.
- The checklist should be the hub and should include optional modules: knife, no-knife, TSA-safe, office-safe, tech, medical, keys, wallet, light, pen, pouch.

## 8. Keyword And SERP Validation

No page should be produced only from intuition. Each launch page needs a lightweight keyword/SERP table before build.

Required fields:

- Target keyword
- Search intent
- Estimated monthly search volume
- Keyword difficulty
- Current top-ranking pages
- Current ranking domains' rough authority
- SERP features: AI Overview, shopping, Reddit, YouTube, forums
- Commercial intent level
- Affiliate fit
- Page decision: build, defer, or drop

Drop or defer a page if:

- Search volume appears near zero
- SERP is dominated by high-authority publishers with no clear angle
- Intent is informational with weak buyer behavior
- The page cannot include useful first-hand or editorial differentiation

The existing no-knife/TSA validation remains useful, but it should be treated as validation for two launch pages and one sub-cluster, not the whole launch plan.

## 8A. v5 Reconciliation Addendum

The repo now contains three partially conflicting launch shapes:

- the broad 10-page v4 launch list in this PRD;
- the narrower no-knife/TSA cluster validated in `docs/keyword-serp-validation-no-knife-tsa-edc.md`;
- the quiz-forward wedge described in `README.md`.

Before build, v5 should reconcile these into a validation-first Phase A.

Recommended Phase A launch set:

1. `/edc-checklist/` — Everyday Carry Checklist
2. `/best-edc-gear-for-beginners/` — Best EDC Gear for Beginners
3. `/best-edc-kit-under-100/` — Best EDC Kit Under $100
4. `/tsa-friendly-edc-kit/` — TSA-Friendly EDC Kit
5. `/best-keychain-edc/` — Best Keychain EDC
6. `/best-edc-without-a-knife/` — Best EDC Without a Knife

The Carry Builder quiz should be a later conversion layer, not a launch dependency. Do not build it until the static pages produce indexing, impressions, or tracked outbound-click evidence.

See `docs/hermes-review-and-v5-additions.md` for build gates, launch sitemap draft, analytics event spec, compliance blocks, and 30-day/120-day criteria.

Further research in `docs/further-research-recommendations-2026-06-20.md` adds three refinements:

- prioritize TSA/no-knife pages first because they have the clearest SERP gap;
- treat the keychain page as conditional until keyword validation proves a winnable angle;
- add direct affiliate targets such as Bellroy, Lever Gear, Olight, Huckberry, and CountyComm before relying on Amazon-only economics.

## 9. Content Requirements

Every page must include:

- Short answer at the top
- Clear use case
- Recommended setup
- Why each item belongs
- Who this setup is for
- Who should skip it
- Tradeoffs
- Product alternatives
- Knife/no-knife guidance where relevant
- Affiliate disclosure
- Last verified date
- Links to related pages

Avoid:

- Generic "top 25 items" lists
- Tactical/survival framing
- Repetitive AI-style intros
- Legal overclaims
- TSA overclaims
- Product recommendations without rationale
- Forcing "without a knife" into pages where it makes the article worse

## 10. E-E-A-T And Trust Plan

This is a trust-first affiliate site. The moat is editorial judgment, constraint honesty, and first-hand usefulness.

Requirements:

- Named author or editor
- Clear selection criteria
- First-hand notes or photos for at least 3 launch products
- Product tradeoffs, not just positives
- Price and availability verification cadence
- Clear distinction between tested, handled, researched, and user-reported recommendations
- Conservative language around TSA, workplace rules, and local knife laws

Minimum credibility bar for launch:

- At least 3 personally handled or tested products
- Original photos if possible
- Clear statement when a recommendation is based on research rather than hands-on testing

## 11. Product And Affiliate Data

MVP can use a spreadsheet or Airtable instead of a custom admin system.

Required fields:

- Product name
- Category
- Use case
- Price band
- Merchant
- Affiliate program
- Affiliate URL
- Non-affiliate URL
- Last price checked
- Last availability checked
- Tested/handled/researched status
- Pros
- Cons
- Best for
- Avoid if
- Constraint tags: TSA-friendly, office-safe, budget, minimalist, keychain, pouch, knife, no-knife

Initial monetization should assume Amazon Associates as the baseline. Direct affiliate programs are upside, not the base case.

## 12. Compliance

Required:

- FTC-compliant affiliate disclosure on every monetized page
- Clear Amazon Associates disclosure if Amazon links are used
- No guarantee that an item is allowed by TSA, workplace policy, or local law
- Date-stamped product and compliance checks
- Conservative wording for knives, tools, and travel

Important TSA framing:

- For air travel pages, treat knives as checked-bag-only unless official guidance says otherwise.
- Cite TSA pages for multi-tools and tools.
- Explain that final decisions can rest with TSA officers.

## 13. Success Metrics

The first validation goal is not revenue. It is proof that Google understands the site and that users click outbound.

### First 120-180 Days

Core metrics:

- 10 launch pages published
- All pages indexed or intentionally revised
- Search Console impressions growing month over month
- At least 3 pages receiving consistent impressions
- Affiliate outbound clicks tracked
- Click-through rate from content to merchant links measured
- Clear winner pages identified

Continuation signal:

- At least one cluster earns repeated impressions and outbound clicks.

Stop or revise signal:

- Pages fail to index
- No impression growth after revision
- No outbound clicks despite impressions
- SERPs are too dominated by stronger brands

## 14. MVP Build Plan

### Phase 0: Validation

- Validate the 10 launch pages with keyword/SERP tables
- Separate TSA/no-knife opportunities from broad EDC opportunities
- Confirm affiliate programs and likely monetizable products
- Build product spreadsheet
- Draft editorial standards

### Phase 1: Static Content MVP

- Publish the 10 launch pages
- Add affiliate disclosures
- Add internal links between hub and spokes
- Add analytics and Search Console
- Track outbound affiliate clicks
- Verify product availability monthly

### Phase 2: Conversion Layer

After early traffic appears, add a lightweight finder/quiz.

Possible quiz questions:

1. What is your budget?
2. Do you want to carry a knife?
3. Does this need to be TSA-friendly?
4. Is this for office, travel, school, or general daily use?
5. Do you prefer pocket, keychain, or pouch carry?
6. Do you want minimal, useful, premium, or budget gear?

The quiz should map users to existing pages and product sets, not require a full recommendation engine on day one.

## 15. Expansion Strategy

Expansion should remain cluster-led.

Good next clusters:

1. Travel EDC
2. Office EDC
3. Budget EDC
4. Minimalist EDC
5. Keychain EDC
6. Pouch EDC
7. No-knife/TSA-friendly EDC
8. Giftable EDC

Avoid launching all clusters at once. Expand from the pages that show impressions, clicks, and affiliate behavior.

## 16. Final Recommendation

Proceed, but with broader positioning than v3.

The v3 strategy was too narrow because it made "without a knife" the main brand idea. The corrected strategy is stronger:

- Everyday Carry Finder is a broad practical EDC recommender.
- TSA-friendly carry is explicitly no-knife.
- No-knife EDC is one article and one useful lane.
- Budget, beginner, office, travel, minimalist, and keychain EDC should not be artificially stripped of knives.
- The first MVP should be a static SEO content product, then add a quiz once the content shows traction.

This keeps the strategic SEO wedge without making the whole product feel lame or overly constrained.
