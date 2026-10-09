---
name: دفتر السماكة (BIDO)
description: An offline Arabic RTL ledger for the fish trade, read like the fish hall's chalk price board.
colors:
  slate: "#111412"
  board: "#181C19"
  board-raised: "#212622"
  rule: "#2B312C"
  rule-strong: "#3B433D"
  chalk-ink: "#F1EFE6"
  chalk-ink-2: "#D2CFC3"
  chalk-muted: "#A4A296"
  chalk-faint: "#908E84"
  live: "#F4D35E"
  live-ink: "#F4D35E"
  live-bg: "#3A3318"
  on-live: "#17150A"
  credit: "#95D9AF"
  credit-bg: "#163020"
  debt: "#F59C92"
  debt-bg: "#3B1E1B"
  warn: "#F2A65A"
  warn-bg: "#3B2914"
  info: "#96CAEC"
  info-bg: "#172C39"
  stick-acct: "#80D6CB"
  stick-box: "#BDA9F5"
  stick-drv: "#EABF74"
  stick-ice: "#96CAEC"
  whatsapp: "#167B56"
  light-slate: "#ECEEE9"
  light-board: "#F9FAF7"
  light-board-raised: "#E3E6E0"
  light-rule: "#DCE0DA"
  light-rule-strong: "#C3C9C2"
  light-ink: "#161A17"
  light-ink-2: "#384039"
  light-muted: "#5B625C"
  light-faint: "#676E68"
  light-live: "#EDC63E"
  light-live-ink: "#7A5D00"
  light-live-bg: "#F6EBC3"
  light-credit: "#1A7543"
  light-debt: "#B0261E"
  light-warn: "#9C540A"
  light-info: "#1A5D8A"
typography:
  display:
    fontFamily: "IBM Plex Mono, SF Mono, ui-monospace, Menlo, Consolas, monospace"
    fontSize: "34px"
    fontWeight: 600
    lineHeight: 1.15
    letterSpacing: "normal"
    fontFeature: "\"tnum\" 1, \"lnum\" 1"
  headline:
    fontFamily: "IBM Plex Mono, SF Mono, ui-monospace, Menlo, Consolas, monospace"
    fontSize: "21px"
    fontWeight: 600
    lineHeight: 1.2
    letterSpacing: "normal"
    fontFeature: "\"tnum\" 1, \"lnum\" 1"
  title:
    fontFamily: "IBM Plex Sans Arabic, Segoe UI, Tahoma, system-ui, sans-serif"
    fontSize: "17px"
    fontWeight: 700
    lineHeight: 1.3
    letterSpacing: "0"
  body:
    fontFamily: "IBM Plex Sans Arabic, Segoe UI, Tahoma, system-ui, sans-serif"
    fontSize: "15px"
    fontWeight: 400
    lineHeight: 1.65
    letterSpacing: "0"
  body-sm:
    fontFamily: "IBM Plex Sans Arabic, Segoe UI, Tahoma, system-ui, sans-serif"
    fontSize: "13.5px"
    fontWeight: 400
    lineHeight: 1.6
    letterSpacing: "0"
  label:
    fontFamily: "IBM Plex Sans Arabic, Segoe UI, Tahoma, system-ui, sans-serif"
    fontSize: "12px"
    fontWeight: 600
    lineHeight: 1.4
    letterSpacing: "0"
rounded:
  pill: "20px"
  board: "10px"
  control: "8px"
  sheet: "16px"
  dialog: "14px"
  round: "50%"
spacing:
  s1: "4px"
  s2: "8px"
  s3: "12px"
  s4: "16px"
  s5: "20px"
  s6: "24px"
