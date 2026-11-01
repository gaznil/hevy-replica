# Product brief — requirements and proposed improvements

Updated 2026-11-01. Product for other people; Android and iPhone. Public repository. This captures the user's requirements and design recommendations; it is not an approved implementation specification.

## Confirmed requirements

1. Reproduce Hevy's workout features, familiar flows, and a premium interface closely; add the capabilities below. Build with original code and assets and a distinct identity before release.
2. Food photo input estimates calories, protein, and other supported nutrients.
3. A food-chat box also accepts descriptions and produces average estimates when photos or precise portions are unavailable. Photo scanning must never be the only way to log food.
4. Connect or display Instagram and other social identities on the app profile to appeal to fitness creators.
5. Explore nearby freelance trainer discovery, with distinct trainer and member panels/roles. Separate subscriptions or purchase plans are an undecided idea.
6. Mostly available free features; control excessive usage later. No prices or quotas chosen now.
7. Interface quality at least comparable to Hevy, with room to improve it.

## Recommended food experience

One food diary supports photo, natural-language chat, and manual search/entry. Voice and barcode input are candidates for a later spec, not already-approved functionality. All routes create the same structured meal record.

Example: "I ate two eggs, rice and chicken curry." Show food candidates and an estimate with portion assumptions. Offer a short clarification when it materially changes the result, plus a visible "use average portion" choice so logging need not stall. Let users edit quantity, cooking oil, sauces, preparation, and recipes, then confirm the saved entry.

The language/vision model proposes food identity and quantity; nutrient totals should come from identified food/recipe records and deterministic serving calculations. Retain source and portion assumptions. Calories, protein, carbohydrate, fat, fiber, and further nutrients can be shown only when supporting data exists. Missing information stays unknown rather than becoming zero or fabricated precision.

Save favorites and custom recipes, repeat previous meals, edit mistakes, and recalculate daily totals without duplicate entries. Offline users can record a description/manual entry and choose analysis later. Define provider cost and failure handling before enabling image analysis. Do not imply that all AI capabilities work offline.

Food, body measurements, and progress photos are private by default. Upload to an analysis provider only with the user's knowledge and control. Keep separate controls for assistant access, coach access, and public sharing. Proposed deletion and retention controls need implementation tests.

Research support: USDA FoodData Central exposes food search/details and nutrient data: https://fdc.nal.usda.gov/api-guide/ . Its coverage must be checked against target cuisines and recipes; it is not a guarantee that every local dish exists. MyFitnessPal's own scan flow asks users to select foods and adjust servings: https://support.myfitnesspal.com/hc/en-us/articles/360045761612-How-to-use-the-Meal-Scanner . This supports the correction-first interaction, not a claim about our future recognition accuracy.

## Recommended creator experience

Start with optional, user-editable social links and a profile that combines training identity, public routines, and selected achievements. Let users hide links and choose which progress is visible. Do not auto-publish food logs, body photos, or location to increase engagement.

Distinguish a user-provided link from an account whose ownership has been verified. Content sync, follower counts, and sign-in are separate integration decisions. Meta's Instagram API eligibility must be verified before promising them; the official documentation request was rate-limited during initial research. Public profile links do not require importing a user's audience or credentials.

Candidate improvement: public routine collections and optional creator attribution, with straightforward reporting and ownership controls. Creator monetization is deferred with the other commercial decisions.

## Recommended trainer experience

Begin with a directory and discovery/contact flow before building marketplace payments. Users choose an area or explicitly permit approximate location. Show whether a trainer works locally, remotely, or both; services, expertise, languages, availability/contact preferences, and actual credentials help people choose.

Use trainer and member roles in one product first, rather than separate apps. A trainer can manage their listing; a member can discover and request contact. Later accepted coaching relationships may expose plans and selected progress with explicit permission. A trainer cannot read another member's workout or food diary just by finding their profile.

Trust is a product requirement: verify credentials before a badge, separate identity verification from qualifications, establish the source of reviews, and include report/block controls. Do not populate fake trainers, invented reviews, or empty promises of certification. Define cancellation, refund, dispute, and abuse-handling rules before adding marketplace purchases.

No marketplace location, payment provider, commission, or trainer subscription is decided. Trainer pricing and platform pricing are separate future decisions.

## Recommended interface and free-plan approach

Keep workout logging fast, with large inputs and a clear active-session state. Nutrition, creator discovery, and coaching should not bury the workout controls. Offer users module visibility controls, accessible contrast/text, and clear privacy settings. Light/dark styling and detailed navigation need observed references and design review.

Protect core logging from future AI limits. When a future analysis allowance is exhausted, explain it before the request and retain manual entry and saved-data access. Determine limits from measured costs and usage after the product works; do not invent numerical caps now. No subscription or billing code is authorized merely by discussing this idea.

## Proposed order

Reliable workout core -> food diary with chat/photo/manual input -> broader progress and sync -> creator/social surfaces -> trainer discovery and coaching -> advanced integrations/wearables and release hardening. Existing parity requirements remain in the roadmap. Each phase gets its own Superpowers design, plan, and acceptance checks.

## Missing decisions to resolve at the right stage

- Approve the first workout slice and its position before nutrition.
- Choose the initial trainer market and supported cuisines/languages when designing those modules.
- Choose a product identity and visual direction before public distribution.
- Select providers, consent/retention design, and a sustainable free-plan policy before enabling chargeable functionality.

No release timeline or running-cost promise is established yet.
