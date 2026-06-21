# Everyday Carry Finder PRD

This repo contains the current product strategy and PRD materials for **Everyday Carry Finder**, a practical EDC recommendation site and quiz/finder concept.

## Core Idea

Everyday Carry Finder helps people build practical everyday carry setups based on budget, lifestyle, pocket space, travel/work constraints, and personal preferences.

The product should not be a knife-first EDC site or a no-knife-only site. The current strategy is a focused beginner/budget wedge with a fun **Carry Builder** quiz.

## Recommended MVP Wedge

Launch a small test instead of building the full system:

1. Everyday Carry Checklist
2. Best EDC Gear for Beginners
3. Best EDC Kit Under $50
4. Best EDC Kit Under $100
5. TSA-Friendly EDC Kit
6. Best Keychain EDC
7. Carry Builder quiz

The first validation goal is SEO traction and affiliate outbound click behavior, not immediate profit.

## Files

- [PRD.md](./PRD.md): current main PRD.
- [docs/prd-gap-review.md](./docs/prd-gap-review.md): what is still missing before build.
- [docs/quiz-experience-addendum.md](./docs/quiz-experience-addendum.md): Carry Builder quiz UX and game-like interaction requirements.
- [docs/freshness-ops-addendum.md](./docs/freshness-ops-addendum.md): daily/weekly update system, Tavily-like monitoring, product freshness requirements.
- [docs/profit-model-v1.md](./docs/profit-model-v1.md): rough affiliate revenue model and assumptions.
- [docs/keyword-serp-validation-no-knife-tsa-edc.md](./docs/keyword-serp-validation-no-knife-tsa-edc.md): initial SERP validation for the TSA/no-knife subcluster.
- [docs/hermes-review-and-v5-additions.md](./docs/hermes-review-and-v5-additions.md): reconciled MVP recommendation, v5 additions, build gates, sitemap draft, analytics spec, and 30-day/120-day criteria.
- [templates/product-seed-template.csv](./templates/product-seed-template.csv): starter product data sheet schema for candidate recommendations.
- [REVIEW_PROMPT.md](./REVIEW_PROMPT.md): prompt to give another LLM for critique.

## Review Goal

The next reviewer should evaluate whether this is a smart MVP wedge, what is missing from the PRD, what should be cut, and what should be validated before any real build.

## Current Reconciliation Note

There is a deliberate tension between the broader 10-page PRD and the no-knife/TSA validation doc. The latest recommendation is to treat the project as a **validation-first 6-page Phase A** before building the Carry Builder quiz or a larger content engine. See [docs/hermes-review-and-v5-additions.md](./docs/hermes-review-and-v5-additions.md).