components:
  button-primary:
    backgroundColor: "{colors.live}"
    textColor: "{colors.on-live}"
    typography: "{typography.title}"
    rounded: "{rounded.control}"
    padding: "12px 16px"
    height: "52px"
  button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.chalk-ink}"
    rounded: "{rounded.control}"
    padding: "12px 16px"
    height: "52px"
  button-danger:
    backgroundColor: "{colors.debt-bg}"
    textColor: "{colors.debt}"
    rounded: "{rounded.control}"
    padding: "12px 16px"
    height: "52px"
  button-small:
    typography: "{typography.body-sm}"
    rounded: "{rounded.control}"
    padding: "8px 12px"
    height: "44px"
  input:
    backgroundColor: "{colors.slate}"
    textColor: "{colors.chalk-ink}"
    typography: "{typography.title}"
    rounded: "{rounded.control}"
    padding: "12px"
    height: "52px"
  pick-chip:
    backgroundColor: "{colors.slate}"
    textColor: "{colors.chalk-ink}"
    typography: "{typography.body}"
    rounded: "{rounded.control}"
    padding: "12px"
    height: "48px"
  pick-chip-selected:
    backgroundColor: "{colors.live}"
    textColor: "{colors.on-live}"
  filter-pill-selected:
    backgroundColor: "{colors.live-bg}"
    textColor: "{colors.live-ink}"
    rounded: "{rounded.pill}"
    padding: "8px 16px"
    height: "44px"
  board-row:
    textColor: "{colors.chalk-ink}"
    padding: "12px 0"
    height: "64px"
  pbal:
    backgroundColor: "{colors.board-raised}"
    textColor: "{colors.chalk-muted}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.control}"
    padding: "8px 12px"
  nav-tab-active:
    backgroundColor: "{colors.live-bg}"
    textColor: "{colors.live-ink}"
    height: "56px"
  fab:
    backgroundColor: "{colors.live}"
    textColor: "{colors.on-live}"
    rounded: "{rounded.round}"
    size: "60px"
  fab-with-form:
    backgroundColor: "{colors.board-raised}"
    textColor: "{colors.live-ink}"
    rounded: "{rounded.round}"
    size: "52px"
---

# Design System: دفتر السماكة (BIDO)

## Overview

**Creative North Star: "The Auction Slate"**

The ledger is the fish hall's price board. Figures are chalked large on green-black slate and read from arm's length at dawn, one-handed, with wet hands and a noisy floor. The keeper logs fifty-plus operations a day, so the system is dense and quiet: almost everything is chalk on slate, divided by hairline chalk rules, and colour appears only where it carries a fixed meaning.

The world refuses the category default of floating grey KPI cards with coloured side stripes. Balances sit in ruled rows, not boxes; today's totals sit in a ruled 2x2, not four tiles. One chalk-yellow plate per screen marks the thing to press or the answer to read. When a save changes a figure, that figure is re-chalked in place so the keeper sees which balance moved without hunting for it.

Dark slate is the ground and the default. Light ("فاتح") exists only as an explicit opt-in from Settings for office daytime use; it never follows the OS preference. Print is a separate white-paper, black-ink world.

**Key Characteristics:**
- Green-black slate ground, one step lighter board panels, warm chalk-white ink.
- Hairline-ruled rows instead of cards; no coloured side stripes anywhere.
- Chalk yellow owns every live state; one solid yellow plate per screen.
- Green = in / credit / له, red = out / debt / عليه, in every context.
- Domain identity is a single 8px chalk-stick dot, never a fill.
- Plex Mono numerals at board scale; Plex Sans Arabic for every word.
- Re-chalk: the signature motion that rewrites a changed figure in place.

## Colors

A near-monochrome chalk-on-slate palette where every hue is a fixed signal, not decoration.

### Primary
- **Chalk Yellow** (`live` / `live-ink`): the live state and nothing else: the primary button, the selected pick chip and quick number, the active bottom tab's pill, the FAB, the report's answer cell, the settlement total on the receipt tape, focus rings, caret and text selection. `live` is the fill; `live-ink` is the same yellow used as text, border and underline (in light mode it deepens to a dark ochre so it stays legible on paper). `on-live` is the near-black ink printed on a yellow plate.
- **Yellow Wash** (`live-bg`): the tinted, non-solid form of the live state: active tab pill, selected filter pill, selected report option, the just-saved row in "last 3", locked fields.

