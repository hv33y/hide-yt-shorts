# Hide YouTube Shorts + Block Ads (uBlock Origin Lite Filter)

> Updated 2026 fork of [gijsdev/ublock-hide-yt-shorts](https://github.com/gijsdev/ublock-hide-yt-shorts) — now with YouTube ad-blocking and anti-adblock bypass.

This filter list does two things:
1.  **Hides all Shorts** - shelf, sidebar, bottom nav, channel tabs, search, chips
2.  **Blocks YouTube ads** - pre-roll, mid-roll, overlay, feed ads, masthead, and the "Ad blockers are not allowed" popup

### Install (uBlock Origin)

**URL install (recommended):**
1. Copy raw URL to your `list.txt`:
```
https://raw.githubusercontent.com/hv33y/hide-yt-shorts/refs/heads/master/list.txt
```
2. uBlock Origin Dashboard > Filter lists > scroll down > Import > paste URL > Apply

**Manual:**
1. Dashboard > My filters > paste contents of `list.txt` > Apply

### Important: Firefox vs Chrome

Chrome removed full uBlock Origin in Aug 2026 (Manifest V3). Use **Firefox** for 100% blocking. On Chrome, use uBlock Origin Lite + this list, but some video ads may leak.

### What this fixes vs old list

- Old list used `ytd-reel-shelf-renderer` only. YouTube now uses `ytm-shorts-lockup-view-model-v2` and `grid-shelf-view-model` - added.
- Added mobile `m.youtube.com` coverage.
- Added ad selectors: `ytd-ad-slot-renderer`, `ytd-in-feed-ad-layout-renderer`, `ytp-ad-module`, etc.
- Added scriptlet bypass: `yt.config_.args.ad3_module`, `ytInitialPlayerResponse.adPlacements`

### Auto-Update

This repo auto-updates the `! Version` and `! Last modified` headers every 3 days via GitHub Actions, so uBlock Origin sees a new version and re-fetches. Workflow file: `.github/workflows/auto-update.yml`

### Contribute

PRs welcome! If YouTube changes layout and Shorts re-appear, open an issue with a screenshot and your browser.

### License

[MIT](LICENSE) - see LICENSE.md
