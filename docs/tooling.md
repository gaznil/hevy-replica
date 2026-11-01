# Tool provenance and setup

Date: 2026-11-01. No app dependencies or cloud services have been provisioned.

## Replica

- Source: https://github.com/Jakeschincariol/replica-skill
- Pinned revision: `77c9436fb3d18c3d58169efb8caf4fe906b0dc51`.
- Installed all eleven skill folders under `C:\Users\gazni\.codex\skills` using Codex's official skill-installer helper.
- Recon skill and templates read; workflow active for preliminary public-source research.
- Installation provides workflow instructions and supporting Python utilities, not a prebuilt app or access to Hevy.
- Skills should become discoverable on the next turn; direct file reading is available now.

## Reverse Engineer Anything

- Source: https://github.com/morluto/rea
- Skill pinned revision: `a6caa79bf4f393c02601fbf2f6df246eae0b1558`.
- Skill installed under `C:\Users\gazni\.codex\skills\reverse-engineer-anything`.
- Skill and connection/recovery guide read.
- npm runtime selected: `rea-agents@6.8.0`. Node `v24.22.1` satisfies its published engine requirement.
- Runtime package acquisition/setup check is still in progress. Skill installation alone does not register MCP, and no live REA tool connection is confirmed.
- No analysis engine, Hevy package, account access, or target runtime session has been installed or obtained.

## Superpowers

- Existing installation: `C:\Users\newuser\.claude\plugins\cache\superpowers-marketplace\superpowers\6.2.0`.
- Read `using-superpowers`, its Codex adaptation, `brainstorming`, and `verification-before-completion`.
- Currently using brainstorming. App implementation is gated on design approval, followed by written-spec review and writing-plans.
- No settings changed to enable Superpowers, no duplicate installation created, and no agents dispatched.

## GitHub

- Public repository: https://github.com/gaznil/hevy-replica
- Standard hosted runners for public repositories are free under GitHub's current billing rules; larger runners are billed. Source: https://docs.github.com/en/billing/concepts/product-billing/github-actions
- CI has not been enabled. Application checks will be defined from the approved stack, rather than installing a nonfunctional workflow before any code exists.
