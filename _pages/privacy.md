---
layout: post
type: "docs"
title: "Privacy Policy — PR File Review Tracker for Bitbucket"
desc: "Privacy policy for the PR File Review Tracker for Bitbucket Chrome extension. No data collection, no tracking, no network requests."
description: "Privacy policy for the PR File Review Tracker for Bitbucket Chrome extension. No data collection, no tracking, no network requests."
date: 2026-05-18 12:00:00 +0100
permalink: /privacy/
---

# Privacy Policy — PR File Review Tracker for Bitbucket

_Last updated: 2026-05-18_

## Summary

This extension does not collect, transmit, sell, or share any personal information. Everything it stores stays on your own device, inside your own browser profile.

## What the extension stores

The extension uses `chrome.storage.local` (a browser-local key/value store) to remember which files you have personally marked as reviewed. For each pull request you interact with, one entry is written in the form:

```
prfilereview:<host>|<project>|<repo>|<prId>
  → { files: { "<path>": { at: <ms> } }, updatedAt: <ms> }
```

Where:

- `<host>` is the hostname of the Bitbucket Data Center site you granted access to.
- `<project>`, `<repo>`, `<prId>` come from the URL of the pull request you opened.
- `<path>` is the file path you marked as reviewed.
- `at` and `updatedAt` are local timestamps used for ordering and cleanup.

Entries that have not been updated in 30 days are automatically deleted.

## What is _not_ collected

- No analytics, telemetry, crash reporting, or usage tracking.
- No content of source files, diffs, comments, or any other PR data is read, copied, or transmitted.
- No personal identifiers — no email, name, account ID, or session tokens are read or stored.
- No data is sent to any server operated by the extension author or any third party. The extension makes no network requests.

## Permissions

- **`storage`** — used to persist the per-PR review state described above on your local device.
- **`activeTab`** + **`scripting`** — used only when you click the extension toolbar icon. The extension runs a one-shot check on the active tab to detect whether the page is Bitbucket (by reading three DOM markers) so it can show an "Enable on this site" button. No page content is exfiltrated or stored.
- **Host permissions** (`http://*/*`, `https://*/*`, optional) — requested per-origin at the moment you click "Enable on this site". Once granted, the content script runs only on URLs that match the pull-request path pattern for that origin. You can revoke the grant at any time from `chrome://extensions` → Details → Site access, or from the extension popup.

## Your control

- "Reset this PR" in the popup deletes the storage entry for the currently open PR.
- "Reset all PRs" deletes every entry the extension has ever written.
- "Disable on this site" revokes the host permission for the current origin. Your review state is preserved in case you re-enable later; use "Reset all PRs" first if you want to delete it.
- Uninstalling the extension causes Chrome to delete all `chrome.storage.local` entries belonging to it.

## Contact

Questions about this policy: open an issue on the project's source repository.