### Secondary (direction)
- **Chalk Green** (`credit`, `credit-bg`): money or crates coming in, a creditor balance, "له", a positive delta, the all-clear line.
- **Chalk Red** (`debt`, `debt-bg`): money or crates going out, a debtor balance, "عليه", a negative delta, errors, voids, the destructive button, the undo pill.

### Tertiary (signals)
- **Chalk Orange** (`warn`, `warn-bg`): drafts (an invoice without an amount) and attention (the attention count pill, warn-level attention rows) only.
- **Chalk Blue** (`info`, `info-bg`): neutral information only: "new" deltas and info-level attention rows.

### Domain sticks (dots only)
- **Accounts Teal** (`stick-acct`), **Crates Lilac** (`stick-box`), **Drivers Amber** (`stick-drv`), **Ice Blue** (`stick-ice`): each domain's chalk stick. They appear as the 8px dot beside a section title, board row, ops tab, header name, attention row or FAB menu entry.
- **WhatsApp Green** (`whatsapp`): the one third-party brand fill, on the share-to-WhatsApp button only, with white text.

### Neutral
- **Slate** (`slate`): the page ground, header, bottom nav, and input wells.
- **Board** (`board`): panels one step lighter: drill-downs, report cards, sheets, records.
- **Raised Board** (`board-raised`): a further step: the pbal line, open record header, table footers, the report answer row in the proof card, segmented active tab.
- **Chalk Rule** (`rule`) and **Strong Rule** (`rule-strong`): hairline dividers between rows, and control borders respectively.
- **Chalk Ink** (`chalk-ink`), **Second Ink** (`chalk-ink-2`), **Muted** (`chalk-muted`), **Faint** (`chalk-faint`): the four ink weights, from figures and names down to carets, dates and zero values.

### Named Rules
**The One Plate Rule.** A screen carries at most one solid chalk-yellow plate: the save button on a form screen, the answer figure on a report. When a form is open the FAB demotes itself to a yellow-ringed outline so it does not compete.

**The Fixed Direction Rule.** Green always means in / credit and red always means out / debt. They are never used for "good" or "bad" decoration, and orange is never a third direction.

**The Dot-Only Rule.** A domain hue is an 8px dot. It is never a fill, a border, a stripe, a tinted screen or a text colour.

**The Slate-First Rule.** Dark slate is the default (`color-scheme: dark`, theme colour `#111412`). Light is applied only through `html[data-mode=light]` when the user picks it in Settings; there is no `prefers-color-scheme` branch.

## Typography

**Text Font:** IBM Plex Sans Arabic (with Segoe UI, Tahoma, system-ui)
**Numeral Font:** IBM Plex Mono (with SF Mono, ui-monospace, Menlo, Consolas), tabular and lining, set LTR inside RTL text

**Character:** a sober humanist Arabic for every word, paired with a typewriter-straight mono that makes figures read like chalk on a price board and line up digit under digit.

### Hierarchy
The scale has exactly six steps (`--fs-xs` to `--fs-2xl`); nothing in the stylesheet or templates sits outside it.
- **Display** (Mono 600, 34px, 1.15): the big board figures: today's 2x2 totals, the report's answer figure, report tile values.
- **Headline** (Mono 600, 21px, 1.2): board-row balances, numeric inputs, handover cells, the receipt total, report names (in Sans 700).
- **Title** (Sans 700, 17px, 1.3): app name, sheet titles, primary buttons, text inputs (16px+ prevents iOS zoom), drill-down amounts in Mono.
- **Body** (Sans 400, 15px, 1.65): the base: table rows, row names, records, slim today strip figures.
- **Body Small** (Sans 400–700, 13.5px): secondary text, section titles, small buttons, filter pills, the pbal line.
- **Label** (Sans 600, 12px): table headers, tags, row sub-lines, helper lines, nav labels.

### Named Rules
**The Mono-for-Numerals Rule.** IBM Plex Mono sets digits, dates and counts only. An Arabic word is always in Plex Sans Arabic, even inside a numeric cell.

**The No-Tracking Rule.** Letter-spacing is 0 on body, inputs and buttons. Arabic is never tracked, never uppercased-by-style, never spaced out for emphasis.

