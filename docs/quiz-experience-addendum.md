# Everyday Carry Finder Quiz Experience Addendum

Updated: June 20, 2026

## Purpose

The quiz should not feel like a generic lead form. It should feel like a fast, playful gear-matching experience: tactile, visual, and slightly game-like, while still producing credible recommendations.

Reference inspirations:

- MED-FINDER: staged intake, progress bars, captured summary chips, animated result reveal, count-up numbers, shareable result state.
- CarCheck: deterministic rules/checks behind the UI, save chips, stateful multi-step flow, clear review/result logic.
- Animation skillsets: tactile input response, reward bursts, progress surges, streak-like momentum, reduced-motion support.

## Product Principle

The quiz is a recommendation game, not a form.

It should make the user feel like they are building a loadout. Each answer adds a visible piece to their carry profile. The final result should feel earned, like the site assembled a personalized kit from their constraints.

## Quiz Name Ideas

- Carry Builder
- Loadout Finder
- Pocket Build
- Carry Match
- Daily Kit Builder
- Setup Finder

Recommendation: use **Carry Builder** in-product. It is clear, simple, and slightly game-like without sounding tactical.

## Core Flow

The quiz should be 6-8 steps max.

Recommended steps:

1. Carry goal
   - Everyday basics
   - Office/work
   - Travel
   - Minimalist pocket
   - Keychain setup
   - Emergency backup

2. Budget
   - Under $50
   - Under $100
   - Under $200
   - Best value
   - Premium but practical

3. Carry style
   - Front pocket
   - Keychain
   - Small pouch
   - Bag/backpack
   - Mix of these

4. Knife preference
   - Yes, recommend one
   - Maybe, show optional
   - No knife
   - TSA-friendly only

5. Style preference
   - Clean/professional
   - Minimal
   - Rugged
   - Tech-focused
   - Low-profile

6. Must-have categories
   - Wallet
   - Pen
   - Flashlight
   - Multitool
   - Knife
   - Charger/cable
   - Pouch
   - Key organizer
   - Small medical/safety

7. Pocket tolerance
   - Barely anything
   - A few slim items
   - Normal pockets are fine
   - I carry a pouch/bag

8. Result reveal
   - Show setup name
   - Match score
   - Recommended kit
   - Budget estimate
   - Constraint badges
   - Product cards
   - Related guide links

## Game-Like Interaction Requirements

### 1. Each Answer Should Feel Physical

Every selected option should respond immediately:

- Button/card compresses on tap.
- Selected card pops slightly on release.
- A rim glow or fill confirms the answer.
- The answer becomes a small captured chip in the running profile.

Timing:

- Press response: 40-90ms.
- Selection pop: 120-220ms.
- Step transition: 260-420ms.

### 2. Build A Visible Carry Profile As The User Answers

Keep a small "Your Carry" strip or side panel that fills as the user progresses.

Example chips:

- Office
- Under $100
- Front pocket
- Knife optional
- Minimal
- Pen + light + wallet

This borrows from MED-FINDER's captured chip pattern and makes progress feel concrete.

### 3. Use A Loadout Meter Instead Of A Plain Progress Bar

The progress indicator should feel themed:

- 6-8 small slots representing the carry build.
- Each completed step fills one slot.
- Milestones can trigger a subtle progress surge.
- On final step, the bar resolves into a "Kit Ready" state.

Avoid fake scoring that implies scientific precision. Use labels like:

- Getting started
- Taking shape
- Nearly built
- Kit ready

### 4. Make Results Feel Like A Reveal

The result page should animate in stages:

1. "Building your kit..." micro-loading state.
2. Constraint chips lock into place.
3. Setup name appears.
4. Match score/count-up appears.
5. Product categories slide in.
6. Product cards reveal in priority order.

Example setup names:

- The Office Minimalist
- The Travel-Safe Kit
- The Under-$100 Starter
- The Pocket-Light Setup
- The Keychain Utility Kit
- The Everyday Essentials Kit

### 5. Use Reward, Not Noise

Use animation for meaningful moments:

- Step completed
- Useful constraint captured
- Budget matched
- Kit complete
- Product recommendation revealed

Do not animate every idle card or every line of text.

Recommended effects:

- Small particles only on final kit completion or major milestone.
- Button pop for selections.
- Captured chip float for completed answers.
- Progress surge after each step.
- Count-up for estimated total price or match score.

### 6. Keep Mistakes Recoverable

If the user chooses incompatible answers, do not block them harshly.

Examples:

- TSA-friendly + knife selected:
  - Soft amber nudge: "For carry-on travel, knives move to checked-bag options."
  - Auto-adjust result to TSA-safe.

- Under $50 + many categories:
  - "Tight budget. We'll prioritize the essentials first."

- Front pocket + pouch selected:
  - "We'll keep pocket items slim and put extras in a pouch."

Use short nudge animations, not red error states, unless the user cannot proceed.

## Recommendation Logic

Behind the playful UI, the quiz needs deterministic rules.

Each answer should map to stable fields:

```json
{
  "carry_goal": "office",
  "budget": "under_100",
  "carry_style": "front_pocket",
  "knife_preference": "optional",
  "style": "minimal",
  "must_have_categories": ["wallet", "pen", "flashlight"],
  "pocket_tolerance": "few_slim_items"
}
```

Rules should produce:

- Setup type
- Product category priorities
- Excluded categories
- Budget allocation
- Constraint badges
- Related article recommendations

Example rules:

- If `knife_preference = tsa_friendly`, exclude knives from carry-on recommendations.
- If `budget = under_50`, cap product count and prioritize wallet/pen/light/keychain.
- If `carry_style = front_pocket`, prefer slim wallets, compact pens, small flashlights, and no bulky pouches.
- If `carry_goal = office`, prioritize non-tactical styling and low-bulk products.
- If `carry_goal = travel`, split air-travel-safe from checked-bag/general travel recommendations.

