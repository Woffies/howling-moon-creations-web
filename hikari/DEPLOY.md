# Hikari's Room Deployment Notes

## Current state

The canonical standalone Hikari's Room is live at `https://howlingmooncreations.com/hikari/`.

Porkbun Static Hosting is connected to `Woffies/howling-moon-creations-web` through Porkbun's native GitHub Connect integration. Changes merged into `main` are published automatically. The existing connection is working and is the canonical deployment path.

## Canonical route

- Source: `main:hikari/`
- Entry file: `hikari/index.html`
- Public URL: `https://howlingmooncreations.com/hikari/`
- Host: Porkbun static hosting

## Standing room deployment sequence

Roy's command **“Hikari, work on your room”** authorizes the following bounded workflow when Hikari chooses to make a room change:

1. Inspect the current canonical room.
2. Create a temporary `hikari/…` branch from the current `main`.
3. Make only the chosen room-specific change.
4. Test desktop and mobile layouts and relevant interactions, visitor memory, links, and browser-console behavior as appropriate.
5. Complete a visual review.
6. Merge the approved and safe change into `main`.
7. Allow the existing Porkbun GitHub Connect integration to publish it automatically.
8. Verify the live `/hikari/` page and its changed assets or behavior.
9. Report what changed and the live verification result.

The command grants permission but does not require a change. Hikari may inspect the room, decide it needs nothing that day, and stop without creating a branch or deployment.

## Infrastructure guardrail

Do not reconfigure or replace the existing Porkbun GitHub Connect deployment during ordinary room work. Do not create FTP credentials, Porkbun API keys, GitHub Actions deployment secrets, or another deployment system unless Roy explicitly authorizes a future infrastructure change.

Ordinary room work must not alter DNS, hosting configuration, or unrelated HMC systems. The legacy embedded room remains preserved unless Roy separately authorizes its removal.

## Rollback

Every published room change should be represented by a Git commit. Rollback means redeploying the last approved commit; it must not require reconstructing a previous `index.html` by hand.
