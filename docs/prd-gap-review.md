# PRD Gap Review: Everyday Carry Finder v4

Reviewed: June 20, 2026

## Bottom Line

The v4 PRD fixes the biggest positioning issue: the product is no longer trapped in "without a knife" territory. It now has a broader, more credible EDC strategy with TSA/no-knife as one lane.

What is still missing is execution specificity. The PRD explains what the product should be, but it does not yet fully define how to validate, build, publish, measure, and monetize it.

Recommendation: create a v5 PRD before build. v5 should keep the v4 positioning, but add page-level SEO validation, site architecture, analytics events, product data requirements, acceptance criteria, and a realistic launch checklist.

## What Is Strong

- Clearer positioning: broad practical EDC, not a no-knife-only site.
- Better launch cluster: beginner, budget, checklist, TSA, office, travel, minimalist, keychain.
- Correct handling of knives: optional except for TSA/no-knife pages.
- Good phased approach: static SEO pages first, quiz later.
- Strong trust framing: editorial judgment, tradeoffs, disclosures, update cadence.
- Sensible monetization assumption: Amazon baseline, direct affiliate programs as upside.

## Biggest Missing Pieces

### 1. Page-Level SEO Validation For The New 10-Page Cluster

The existing keyword/SERP validation only validates the no-knife/TSA wedge. The PRD now recommends a broader launch cluster, but the broader pages have not been validated yet.

Missing validation for:

- Everyday Carry Checklist
- Best EDC Gear for Beginners
- Best EDC Kit Under $50
- Best EDC Kit Under $100
- Best Office EDC
- Best Travel EDC
- Best Minimalist EDC
- Best Keychain EDC

Why this matters:

Some of these are likely much more competitive than the no-knife pages. The PRD should not commit to all 10 pages until the SERPs confirm there is a winnable angle.

Needed addition:

- A keyword/SERP validation table for all 10 launch pages.
- A final decision for each page: build, reframe, defer, or replace.

### 2. Site Architecture And URL Plan

The PRD lists pages, but it does not define the structure of the site.

Missing:

- URL slugs
- Hub/spoke model
- Navigation
- Breadcrumbs
- Internal linking rules
- Related article blocks
- Product comparison blocks
- Category/tag structure

Suggested structure:

- `/edc-checklist/`
- `/best-edc-gear-for-beginners/`
- `/best-edc-kit-under-50/`
- `/best-edc-kit-under-100/`
- `/tsa-friendly-edc-kit/`
- `/best-edc-without-a-knife/`
- `/best-office-edc/`
- `/best-travel-edc/`
- `/best-minimalist-edc/`
- `/best-keychain-edc/`

Needed addition:

- A launch sitemap with URL, primary keyword, search intent, page type, internal links in, and internal links out.

### 3. Page Template And Editorial Briefs

The PRD says what every page must include, but it does not define reusable page formats.

Missing:

- Page outline template
- Product card requirements
- Comparison table format
- "Best for / avoid if" module
- Disclosure placement
- Last-updated placement
- Testing/research note placement
- CTA language

Needed addition:

- One reusable content brief template.
- One sample brief for the highest-priority page.

Recommended first sample:

- `Everyday Carry Checklist`, because it can become the site hub.

### 4. Product Seed List

The PRD says to use a spreadsheet or Airtable, but it does not define the initial inventory.

Missing:

- Minimum number of products needed at launch
- Product categories
- Product selection rules
- Product exclusion rules
- Merchant strategy
- Direct affiliate targets
- Amazon fallback logic

Suggested launch inventory:

- 8-12 wallets/card holders
- 8-12 flashlights
- 8-12 pens
- 6-10 multitools
- 6-10 key organizers/keychain tools
- 6-10 pouches/organizers
- 6-10 chargers/cables
- 4-8 knives
- 4-8 medical/safety items
- 4-8 travel-safe alternatives

Needed addition:

- A seed product database with 75-100 candidate products before writing final articles.

### 5. Monetization Model Is Too Thin

The PRD says Amazon baseline and direct affiliates as upside, but it does not define expected economics.

Missing:

- Expected average order value by category
- Estimated commission by merchant/category
- Conversion assumptions
- Revenue sensitivity model
- Which pages are likely to monetize best
- Which pages are mostly traffic/trust builders

Needed addition:

- A simple unit economics table by page and product category.

Example:

| Page | Monetization Strength | Likely Products | Revenue Role |
|---|---:|---|---|
| Best EDC Kit Under $100 | High | Wallets, lights, pens, pouches, tools | Buyer page |
| Everyday Carry Checklist | Medium | Many categories | Hub/trust page |
| TSA-Friendly EDC Kit | High | Pouches, pens, lights, chargers, bladeless tools | Constraint buyer page |
| Best Office EDC | Medium-high | Wallets, pens, lights, bags | Lifestyle buyer page |

