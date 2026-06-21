# Everyday Carry Finder Freshness Ops Addendum

Updated: June 20, 2026

## Why This Matters

EDC affiliate content decays quickly.

Products go out of stock, prices change, brands release lookalike junk, Amazon listings mutate, new gear trends appear on YouTube/Reddit, and older recommendations can become embarrassing fast. If Everyday Carry Finder is going to be trusted, it needs an update system from day one.

This should be added to PRD v5 as a required operating system, not a nice-to-have.

## Recommendation

Use a two-layer freshness system:

1. **Web intelligence layer**
   - Use Tavily or a similar real-time web search/extraction API to monitor the broader EDC market.
   - Purpose: discover new products, trend shifts, Reddit/forum complaints, recall/safety issues, and competitor updates.

2. **Product data verification layer**
   - Use official affiliate/product APIs where possible for prices, availability, merchant URLs, and product metadata.
   - For Amazon, use the official current Amazon affiliate/product API path rather than scraping Amazon pages.
   - Purpose: avoid stale prices, broken links, unavailable products, and compliance problems.

Tavily is good for discovery and evidence gathering. It should not be the only source of truth for price/availability.

## Freshness Cadence

### Daily Checks

Run lightweight automated checks daily for:

- Broken affiliate links
- Products returning 404/unavailable
- Amazon/merchant pages with unavailable indicators
- Major price changes if API access exists
- Pages with high outbound click volume
- Top recommended products
- TSA/legal source page changes for relevant travel content

Daily output:

- Freshness queue with product/page issues.
- Severity labels: critical, warning, watch.

Critical examples:

- Product unavailable
- Affiliate link broken
- Product replaced by unrelated listing
- TSA guidance changed
- Product has major safety complaint trend

### Weekly Checks

Run broader market monitoring weekly:

- Search for new EDC product launches
- Search for "best EDC gear" competitor updates
- Scan Reddit/forums for repeated product complaints
- Check YouTube for new high-engagement EDC roundups
- Check manufacturer/new-arrivals pages for known brands
- Review top 10 launch pages for stale recommendations
- Refresh "last checked" dates when product data is verified

Weekly output:

- Products to add
- Products to remove
- Products to demote
- Pages needing update
- New content ideas
- Competitor movements

### Monthly Checks

Run deeper editorial refresh:

- Re-score all recommended products
- Update comparison tables
- Review affiliate performance by product/page
- Replace weak products with better converters or better-reviewed options
- Add first-hand testing notes/photos where possible
- Re-check SEO titles/meta against Search Console performance
- Review direct affiliate program opportunities

Monthly output:

- Updated page changelog
- Product database refresh
- Affiliate performance report
- New testing/sample purchase list

## Freshness Data Model

Every product should have these fields:

- `product_id`
- `product_name`
- `brand`
- `category`
- `merchant`
- `affiliate_program`
- `affiliate_url`
- `canonical_product_url`
- `price_last_seen`
- `availability_status`
- `last_price_checked_at`
- `last_availability_checked_at`
- `last_editorial_review_at`
- `last_external_signal_check_at`
- `recommendation_status`
- `freshness_status`
- `risk_flags`
- `source_urls`
- `notes`

Recommended `recommendation_status` values:

- `recommended`
- `recommended_with_caution`
- `testing`
- `watch`
- `demoted`
- `removed`

Recommended `freshness_status` values:

- `fresh`
- `needs_review`
- `stale`
- `broken`
- `unavailable`
- `replaced`

Recommended `risk_flags`:

- `price_changed`
- `out_of_stock`
- `listing_changed`
- `quality_complaints`
- `safety_complaints`
- `affiliate_link_broken`
- `merchant_changed`
- `legal_or_tsa_risk`
- `needs_hands_on_review`

## Tavily-Like Web Intelligence Workflows

Use Tavily or an equivalent search/extraction API for questions like:

- What new products are people discussing in EDC communities this week?
- Are there repeated complaints about a recommended product?
- Did a major gear publisher update a competing article?
- Are there new TSA-friendly or bladeless multitools being recommended?
- Are any recommended brands getting quality complaints?
- Are there new budget EDC products under $50/$100?
- Are top YouTube creators pushing a new product category?

Example recurring queries:

```text
site:reddit.com/r/EDC "broke" "wallet" OR "flashlight" past week
"best EDC gear" "2026" "updated"
"TSA friendly multitool" new
"EDC kit under $50" "2026"
"keychain EDC" "new" "review"
"[product name]" "broke" OR "returned" OR "junk"
"[brand name]" "quality control" OR "QC"
```

