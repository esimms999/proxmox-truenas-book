# Project memory: proxmox-truenas-book

## What this is

A Quarto book (`_quarto.yml`, chapters `01-*.qmd` … `12-*.qmd`, `index.qmd`) documenting how to run TrueNAS SCALE as a VM on Proxmox VE with an HBA passed through in IT mode, plus a parallel GPU passthrough setup on the same host. Render with `quarto render` (RStudio: **Render Book**); output goes to `_book/`.

## Source-of-truth priority

The user maintains a personal set of hardware notes/runbook text for their **own specific hardware**, separate from this book. When adding or reconciling content in this book:

- If the user's notes and general/vendor guidance conflict, **follow the user's notes** — they reflect what actually works on their hardware, not generic advice.
- Where the two differ meaningfully across vendors or configurations (not just "my box" vs. generic), prefer capturing **both** as vendor/config-specific guidance in the book (with a short rationale) rather than picking one silently. Example already applied: Resizable BAR is split into separate Intel and AMD rows in `02-bios.qmd` — enable on Intel when also passing a GPU, disable on AMD regardless — instead of one blanket rule.
- When unsure whether a discrepancy is "my hardware only" vs. general, ask before overwriting existing guidance.

## User's reference hardware

The user's notes describe this specific build (Intel platform):

- **Motherboard:** Gigabyte Z390 AORUS PRO WIFI-CF, AMI UEFI firmware, BIOS version F14a (06/12/2025).
- **CPU:** Intel Core i9-9900 @ 3.10GHz (8 cores / 16 threads).

Called out as a worked example in `02-bios.qmd`'s BIOS chapter. Since it's Intel, the AMD-specific rows/quirks in that chapter (SVM Mode path, forced-off Resizable BAR) don't apply to this build.
