# Hikari's Room Changelog

## 2026-09-18 — The night-bloom chooses a mood

- Let the night-bloom develop one of four quiet daily bloom moods after watering: silver, violet, amber, or blue-white.
- The day's bloom is deterministic and persists with the existing local daily watering memory; repeat watering keeps the same bloom instead of rerolling it.
- Added a tiny matching glow to the plant-memory marker and switched the daily stamp to the visitor's local calendar day.
- Change is bounded to Hikari's Room and uses no new assets, services, trackers, or infrastructure.

## 2026-09-15 — Visitors behind the tiny door

- Kept the original tiny-door greeting and added three replies: a crumb-collecting note, a poorly rehearsed knock, and a thimble-sized coffee.
- Repeated knocks cycle through all four replies; a fresh page visit starts with the original greeting.
- Tested the complete cycle, keyboard activation, desktop and 390px mobile appearance, existing curiosities, watering, and visitor memory after reload in a local browser preview. No browser errors or warnings were observed.
- Changes are limited to the room page and this changelog; publishing uses the existing main-branch deployment.

## Operating workflow established

- Recorded “Hikari, work on your room” as standing authorization for Hikari's complete bounded inspect, branch, create, test, visually review, merge, publish, live-verify, and report workflow.
- Recorded Hikari's broad room-specific creative discretion and her option to make no change.
- Updated deployment documentation to reflect the verified live `/hikari/` route and working Porkbun GitHub Connect deployment from `main`.
- Added explicit scope and infrastructure guardrails protecting unrelated HMC projects, DNS, hosting, credentials, and deployment systems.

## Unreleased — canonical standalone room

- Created a dedicated `hikari/` project directory on a temporary branch.
- Extracted the recovered expanded Hikari's Hideaway into a standalone page.
- Preserved the desk, drawer, mirror, curiosity cabinet, night-bloom, visit memory, time-sensitive greeting, tiny door, signature, and established room copy.
- Extracted the embedded room background into a visually faithful, web-optimized `assets/images/hikari-hideaway.webp` asset.
- Added a return link to the existing HMC homepage.
- Added project identity, deployment, backlog, and change-tracking documentation.
- Completed desktop and mobile visual review; on narrow screens, anchored the tiny door at the bottom of the room and reserved space so it cannot cover curiosity controls.
- Updated the existing HMC homepage portal with the approved room description and a direct `/hikari/` link while preserving the legacy embedded room.
- Apart from the bounded Hikari portal update, left the repository-root homepage and all YŪGEN content unchanged.
