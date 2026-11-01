# Proposed first release — awaiting approval

Date: 2026-11-01. Audience: other people. Platforms: Android and iPhone.

This is a discussion proposal, not an approved specification or permission to implement. Full Hevy parity and selected extensions remain the overall roadmap.

The confirmed broader product includes a single food diary with chat, photo and manual input, creator social profiles, nearby trainer discovery, generous free access, and a premium interface. See `docs/product-brief.md`. Nutrition follows the reliable workout core as its own spec; this proposal does not drop those requirements.

## Approaches

1. **Recommended: a reliable workout core first, then parity phases.** A shared phone application, local workout storage, and a later independent synchronization service. Produce something that can complete real workouts before adding social, assistants, and wearable companions. Exact libraries and versions will be chosen from current official documentation during planning.
2. **UI demonstration first.** Faster to compare screens, but it cannot validate workout reliability, synchronization, or a product other people can use. Not recommended as the main milestone.
3. **All subsystems together.** Delays a useful release and ties workout logging to social, cloud, wearables, and AI. Not recommended for the initial slice.

## Proposed first slice

Preserve Hevy's familiar workout flow: select or make a routine, add exercises, enter sets/reps/weight, mark a set complete, use the rest timer, finish the workout, and inspect saved history and basic progress. Use original code and assets. Detailed layout specifications require observed phone references; they are not invented here.

Core units: routine editor, exercise selector, live workout session, timer, history, basic exercise progress, preferences, and local persistence. Sessions and routines are independent data records; a finished workout preserves what actually happened rather than changing when a routine is edited later.

Workout data must survive normal app restarts and an interrupted session. Timer state is based on a stored end time so backgrounding the app does not depend on continuous JavaScript execution. Users control kg/lb preferences and optional sounds or notifications. Notification permission denial must not block logging.

For the initial slice, data stays on the device. Account synchronization, public profiles, feeds, third-party connections, wearables, paid services, and AI are later phases. Their deferral does not count as parity.

## Acceptance checks

- On both phones: make a routine, start it, edit and complete sets, finish, and see the saved workout after reopening.
- Begin a workout offline, close the app, reopen, and recover the in-progress session without silently losing recorded sets.
- Changing a routine does not rewrite historical workout records.
- Weight/unit conversion and workout totals have deterministic tests and clear display rounding.
- Rest timer recovers correctly after backgrounding; denied notifications leave an on-screen timer available.
- Empty and invalid inputs have usable states; saving cannot create duplicate completed workouts on repeated taps.
- Basic progress reflects recorded workouts and does not invent training results.
- No claim of tested iPhone/Android behavior without a corresponding simulator/device check and evidence.

## Decisions still needed before a complete implementation specification

- Product approval of this first slice.
- Target app version and phone references for close UI comparison.
- Product name and identity before distribution.

The exact technical design and test commands follow in the implementation plan after design approval.