### 6. Analytics Plan Needs Event-Level Detail

The PRD says to track outbound clicks, but not how.

Missing:

- Analytics tool choice
- Event names
- Required event properties
- Dashboard/reporting cadence
- Search Console review cadence
- Success thresholds by date

Needed addition:

Core events:

- `affiliate_click`
- `product_card_click`
- `comparison_table_click`
- `quiz_start`
- `quiz_complete`
- `recommendation_click`
- `internal_related_page_click`

Core properties:

- page_slug
- product_id
- product_category
- merchant
- price_band
- affiliate_program
- position_on_page
- recommendation_type

### 7. Acceptance Criteria Are Missing

The PRD has success metrics, but not build acceptance criteria.

Missing:

- What must be true before launch?
- What makes a page publishable?
- What makes the MVP complete?
- What makes the quiz ready?

Needed addition:

Launch acceptance criteria:

- 10 pages published or intentionally reduced after SERP validation.
- Every page has disclosure, last-updated date, author, internal links, product rationale, and at least 5 recommended products.
- Every monetized link is tracked.
- Search Console and analytics are installed.
- Product database has required fields filled.
- TSA/legal/compliance language reviewed for relevant pages.

### 8. Compliance Needs More Affiliate Detail

The compliance section is directionally right, but it needs more operational rules.

Missing:

- Amazon image usage rules
- Amazon price display rules
- Rules for email/social affiliate links
- Required disclaimer templates
- Product availability update rules
- Process for removing unavailable products

Needed addition:

- A compliance checklist before publication.
- A standard disclosure block.
- A TSA disclaimer block.
- A knife/legal disclaimer block.

### 9. First-Hand Testing Plan Is Too Vague

The PRD says at least 3 handled/tested products, but that is probably too low for a trust-first affiliate site.

Missing:

- Which categories need first-hand testing first
- Photo requirements
- Testing criteria
- How to label researched vs tested products
- Plan for updating pages as testing expands

Suggested minimum:

- Launch with at least 10 personally handled/tested products across 4 categories.
- Use original photos for hub/checklist and at least 3 buyer pages.

### 10. Technical Scope Is Undefined

The PRD does not specify how the site will be built.

Missing:

- CMS/static framework choice
- Hosting
- Content editing workflow
- Product database source
- Affiliate redirect/tracking approach
- Schema strategy
- Page performance requirements
- Image optimization

Needed addition:

- Technical implementation section.

Suggested lightweight approach:

- Static site or Next.js content site
- Markdown/MDX for articles
- JSON/CSV/Airtable product source
- Tracked outbound redirect route
- Product, Article, Breadcrumb, and FAQ schema where appropriate

### 11. Competitive Differentiation Needs Sharpening

The PRD says "constraint-led," which is good, but it needs sharper proof.

Missing:

- Specific competitor set
- What competitors do poorly
- What Everyday Carry Finder will do differently
- Why users should trust this site over Reddit, YouTube, or big gear publishers

Needed addition:

- Competitive positioning table.

Differentiators to test:

- Practical setups, not gear flexing
- Budget-aware recommendations
- Knife optional, not knife obsessed
- Clear "skip this if" guidance
- Constraint filters by travel, office, budget, and pocket space
- Honest tested/researched labels

### 12. Roadmap Needs Dates And Decision Gates

The PRD has phases, but not timeline or gates.

Missing:

- Launch timeline
- Weekly milestones
- Who owns each task
- Decision points
- What happens if validation fails

Needed addition:

- 6-week build plan.
- 120-day validation plan.
- Explicit continue/pivot/kill criteria.

## Priority Fixes For v5

### Must Add Before Build

1. SERP validation for all 10 revised launch pages.
2. Launch sitemap with URLs and internal links.
3. Page template/content brief.
4. Product seed database requirements.
5. Analytics event spec.
6. Launch acceptance criteria.

### Should Add Before Publishing

1. Affiliate compliance checklist.
2. Standard disclosure blocks.
3. Technical implementation plan.
4. First-hand testing/photo plan.
5. Unit economics table.

### Can Add Later

1. Full quiz logic.
2. User accounts.
3. Community loadouts.
4. Advanced recommendation engine.
5. Direct affiliate expansion roadmap.

## Recommended Next Step

Create PRD v5 with these new sections:

1. Final launch page validation table
2. Launch sitemap and internal linking plan
3. Page template
4. Product database and seed inventory plan
5. Analytics and tracking spec
6. Compliance checklist
7. Technical implementation plan
8. Launch acceptance criteria
9. 6-week execution roadmap

After v5, the next artifact should be the `Everyday Carry Checklist` content brief, because that page is likely the hub of the whole site.