## Result Page Requirements

The result page should include:

- Setup name
- One-sentence rationale
- Match confidence label
- Estimated kit cost
- Constraint badges
- Recommended categories in priority order
- Product cards
- "Best for / avoid if" section
- Optional swaps
- Related guides
- Affiliate disclosure

Recommended result layout:

1. Hero result block
   - Setup name
   - Match score or confidence
   - Budget estimate
   - Key badges

2. Your carry profile
   - Answers summarized as chips

3. Recommended kit
   - Product cards grouped by priority

4. Optional upgrades/swaps
   - Knife option
   - No-knife option
   - Travel-safe option
   - Budget save option

5. Related guides
   - Link to the closest SEO page

## Product Card Requirements

Each card should include:

- Product name
- Category
- Price band
- Best for
- Avoid if
- Constraint badges
- Tested/handled/researched label
- Affiliate CTA

Card interaction:

- Hover/tap lift.
- CTA press pop.
- Badge reveal on focus/hover if needed.
- No distracting idle animation.

## Motion And Animation Spec

Use motion sparingly but deliberately.

Default timing:

- Tap down: 40-90ms.
- Selection confirmation: 120-220ms.
- Step exit/enter: 260-420ms.
- Progress fill: 300-500ms.
- Result reveal: 450-700ms.
- Major completion celebration: 700ms max.

Reduced-motion mode:

- Remove particles.
- Remove shake.
- Replace sliding transitions with fades.
- Keep progress updates instant or very short.

Performance rules:

- Prefer transform and opacity.
- Avoid layout-shifting animation.
- Do not queue animations on repeated clicks.
- Do not delay navigation for flourish.

## Visual Direction

The quiz should feel like assembling a kit on a clean desk.

Good motifs:

- Slots
- Chips
- Loadout tray
- Pocket/pouch sections
- Gear category icons
- Compact product cards
- Checkmarks
- Small progress sparks

Avoid:

- Tactical HUDs
- Military/survival language
- Fake RPG stats
- Overly childish badges
- Casino-like rewards
- Loud confetti on every step

## Analytics Events

Track quiz behavior with event-level detail.

Events:

- `quiz_start`
- `quiz_step_view`
- `quiz_answer_select`
- `quiz_back`
- `quiz_complete`
- `quiz_result_view`
- `quiz_product_click`
- `quiz_related_guide_click`
- `quiz_restart`

Properties:

- step_id
- step_index
- answer_id
- carry_goal
- budget
- carry_style
- knife_preference
- result_setup_type
- estimated_kit_cost
- product_id
- product_category
- merchant

## Acceptance Criteria

The quiz is ready for MVP when:

- It can be completed in under 60 seconds.
- It has 6-8 steps, not a long form.
- Every answer gives visible feedback within 100ms.
- Progress/profile state is visible throughout.
- The final result is generated from deterministic rules, not freeform copy.
- Results include at least 5 recommended products or categories.
- TSA/no-knife conflicts are handled gracefully.
- All affiliate clicks are tracked.
- Reduced-motion users get a calm version.
- Mobile layout is fully usable one-handed.

## Claude Design Prompt

Use this prompt when asking Claude to design the quiz:

```text
Design the quiz/finder experience for Everyday Carry Finder.

The quiz should feel like a fun, tactile "Carry Builder," not a boring form. The user is building a practical everyday carry setup based on budget, lifestyle, pocket space, travel/work constraints, and preferences.

The brand is practical, trustworthy, modern, and non-tactical. It should not feel like a survivalist site, knife site, casino game, or childish RPG. Think clean gear desk, product cards, setup chips, compact loadout tray, and satisfying microinteractions.

Reference interaction patterns:
- Staged intake like MED-FINDER: short steps, visible progress, captured summary chips, animated result reveal.
- Rule-backed confidence like CarCheck: deterministic recommendation logic behind the playful UI.
- Arcade/dopamine motion: instant tap response, card pop, progress surge, captured chips, final kit reveal, reduced-motion support.

Quiz steps:
1. Carry goal: everyday basics, office/work, travel, minimalist pocket, keychain setup, emergency backup.
2. Budget: under $50, under $100, under $200, best value, premium but practical.
3. Carry style: front pocket, keychain, small pouch, bag/backpack, mix.
4. Knife preference: yes, maybe/optional, no knife, TSA-friendly only.
5. Style: clean/professional, minimal, rugged, tech-focused, low-profile.
6. Must-have categories: wallet, pen, flashlight, multitool, knife, charger/cable, pouch, key organizer, small medical/safety.
7. Pocket tolerance: barely anything, a few slim items, normal pockets fine, pouch/bag.
8. Result reveal.

Required UX:
- Each answer card should depress and pop on selection.
- The selected answer should become a captured chip in a "Your Carry" profile strip.
- Progress should feel like filling a loadout tray, not a generic bar.
- The result should reveal in stages: building kit, chips lock in, setup name, match confidence, estimated cost, product cards.
- Handle conflicts gracefully, such as TSA-friendly plus knife selected.
- Design mobile first and make it easy to complete one-handed.
- Include reduced-motion behavior.

Deliverables:
1. Quiz UX concept.
2. Mobile-first wireframe.
3. Desktop wireframe.
4. Step card component spec.
5. Carry profile chip spec.
6. Loadout progress component.
7. Result reveal sequence.
8. Product card layout.
9. Motion timing notes.
10. Empty/error/conflict states.
11. Analytics events to track.

Important:
Do not design this as a standard form. Design it as a fast, game-like decision tool that still feels credible enough for affiliate recommendations.
```
