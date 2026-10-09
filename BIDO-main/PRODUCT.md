# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

(Mobile-first PWA, installed to the home screen on Android and iOS and run full-screen offline. The interface is entirely in Arabic and right-to-left.)

## Users

- **Primary: أمين المخزن (the store keeper).** They log operations on a phone at the fish market at dawn: wet hands, bad light, often one-handed, high speed, and 50+ operations a day. Their job is to get every movement (sales, crates, drivers, ice) into the ledger correctly and without slowing the market down.
- **Secondary: صاحب العمل (the owner).** They read reports, check balances, and approve farm settlements (التصفيات). Confirmed: the owner comes second. The store keeper's logging speed sets the priority.

## Product Purpose

دفتر السماكة runs a commission fish-trading office in Egypt. The office sits between **farms** (they supply fish and are owed its value minus the office commission), **sale halls / traders (المبايع)** (they buy on credit and carry debt), **drivers** (they transport for a fee and may take advances), and **ice factories** (they supply ice blocks).

In this trade, numbers are a constant source of dispute. Success means every figure traces back to a dated movement, with no balance ever typed in by hand. Recording must also be fast enough that the store keeper actually logs everything as it happens.

## Positioning

An **append-only ledger with a hash chain** that lives on the device. Nothing is edited or deleted: corrections are new movements. The UI can feel like simple add/edit/delete while the data underneath stays auditable. Crates (البكش) are tracked with a double-entry, location-based ledger, and money is stored in integer piasters.

## Operating Context

- Logging happens in a wet, crowded market at dawn under poor light, often with one hand.
- No server and no account. Data lives in IndexedDB on the device. It works offline, with a backup every 50 movements and merge-restore from file.
- Reports are shared as formatted WhatsApp text and printed through `window.print()`.
- Main navigation (current): Home (needs-attention + 4 domains), Operations (accounts · crates · drivers · ice), Reports (20 reports behind 6 doors), Settings.
- Domains: الحسابات (accounts / farms / merchants), البكش (crates), السائقين (drivers), الثلج (ice).

## Capabilities and Constraints

- Owner PIN protects settlement, undo-beyond-window, edit, delete, stock count, restore, and final close. Periods can be locked. 20-second undo for the last movement on the same device.
- Single entity picker (`entPick`) for the whole app: if there are 24 entities or fewer, all show as buttons; above that, search plus the last 3 used.
- Input helpers: last 3 operations above each form, suggested crate counts (70, 84, plus most used), "save + another" keeps context, Arabic-Indic digits are normalized, voice entry for amounts, the error shows at the field, and haptics.
- Voided movements are hidden by default. The toggle lives only in memory.
- Version number is visible in the header on Home and Settings (diagnosis of cached versions).
- Built-in self-tests for `derive()` must keep passing. See HANDOVER.md §9.
- **Open for this redesign (not confirmed as binding):** single-file / no-build delivery, the existing color semantics (green in / red out, per-domain hues), and the dark-mode approach. The owner did not mark these as must-keep. Any change must still respect GitHub Pages hosting from a phone upload and offline PWA behavior.

## Brand Commitments

- Name: **دفتر السماكة**.
- **Typefaces are binding:** IBM Plex Sans Arabic for text, IBM Plex Mono for numbers (tabular), chosen for legibility in market light.
- Voice: Egyptian Arabic colloquial in UI copy ("دلوقتي", "واحدة تانية", "محتاج انتباهك").

## Evidence on Hand

- Real app: `index.html` (APPVER 4.28.0), `manifest.json`, `sw.js`, icons `icon-192.png`, `icon-512.png`, `maskable-512.png`.
- Detailed product and engineering record: `HANDOVER.md` (rules, decisions, past mistakes). `README.md` covers deployment.
- No testimonials, customer names, or usage metrics exist. Do not fabricate them.

## Product Principles

1. **Every number is traceable.** Show where a figure comes from. Never present an unexplained balance.
2. **Logging speed beats everything.** The fewest taps and the least thought for the 50+ daily entries made one-handed at dawn.
3. **Calm screens, loud exceptions.** Reduce density. What needs attention (negative stock, overdue debt, stale custody) must be impossible to miss.
4. **Reports answer a question first.** The key figure comes before the table, so the owner can trust the result at a glance.

## Accessibility & Inclusion

- Low-light and glare legibility. Arabic text never gets letter-spacing. Inputs are at least 16px (prevents iOS zoom). Touch targets are 44–52px for one-handed wet use.
- Fully RTL. Numbers use tabular alignment.
