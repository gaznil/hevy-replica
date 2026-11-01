# Delivery roadmap

This sequence is proposed. The destination is comprehensive Hevy feature coverage plus selected improvements, not a single-session clone. App code starts after the first design is approved.

| Phase | Outcome | Evidence required to finish |
| --- | --- | --- |
| 0. Research and design | Source-linked coverage matrix, phone screen/flow inventory, approved first slice | Unknowns labeled; product design approved; implementation plan reviewed |
| 1. Core workout loop | Routines, exercises, set logging, rest timer, saved workout history, basic progress, offline recovery on both phones | Create routine -> log sets -> finish -> reopen; data persists; interrupted workout recovers; kg/lb and timer checks; device verification on both platforms |
| 1b. Nutrition | One food diary with chat, photo and manual input; editable calories/macronutrients and supported nutrient estimates | Portion/recipe assumptions shown; corrections recompute totals; unknowns are not zero; retry cannot duplicate meals; private-by-default media and diary |
| 2. Progress and programming | Remaining analytics, personal records, measurements, routine organization, programming tools | Recorded calculations and trend fixtures; accessible charts; source-linked feature coverage |
| 3. Accounts and sync | Account control, backup, multi-device synchronization, data export/import | Offline conflict and duplicate-write tests; ownership checks; restore and deletion checks |
| 4. Social | Profiles, feed, following, workout/routine sharing, interactions | Privacy and block/report flows; ownership/access checks; real end-to-end interaction tests |
| 4b. Creator identity | Optional Instagram/social links and creator profile surfaces | User controls visibility and removal; no assumed API access or imported audiences |
| 4c. Trainer discovery | Search a chosen area; trainer/member experiences; contact and service discovery | Approximate location; real credential checks before badges; reporting and private-data consent; business model approved before payments |
| 5. Integrations and wearables | Opt-in API/MCP, approved health/Strava integrations, Apple Watch/Wear OS companion scope | Consent, revocation, scoped access, device/provider tests; no claimed compatibility without evidence |
| 6. Extensions | Highest-value validated gaps, individually optional | Gap evidence and demand recorded; acceptance checks; user-controlled enable/disable |
| 7. Release | Own identity, distribution, reliability, operating costs | Parity report, security/privacy review, signed phone builds and explicit release authorization |

Web parity and the exact boundaries of Hevy Trainer/Coach need separate scope decisions. They remain documented requirements to assess, not silently completed or discarded features.

## Requested additions

See `docs/product-brief.md` for the user's food photo AND chat requirement, creator profiles, nearby trainer discovery, generous free plan, premium UX, and the proposed improvements. The nutrition, creator, and trainer phases are separate specs because they have independent data, trust, and integration requirements.

## Further candidate improvements to investigate

- User-defined progression rules and editable multi-week program blocks, inspired by Liftosaur's documented approach.
- Granular assistant permissions and preview/confirmation of AI-generated changes.
- Portable backups and an optional self-hosted data service.
- Calendar-based program scheduling, equipment-aware substitutions, and interval/mobility tracking; avoid expanding the initial slice before evidence and demand.

These are proposals. None is currently proven absent from Hevy, technically validated for this product, or approved for implementation. AI providers, connected services, and hosting may have costs; evaluate them before enabling them.
