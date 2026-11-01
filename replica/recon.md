# Initial recon: Hevy, Android and iPhone

Date: 2026-11-01. For: an independent product for other people. Scope: comprehensive parity roadmap, with the workout core proposed as the first implementation slice.

**Evidence level:** public official documentation only. No installed mobile app, authenticated account, binary, network capture, or runtime trace has been examined. This is a preliminary map, not completed reconnaissance.

## Sources

| ID | Official source | URL | Use |
| --- | --- | --- | --- |
| H01 | Hevy feature guide | https://help.hevyapp.com/hc/en-us/articles/33106320824727-Everything-You-Need-to-Know-About-the-Hevy-App-2026-Features-Guide | Documented capabilities and platforms |
| H02 | Feature list | https://www.hevyapp.com/features/ | Areas to inventory |
| H03 | Social guide | https://www.hevyapp.com/features/social-features/ | Feed and sharing behavior |
| H04 | MCP guide | https://www.hevyapp.com/hevy-mcp/ | Existing assistant capabilities and consent |
| H05 | October 2026 update | https://www.hevyapp.com/community-updates/october-26/ | Notes and current assistant integration changes |
| H06 | Offline comparison | https://www.hevyapp.com/compare/fitbod/ | Hevy's documented offline behavior |
| H07 | Home/product overview | https://www.hevyapp.com/ | Workout, watch, and web scope |
| H08 | Coach connection | https://www.hevyapp.com/features/strength-coach/ | Assigned plans, communication, and shared progress |
| C01 | Liftosaur overview | https://www.liftosaur.com/blog/posts/liftosaur-overview/ | Candidate progression/programming extension research |

Each feature row links its source directly. Official documentation establishes a feature claim, not the implementation or every screen state. Provider announcements are time-sensitive and must be refreshed before integration work.

## Core loop

Plan a routine -> log the workout -> review progress -> repeat. Community sharing surrounds this loop.

## Provisional screen inventory

These are candidate functional surfaces inferred from documentation. Routes, layouts, screen boundaries, tap counts, and empty/loading/error states have not been observed in either phone app.

| ID | Surface | Purpose | Evidence | States observed |
| --- | --- | --- | --- | --- |
| S01 | Workout/routine area | Select or create a routine | H01, H02 | None in runtime |
| S02 | Routine editor | Configure exercises and sets | H01 | None in runtime |
| S03 | Exercise selection/details | Find movements and guidance | H01 | None in runtime |
| S04 | Active workout | Record sets and notes; timer | H01 | None in runtime |
| S05 | Workout summary/history | Save and revisit sessions | H01, H07 | None in runtime |
| S06 | Exercise progress | Inspect trends and records | H01 | None in runtime |
| S07 | Measurements | Record body measurements | H01 | None in runtime |
| S08 | Feed/profile | Social workout discovery | H03 | None in runtime |
| S09 | Trainer/program | Guided programming | H01 | None in runtime |
| S10 | Integrations/preferences | Manage connections and settings | H04, H05 | None in runtime |

This is a provisional set of ten surfaces, not a count of Hevy's real screens.

## Flows to observe

- F01: routine selection/editor -> active workout -> finished workout -> history.
- F02: exercise detail -> previous performance -> new set -> progress review.
- F03: feed/profile -> workout detail -> interaction or routine save.
- F04: explicit assistant connection -> read training information -> preview/update routine -> revoke access.

These four candidate flows have no measured tap counts or captured mobile edge states yet.

## Candidate components and records

Likely components: exercise row, set table, set-type control, timer, notes, routine card, chart, calendar, profile/feed card, consent control. Exact variants and states await observation.

Inferred records: User, Exercise, Routine, RoutineExercise, Workout, WorkoutExercise, Set, Measurement, Connection. These are our proposed entities, not recovered Hevy database tables. Routine and workout distinction follows the documented reusable-routine behavior; fields and relationships still need design.

## Coverage and unknowns

See `features.csv`. All implementation entries start at `no`; no parity score is claimed. Baseline rows use documented evidence. Candidate additions have `original=unknown`; do not market them as missing from Hevy without more research.

Exercise demonstration media must be independently produced or licensed. Existing community users/content, private endpoints, branding, and partner entitlements are not transferable. App Store listings, actual phone screens, accessibility states, import formats, settings, and integration constraints still need investigation.

## Size and next step

The complete request is XL: separate phone UX, durable/offline data, sync/backend, analytics, social, and hardware/provider integrations. No delivery date is established. The three main engineering uncertainties are reliable offline sync, cross-platform/watch behavior, and privacy/authorization across social and assistant integrations.

Next: approve the first slice, complete its phone evidence, then run Replica architecture/design and the Superpowers specification/plan workflow. REA is reserved for a concrete authorized runtime question; public docs have not been re-labeled as REA findings.