## Layout

A single centred column (max 820px for content, 788px for the header row) on a 4px spacing scale (`s1` 4px through `s6` 24px; 28px is used only for the empty state and section-title top margin). Page gutter is 16px on phones and 24px from 640px up. The page reserves room at the bottom for the fixed nav (84px plus safe area).

The home first viewport is: compact sticky slate header (mark, name with domain dot, date, search), the today board, one attention line, then the balance board. Operation screens open with the slim today strip and the last three operations above the form. Forms keep a fixed field order for muscle memory.

Rows breathe at 12px vertical padding with a 64px minimum for board rows and 52px for drill rows; every tap target is at least 44px.

### Named Rules
**The Ruled Board Rule.** Groups of figures are separated by 1px chalk rules (`rule`), not by gaps between boxes. Multi-cell boards (today 2x2, handover grid, report gates, report summary) are one panel cut by 1px rules (`gap: 1px` over a `rule` background), never separate tiles.

**The Thumb Lane Rule.** On a form screen the save button sticks above the nav (72px plus safe area) and leaves a 64px lane on its inline-end side for the shrunken 52px FAB, which rides beside the save bar instead of over the fields.

## Elevation & Depth

The world is flat. Depth comes from three tonal steps (slate, board, raised board) and hairline rules. One soft shadow exists, and it belongs only to things that float above the page.

### Shadow Vocabulary
- **Float** (`box-shadow: 0 8px 24px -10px rgba(0,0,0,.7)`, light: `0 10px 26px -12px rgba(22,26,23,.45)`): the FAB, FAB menu entries, toasts, bottom sheets, and the sticky save bar.
- **Save-bar fade** (`box-shadow: 0 -8px 12px -4px var(--card)`): a board-coloured fade above the sticky save bar so fields scroll under it cleanly.
- **Scrim** (`rgba(5,7,6,.72)`, light `rgba(22,26,23,.5)`): behind sheets, dialogs and the open FAB menu.

### Named Rules
**The Border-or-Shadow Rule.** A resting surface gets a hairline border or nothing. Shadow is reserved for floating elements, and a floating element takes the shadow instead of a border.

## Shapes

Restrained, practical corners: 8px on controls (buttons, inputs, chips, pbal), 10px on board panels and grouped boards, 20px pills for tags, filter pills and counters, 16px top corners on bottom sheets, 14px on centred dialogs, full circles for the FAB and domain dots. Board rows, the today board and attention rows have no radius at all: they are ruled lines, not shapes. The receipt tape is the one deliberate exception: 4px corners with a scalloped tear edge top and bottom.

## Components

### Buttons
Heavy, flat plates sized for a thumb.
- **Shape:** gently rounded (8px), 52px minimum height, full width by default.
- **Primary:** the solid chalk-yellow plate, near-black 17px bold text. This is the screen's one plate.
- **Pressed:** scales to .98 and dims (brightness .92) over 120ms. Disabled drops to 45% opacity.
- **Ghost / Dark:** transparent or raised-board fill with a strong-rule border, chalk ink.
- **Danger:** red wash with red text and red border.
- **Small:** 44px high, 13.5px text, auto width.

### Chips and pills
- **Pick chips:** an equal-width grid of 48px slate wells with strong-rule borders; the chosen entity becomes a solid yellow plate with bold near-black text. Long names truncate with an ellipsis.
- **Filter pills and inner tabs:** 20px pills, muted text with strong-rule border; selected becomes yellow wash with yellow ink and border.
- **Quick numbers:** Mono pills under a numeric field; selected is the solid yellow plate.
- **Tags:** 12px semibold pills on raised board; red wash for void and damage, orange wash for drafts.

### Board rows (signature)
The home balance board: each balance is a full-width ruled row, name and 8px domain dot on the start side, the figure in 21px Mono on the end side, a faint caret. No background, no radius, 1px rule below. Expanding a row turns its name and caret chalk-yellow and opens a board-coloured drill list beneath with no border of its own. The custody row adds a two-column split of small figures.

