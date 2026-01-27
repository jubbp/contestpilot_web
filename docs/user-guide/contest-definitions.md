---
layout: default
title: Contest Definitions
parent: User Manual
nav_order: 8
description: How built-in contest definitions and the rules engine work in ContestPilot
---

# Contest Definitions

Contest definitions are built-in rulesets that encode everything ContestPilot needs to validate, score, and format logs for specific contests.

## What's in a Definition

Each definition specifies:

- **Allowed Bands/Modes**: Which bands (e.g., 80m, 40m, 2m) and modes (SSB, CW, FT8) are legal.
- **Exchange Format**: What information you send/receive (serial, grid, state, etc.).
- **Scoring Rules**: Base points per QSO, mode/band multipliers, and segment scoring.
- **Multipliers**: Unique entities that boost your score (states, grids, prefixes, segments).
- **Duplicate/Rework Rules**: Whether repeat contacts on the same band/mode are allowed or score.
- **Time Windows**: Segments or operating periods that affect scoring.

## Browsing Definitions

When creating a contest:

1. Tap "New Contest" and you'll see a searchable list.
2. Definitions are grouped by sponsor (e.g., ARRL, WIA, CQ).
3. Search by name or sponsor to filter quickly.
4. Select a definition to view details: bands, modes, exchange fields, duration.

Examples of built-in definitions:
- **WIA Remembrance Day Contest**: VK/ZL focus, grid exchanges, per-band scoring.
- **VK Shires Contest**: Australian shire exchanges, multiplier logic.
- **ARRL Sweepstakes**: Serial, precedence, call, check, section exchange.
- **CQ WW DX**: Zone and country multipliers on all HF bands.

## How the Rules Engine Works

Once you select a definition and start logging, the **Rules Engine** enforces it automatically:

### 1. Band/Mode Validation
- Frequency entry infers band; mode is selected manually.
- If the band/mode combo isn't allowed by the definition, you'll see a warning before logging.

### 2. Exchange Validation
- Required fields are highlighted if missing or malformed.
- The **Exchange Validator** checks format (e.g., 4-character grid, valid state abbreviation).
- Real-time feedback appears as you type.

### 3. Duplicate and Rework Detection
- As you enter a callsign, the engine checks your log for duplicates on the same band/mode.
- **Duplicate**: Exact match on band/mode where rework isn't allowed; QSO won't score.
- **Rework**: Allowed repeat (e.g., same station on a different band or mode); may score per rules.

### 4. Scoring Calculation
- **Base Points**: Awarded per QSO based on band/mode (e.g., CW may earn more points than SSB).
- **Multipliers**: Tracked for unique states, grids, zones, or segments worked.
- **Segment Scoring**: Some contests split operating time into segments; each segment may have independent mults and scoring.
- The score bar updates live as you log contacts.

### 5. Export Formatting
- Definitions include Cabrillo templates and ADIF mappings.
- When you export, ContestPilot formats fields and categories per the contest's submission requirements.

## Customization and Overrides

- **Developer Mode** (if enabled in Settings): Bypass certain validations for testing; use with caution during real contests.
- **Default Exchange**: Set your typical exchange in Settings to speed up entry.

## Missing a Contest?

If a contest you want isn't in the built-in list:
- Check for updates; new definitions are added with app releases.
- Report via Get Involved → Reporting & Feedback with contest details (sponsor, rules URL, exchange format).

## Under the Hood

ContestPilot's rules engine comprises:
- **RulesEngine**: Orchestrates validation, dupe checks, and scoring.
- **ExchangeValidator**: Parses and validates exchange fields per definition.
- **ScoreCalculator**: Computes points, multipliers, and segment totals.

This architecture ensures consistent, accurate scoring without manual rule lookups.
