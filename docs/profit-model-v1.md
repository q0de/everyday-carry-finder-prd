# Everyday Carry Finder Profit Model v1

Updated: June 21, 2026

## Short Answer

The current PRD does not yet include estimated profits. That should be a separate financial model, with a short summary copied into PRD v5.

Reason: the PRD should define what to build and why. The profit model should define assumptions, scenarios, and what has to be true for the project to be worth continuing.

This v1 model is directional, not a forecast.

## Key Assumptions

### Monetization

Baseline monetization:

- Amazon Associates for launch.
- Direct affiliate programs added later where available.
- No ads in MVP.
- No paid product in MVP.

Important Amazon notes:

- Amazon says Associates can earn commission from qualifying purchases, with rates varying by category.
- Amazon's public Associates page says publishers can earn "up to 10%" in associate commissions.
- Amazon's 24-hour session window applies after a customer clicks an Associates link, with a longer cart exception if the item is added during that window.
- Amazon payments are typically made about 60 days after the end of the earned month if payment thresholds and tax info are satisfied.
- Amazon Associates can close an account if it does not generate the required qualifying sales within the initial approval window; do not start that clock before the site can plausibly drive purchases.

Sources:

- Amazon Associates: https://affiliate-program.amazon.com/
- Amazon standard commission income rates: https://affiliate-program.amazon.com/help/node/topic/GRXPHT8U84RAYDXZ
- Amazon 24-hour session explanation: https://affiliate-program.amazon.com/help/node/topic/G9SMD8TQHFJ7728F
- Amazon payment timing: https://affiliate-program.amazon.com/help/node/topic/G63DR893K4DH55XZ

### Product Economics

Likely average order values:

| Product Type | Typical Price Band | Notes |
|---|---:|---|
| Pens | $8-$40 | Low AOV, useful add-ons |
| Wallets | $15-$80 | Good beginner/budget fit |
| Flashlights | $15-$80 | Strong EDC fit |
| Knives | $20-$120 | Useful where appropriate, but not brand center |
| Multitools | $15-$120 | Strong affiliate fit |
| Key organizers/tools | $10-$60 | Good keychain page fit |
| Pouches/organizers | $15-$80 | Good travel/kit fit |
| Chargers/cables | $10-$80 | Good travel/tech add-ons |

Estimated blended order value:

- Conservative: $35
- Base: $55
- Upside: $85

Estimated blended commission rate:

- Conservative: 2.5%
- Base: 3.5%
- Upside with direct programs: 6.0%

Estimated commission per purchase:

| Scenario | AOV | Commission Rate | Cookie Duration | Earnings Per Purchase |
|---|---:|---:|---:|---:|
| Conservative | $35 | 2.5% | 24 hours | $0.88 |
| Base | $55 | 3.5% | 24 hours to 7 days | $1.93 |
| Upside | $85 | 6.0% | 14-30 days | $5.10 |

Direct-affiliate upside is not just higher commission rate; longer cookie windows can materially improve realized EPC. Example: a $60 wallet at 8% commission with a 30-day direct-program cookie can be worth $4.80 per purchase versus $1.80 at a 3% Amazon-like rate with a 24-hour window. Program research should capture commission rate, cookie duration, network, approval requirements, and traffic/sales thresholds before application. Conservative assumes Amazon-heavy economics; upside assumes direct-program approval and longer-cookie economics.

## Traffic And Conversion Model

Definitions:

- Sessions: visits to the site.
- Affiliate click rate: percent of sessions that click a merchant/product link.
- Purchase conversion: percent of affiliate clicks that turn into purchases.
- Earnings per purchase: average commission earned per completed purchase.

Formula:

```text
Monthly revenue = sessions × affiliate click rate × purchase conversion × earnings per purchase
```

## Monthly Revenue Scenarios

### Early MVP

| Scenario | Monthly Sessions | Affiliate Click Rate | Purchase Conversion | Earnings/Purchase | Monthly Revenue |
|---|---:|---:|---:|---:|---:|
| Conservative | 1,000 | 8% | 3% | $0.88 | $2 |
| Base | 2,500 | 12% | 5% | $1.93 | $29 |
| Upside | 5,000 | 18% | 7% | $5.10 | $321 |

Takeaway:

The MVP is unlikely to make meaningful money immediately. The first goal is proof of SEO traction and affiliate click behavior, not profit.

### Small Working Site

| Scenario | Monthly Sessions | Affiliate Click Rate | Purchase Conversion | Earnings/Purchase | Monthly Revenue |
|---|---:|---:|---:|---:|---:|
| Conservative | 10,000 | 10% | 4% | $0.88 | $35 |
| Base | 25,000 | 14% | 5% | $1.93 | $338 |
| Upside | 50,000 | 20% | 7% | $5.10 | $3,570 |