### Today board and slim strip
Home opens with a ruled 2x2 of sales, collections, crates out and crates in at 34px Mono, labels in 12px muted beneath, cut by one vertical and one horizontal rule. An unpriced invoice adds an orange draft marker beside the sales figure. On operation screens it collapses to the slim strip: one row of four cells at 15px, no header, separated by vertical rules.

### Attention line
A single ruled line ("محتاج انتباهك") with an orange count pill (red when any item is serious). Expanded rows carry an 8px dot by severity: orange warn, red bad, blue info. When nothing needs attention, a single green-dotted "all clear" line replaces it.

### pbal (picked entity's balance)
As soon as an entity is picked in a form, a raised-board 8px-radius line appears beneath the picker showing its live balances in Mono (red for owed out, green for owed in). It is `aria-live=polite` and its figures take part in re-chalk.

### Inputs / Fields
- **Style:** slate wells with a 1px strong-rule border, 8px radius, 52px tall, 17px text; numeric fields use 21px Mono semibold, right-aligned.
- **Focus:** 2px chalk-yellow outline and yellow border; the caret is yellow.
- **Error:** red border on a red wash, label turns red; a picker in error gets a red 2px outline offset 5px.
- **Locked:** yellow wash with a dashed border.

### Navigation
A fixed slate bottom bar with a top rule, up to 200px per tab, 56px tall. Tabs are a 22px line icon over a 12px label in muted ink; the active tab turns chalk-ink bold and its icon sits in a 56x30 yellow-wash pill with yellow ink. Segmented controls on board panels mark the active segment with raised board plus a 2px yellow underline; the ops segmented control prefixes each tab with its domain dot (55% opacity when inactive).

### FAB
A 60px chalk-yellow disc at the inline-end, 88px above the bottom, carrying the float shadow; it rotates 45 degrees to open a staggered menu of pill entries, each with a domain-coloured icon in a raised-board disc. On a form screen it shrinks to 52px, drops to the thumb lane beside the save bar, and turns into a raised-board disc with a 1.5px yellow ring (The One Plate Rule).

### Receipt tape
The settlement receipt: a board panel with scalloped tear edges, dotted leaders between label and Mono value, a rule before the totals, and the net settlement printed on the solid yellow plate.

### Re-chalk (signature motion)
Any figure marked `data-fig` whose text changed since it was last drawn is rewritten in place: a 700ms left-to-right clip reveal (from 20% opacity and 1.5px blur to sharp) on the expo-out curve `cubic-bezier(.16,1,.3,1)`, with a 2px chalk-yellow underline offset 6px that fades out over 800ms after 1.6s. The first render of a session never animates. Under `prefers-reduced-motion: reduce` every animation and transition is removed and the figure simply updates.

## Do's and Don'ts

### Do:
- **Do** build every group of figures as ruled rows or a 1px-ruled board on slate.
- **Do** give each screen exactly one solid chalk-yellow plate: the save button, or the report's answer figure.
- **Do** colour a figure green for in / credit and red for out / debt, everywhere, and nothing else.
- **Do** mark a domain with one 8px chalk-stick dot beside its name.
- **Do** set every digit in IBM Plex Mono with tabular, lining numerals, LTR inside the RTL line.
- **Do** keep type on the six-step scale (12, 13.5, 15, 17, 21, 34px) and spacing on the 4px scale.
- **Do** add `data-fig` to any figure a save can change so it re-chalks.
- **Do** keep tap targets at 44px or more, and form rows at 52px.

### Don't:
- **Don't** use floating grey KPI cards or coloured side stripes on rows, cards or alerts.
- **Don't** fill, border, stripe or tint anything with a domain hue; it is a dot.
- **Don't** use orange (`warn`) as a direction colour or as decoration; it is for drafts and attention.
- **Don't** put Arabic words in IBM Plex Mono, or apply letter-spacing to Arabic.
- **Don't** give a resting surface both a border and a shadow; shadow is for floating elements.
- **Don't** make light mode follow the OS; slate is the default and light is an explicit choice.
- **Don't** animate figures on first render or without a reduced-motion fallback.
