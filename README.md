# Fitness tracker for Android and iOS

An independent fitness app, using Hevy as the reference for feature coverage and workout flows, with original code and branding. Working project name: `hevy-replica`.

**Stage:** research and design. No app implementation or deployable release exists yet.

The aim is comprehensive feature parity, followed by useful, optional extensions. This is a roadmap, not a claim that an entire established product can be recreated in one build.

## Project documents

- [Current status and operating rules](STATUS.md) — the canonical project record.
- [Roadmap](ROADMAP.md) — delivery sequence and completion criteria.
- [Product brief](docs/product-brief.md) — requested additions and improvements to review.
- [Research](replica/recon.md) and [feature matrix](replica/features.csv) — evidence, unknowns, and coverage.
- [Proposed first release](docs/superpowers/specs/2026-11-01-first-release-proposal.md) — draft awaiting product approval.
- [Superpowers workflow checklist](docs/superpowers/checklist.md).
- [Tool provenance and setup](docs/tooling.md).

## Development approach

Use Superpowers for design, planning, testing, and verification; Replica for feature mapping and comparison; REA for focused runtime investigation when suitable evidence is available. Public documentation is the current evidence source. Installed tools do not establish access to Hevy's internal implementation.

Public GitHub repository. Use standard GitHub-hosted runners for future CI. Deployment, cloud services, mobile distribution, and paid services require a separate decision.

This project is independent of Hevy. Reference screenshots and third-party exercise media are not app assets.
