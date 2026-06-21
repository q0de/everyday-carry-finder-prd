# Everyday Carry Finder PRD

This repo contains the current product strategy and PRD materials for **Everyday Carry Finder**, a practical EDC recommendation site and quiz/finder concept.

## Canonical PRD

The current source of truth is:

- [PRD-v5-build-ready.md](./PRD-v5-build-ready.md)

Use that file for build decisions. Older docs are appendices and should not override the v5 PRD.

## Core Idea

Everyday Carry Finder helps people build practical everyday carry setups based on budget, lifestyle, pocket space, travel/work constraints, and personal preferences.

The product should not be a knife-first EDC site or a no-knife-only site. The current strategy is a validation-first beginner/budget/constraint wedge.

## Recommended MVP Wedge

Launch a small static test instead of building the full system:

1. `/edc-checklist/` - Everyday Carry Checklist
2. `/best-edc-gear-for-beginners/` - Best EDC Gear for Beginners
3. `/best-edc-kit-under-100/` - Best EDC Kit Under $100
4. `/tsa-friendly-edc-kit/` - TSA-Friendly EDC Kit
5. `/best-keychain-edc/` - Best Keychain EDC
6. `/best-edc-without-a-knife/` - Best EDC Without a Knife

The first validation goal is SEO traction and affiliate outbound click behavior, not immediate profit.

The Carry Builder quiz is a Phase C conversion layer, not part of the MVP build.

## Files

- [PRD-v5-build-ready.md](./PRD-v5-build-ready.md): canonical build-ready v5 PRD.
- [PRD.md](./PRD.md): older v4 PRD preserved as background.
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

There was a deliberate tension between the broader 10-page PRD and the no-knife/TSA validation doc. That has been resolved in [PRD-v5-build-ready.md](./PRD-v5-build-ready.md): build a **validation-first 6-page Phase A** before building the Carry Builder quiz or a larger content engine.
