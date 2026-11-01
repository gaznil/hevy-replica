# WHAT THIS IS

A fitness app for both Android and iPhone, intended for other people to use. User requests: reproduce Hevy's features and experience closely, add useful capabilities including MCP where appropriate, use REA and Replica, create a public repository, and follow Superpowers before implementation.

# STATUS

2026-11-01, Asia/Calcutta. Project setup and initial public-source research underway. No application code, production service, account integration, or mobile build exists.

Confirmed: both phone platforms; product for other people; public repository to avoid drawing standard public CI from the private-repository minutes allowance. Requested extras: food-photo nutrition estimates AND a chat box for describing food with average estimates when needed; linked Instagram/social profiles for creators; nearby freelance trainer discovery with distinct trainer/member experiences; mostly available free features with usage limits and pricing deferred; premium interface matching or improving the Hevy experience. Trainer subscriptions and business model remain raw ideas, not settled requirements.

Superpowers brainstorming is active. The proposed first-release design is not approved. Full feature parity remains the overall ambition; a first release does not replace that scope.

# WHERE THINGS LIVE

- Project folder: `C:\Gaznil\builds\hevy-replica`.
- GitHub: https://github.com/gaznil/hevy-replica (public).
- This file is the canonical status. Do not create another task board or project-memory copy.
- Research: `replica/recon.md`, `replica/features.csv`.
- Roadmap: `ROADMAP.md`.
- Product brief: `docs/product-brief.md`. Design proposal and workflow: `docs/superpowers/`.
- Tools and exact revisions: `docs/tooling.md`.

# RULES

- Use Superpowers brainstorming before implementation, then writing-plans, meaningful tests, review, and verification.
- Use Replica's recon -> architecture -> design -> build -> backend -> test -> diff sequence as relevant.
- Original implementation and own product identity. Keep references outside shipped assets.
- Only claim features, screen states, compatibility, tests, and parity supported by recorded evidence.
- REA is available for focused investigation; no binary analysis or account access has been performed. Do not imply that installing REA reproduced Hevy.
- Optional AI/MCP access must be controlled by each user: explicit connection, limited permissions, confirmation of writes, and revocation. No automatic sharing of workout data.
- Nutrition estimates are editable and explicitly approximate. Show assumptions for portions/ingredients; nutrient values without supporting data remain unknown. Allow manual/text entry when photos or network analysis are unavailable. Food logs stay private unless individually shared.
- Social links are optional. Do not promise Instagram account verification, follower imports, or content synchronization without confirmed official API eligibility and review.
- Trainer discovery must allow a manually selected area. Do not publish precise user/home coordinates. Trainer/member roles and consent govern shared progress; credentials need verification before a verified badge is shown.
- Pricing, numerical quotas, trainer commissions/subscriptions, and paid AI providers are deferred decisions. Do not hardcode them from guesses.
- Public repository: no credentials, tokens, personal workout exports, account recordings, or unlicensed media in commits.
- User authorized project setup, tool installation, and creation of this public repository. Deployments, paid resources, production writes, destructive operations, and later pushes require the user's exact authorization unless explicitly covered by the current request.
- Prefer standard public Linux runners for CI. No CI has been enabled yet; larger runners and external build services are separate cost decisions.
- Keep product-owner updates concise. Ask about product choices or necessary physical steps, one next action at a time.

# GOTCHAS

- Hevy already offers offline logging, an adaptive Trainer, and MCP/ChatGPT integration. These are baseline features, not verified differentiators.
- Public documentation is not a complete screen-by-screen inventory. Installed iOS/Android versions and unobserved states remain unverified.
- Hevy's community, existing users, proprietary media, and commercial integrations do not transfer to a new app.
- Full parity spans phone apps, backend/sync, social, analytics, integrations, and wearables. Each needs its own accepted scope and passing checks.
- A public GitHub repository does not automatically grant a license or make third-party build, hosting, AI, or store services free.

# QUEUE

1. Finish and verify tool setup; record exact status in `docs/tooling.md`.
2. Review the consolidated product brief and approve the proposed first product slice before implementation.
3. Complete mobile screen/flow evidence and feature inventory without claiming unseen states.
4. Write and review the approved design, then create a detailed Superpowers implementation plan.
5. Implement and verify the core workout loop on Android and iPhone.
6. Work through parity plus the requested nutrition, creator, and trainer modules; verify candidate extras before describing them as missing from Hevy.