Use results to create an editorial review queue, not automatic page changes.

## Product Update Rules

### Remove Or Demote Product If

- It is unavailable for more than 14 days.
- Affiliate link is broken.
- Listing changes to a materially different product.
- Price rises above the page's promised budget band.
- Repeated credible complaints appear.
- Better alternatives exist at the same price.
- The product conflicts with a page constraint, such as TSA-friendly or office-safe.

### Keep Product If

- Price is stable.
- Availability is stable.
- Reviews/signals remain positive.
- It still fits the page's constraint.
- It has good outbound click or conversion behavior.
- There is no clearly better replacement.

### Mark As Watch If

- Price jumps sharply.
- Stock is intermittent.
- New complaints appear but are not decisive.
- A new version/model may be replacing it.
- Merchant changes create affiliate risk.

## Page Freshness Rules

Every monetized page should show:

- Last updated date
- Product prices last checked date, if prices are displayed
- Editorial review date
- Affiliate disclosure
- Tested/researched labels

Update frequency:

| Page Type | Review Frequency |
|---|---:|
| Best/buyer pages | Monthly |
| Budget pages | Every 2-4 weeks |
| TSA/legal-sensitive pages | Monthly plus source-change watch |
| Checklist/hub page | Monthly |
| Low-traffic informational pages | Quarterly |

## Automation Architecture

Suggested MVP architecture:

- `products` table or spreadsheet as the source of truth.
- `product_checks` table for automated runs.
- `page_checks` table for page-level freshness.
- Scheduled daily job for link/availability checks.
- Scheduled weekly job for Tavily-style discovery.
- Admin/editor queue for human approval.
- Changelog stored per product and page.

Do not auto-publish recommendation changes without review.

## Freshness Queue

The update system should produce a queue like:

| Severity | Type | Item | Reason | Suggested Action |
|---|---|---|---|---|
| Critical | Product | Example flashlight | Out of stock 7 days | Replace or mark unavailable |
| Critical | Link | Example wallet | Affiliate URL broken | Update link |
| Warning | Product | Example pouch | Price up 28% | Move out of budget page |
| Watch | Trend | TSA multitool | New competitor product trending | Research for next update |
| Watch | Quality | Example key tool | Reddit complaints increasing | Investigate |

## Technical Notes

Potential integrations:

- Tavily for web search, extraction, research, and crawling.
- Amazon official product/affiliate API path for Amazon product metadata where available.
- Merchant-specific affiliate feeds where direct programs provide them.
- Cron/scheduled jobs for daily and weekly checks.
- Search Console API for page trend monitoring later.

Important:

- Tavily can discover and summarize external signals.
- Official merchant/affiliate APIs should handle price and availability when possible.
- Human editorial review should approve recommendation changes.

## Acceptance Criteria

Freshness system is MVP-ready when:

- Every recommended product has a `last_checked_at` date.
- Every monetized page has a visible `last_updated` date.
- Broken affiliate links can be detected.
- Unavailable products can be flagged.
- Budget-page products can be flagged when price exceeds the budget.
- Tavily-like weekly discovery produces a review queue.
- Editors can mark product status as recommended, watch, demoted, or removed.
- Recommendation changes are logged.

## PRD v5 Addition

Add this section to PRD v5:

> Everyday Carry Finder requires a freshness operations layer. Because EDC products change quickly and affiliate recommendations decay, the MVP must include product/page freshness fields, daily link and availability checks, weekly market monitoring using Tavily or a similar web intelligence API, and a human editorial review queue. Tavily should be used for discovery, trend monitoring, competitor updates, and complaint detection. Official merchant or affiliate APIs should be used for price and availability where possible. No product recommendation should be changed automatically without editorial approval.

## Sources

- Tavily docs: https://docs.tavily.com/welcome
- Tavily API endpoints: https://docs.tavily.com/documentation/api-reference/introduction
- Tavily search endpoint: https://docs.tavily.com/documentation/api-reference/endpoint/search
- Amazon Product Advertising API documentation: https://webservices.amazon.com/paapi5/documentation/
- Amazon PA-API SearchItems documentation: https://webservices.amazon.com/paapi5/documentation/search-items.html
- Amazon offer information documentation: https://webservices.amazon.com/paapi5/documentation/use-cases/using-offer-information/determining-price-merchant-and-delivery-information.html
