# Hikari's Room Deployment Notes

## Current state

This directory is staged on a temporary branch only. It must not be merged or deployed without Roy's approval.

The existing live homepage continues to serve the embedded Hikari's Hideaway from the repository-root `index.html`. That implementation remains untouched during this extraction.

## Intended route

- Source: `main:hikari/`
- Entry file: `hikari/index.html`
- Intended public URL: `https://howlingmooncreations.com/hikari/`
- Host: Porkbun static hosting

## Approval-gated deployment sequence

1. Review the temporary branch and local test results.
2. Obtain Roy's explicit approval to merge.
3. Merge the approved branch into `main` without removing the embedded root implementation.
4. Upload or automatically synchronize the repository tree to Porkbun's static document root.
5. Verify `/hikari/` returns HTTP 200 and loads its background asset.
6. Test all interactions, local memory, the return link, mobile layout, and browser console on the live URL.
7. Only in a later, separately approved change should the homepage portal be pointed at `/hikari/` and the old embedded implementation considered for removal.

## Connection still required

GitHub write authorization is available. Porkbun publishing is not yet automated or exposed to the project. A secure repository-to-Porkbun deployment route must be established before “work on your room” can include publishing without manual uploads.

Credentials must never be committed to this repository. Deployment secrets belong in the approved deployment system's encrypted secret store.

## Rollback

Every published room change should be represented by a Git commit. Rollback means redeploying the last approved commit; it must not require reconstructing a previous `index.html` by hand.