Takeaway:

Meaningful revenue likely requires either:

- much more traffic,
- better direct affiliate rates,
- higher-AOV products,
- strong quiz conversion,
- or a non-affiliate monetization layer.

### Strong Niche Site

| Scenario | Monthly Sessions | Affiliate Click Rate | Purchase Conversion | Earnings/Purchase | Monthly Revenue |
|---|---:|---:|---:|---:|---:|
| Conservative | 75,000 | 12% | 4% | $0.88 | $317 |
| Base | 150,000 | 16% | 5% | $1.93 | $2,316 |
| Upside | 300,000 | 22% | 7% | $5.10 | $23,562 |

Takeaway:

The upside exists, but only if the site becomes a real content asset with winning pages, better affiliate programs, and strong recommendation UX.

## Page-Level Monetization Strength

| Page | Traffic Role | Buyer Intent | Monetization Strength | Notes |
|---|---|---:|---:|---|
| Everyday Carry Checklist | Hub/trust | Medium | Medium | Broad traffic, many internal links |
| Best EDC Gear for Beginners | Buyer/trust | High | High | Strong recommendation fit |
| Best EDC Kit Under $100 | Buyer | High | High | Better AOV and useful products |
| Best EDC Kit Under $50 | Conditional buyer page | High | Medium | Lower AOV; build only if chosen over keychain page |
| TSA-Friendly EDC Kit | Constraint buyer | High | High | Strong fit for pouches, pens, lights, chargers |
| Best EDC Without a Knife | Constraint buyer | Medium-high | Medium-high | Good gap page, not whole brand |
| Best Office EDC | Lifestyle buyer | Medium-high | Medium-high | Wallets, pens, bags, slim tools |
| Best Travel EDC | Buyer | High | High | Travel gear and pouches can lift AOV |
| Best Minimalist EDC | Buyer/trust | Medium | Medium | Competitive, but good internal value |
| Best Keychain EDC Without Bulk | Conditional buyer page | High | Medium | Lower AOV but strong product fit; build only if SERP validation beats under-$50 page |

## Costs

Expected MVP costs if bootstrapped:

| Cost | Monthly Estimate | Notes |
|---|---:|---|
| Domain | $1-$2 | Annualized |
| Hosting | $0-$25 | Static/low-traffic app |
| Analytics | $0-$20 | Depends on tool |
| SEO tools | $0-$150 | Can start manual/lightweight |
| Product samples | $50-$300 | Variable; important for trust |
| Content production | $0-$2,000+ | Depends on who writes/tests |

Real cost issue:

The main cost is not hosting. It is content, testing products, editing, updating, and getting enough pages to rank.

## Break-Even Examples

If monthly fixed costs are $100:

| Scenario | Earnings/Purchase | Purchases Needed / Month | Approx Affiliate Clicks Needed at 5% Purchase Conversion |
|---|---:|---:|---:|
| Conservative | $0.88 | 114 | 2,280 |
| Base | $1.93 | 52 | 1,040 |
| Upside | $5.10 | 20 | 400 |

If monthly fixed costs are $500:

| Scenario | Earnings/Purchase | Purchases Needed / Month | Approx Affiliate Clicks Needed at 5% Purchase Conversion |
|---|---:|---:|---:|
| Conservative | $0.88 | 568 | 11,360 |
| Base | $1.93 | 260 | 5,200 |
| Upside | $5.10 | 99 | 1,980 |

## What Has To Be True

For this to become meaningfully profitable, at least one of these must happen:

1. Several pages rank and produce meaningful organic traffic.
2. The quiz increases affiliate click-through rate materially.
3. Direct affiliate programs lift commission rates above Amazon baseline.
4. The site recommends higher-AOV bundles, not just single cheap items.
5. The brand later adds a higher-margin revenue layer.

Possible higher-margin layers:

- Sponsored placements, clearly disclosed.
- Paid downloadable packing/checklist guides.
- Email newsletter sponsorships.
- Direct commerce bundles.
- Lead-gen partnerships with gear brands.
- A premium "build my kit" service.

## Recommendation For PRD v5

Do not put the full financial model inside the PRD.

Add a short section:

> MVP revenue is expected to be low during the first 120-180 days. The primary validation metric is SEO traction and affiliate outbound behavior, not profit. A separate financial model estimates that meaningful monthly revenue likely requires tens of thousands of monthly sessions, improved affiliate rates through direct programs, or a higher-margin monetization layer.

Then link to this document as the financial appendix.

## Current Decision

The project is still worth testing, but only as a low-cost SEO/content MVP.

Do not spend heavily on development, paid ads, or a complex quiz until the first pages show impressions and outbound click behavior.
