# ELP screen captures → Figma

Captures of the 86 frames in `ELP Figma Export (ecd_connect).html`, rendered at 2x
(360×768+ logical px) and placed into the Final-design Figma file
(6gF4aWrKXg4MnUxhp3XCrU) as `ELP · <screen name>` frames, each with a
description card built from `elp-per-screen-descriptions.md`.

- `scr-NN.png` — screen NN in export order (see `shots-manifest.json` for names).
- `shots-manifest.json` — capture order, labels, sizes.
- `layout-plan.json` — flow sections, screen→description matching (12 screens
  in the export have no doc entry and carry "— description pending —" cards).
- `ids.json` — Figma node IDs for each screen's wrapper and frame.

`.github/workflows/figma-upload.yml` relays PNGs to Figma single-use upload
URLs (this environment cannot reach mcp.figma.com directly); to re-run, mint
fresh URLs via the Figma MCP `upload_assets` tool, write them to
`figma-screens/urls.tsv` (`<file>\t<url>` per line) and push.
