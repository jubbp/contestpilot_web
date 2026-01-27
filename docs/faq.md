---
layout: default
title: FAQ & Troubleshooting
nav_order: 5
description: Common questions and fixes for ContestPilot users
---

# FAQ

**Which platforms are supported?**
- iPhone and iPad on iOS/iPadOS 15.1 or later. Mac builds may be limited during testing.

**How do I join testing?**
- Install TestFlight and request access via [info@contestpilot.app](mailto:info@contestpilot.app). See Get Involved for alpha/beta details.

**Where do I export logs?**
- Open Export in a contest to generate ADIF or Cabrillo and share via the system Share Sheet.

**Why is a QSO marked duplicate?**
- The same station on the same band/mode is already logged. Reworks may be allowed on other bands/modes per contest rules.

**How are bands and modes set?**
- Frequency sets band automatically; mode is selected manually in QSO Entry.

**What is a multiplier?**
- A scoring factor for unique entities (states, grids, prefixes, segments) defined by the contest rules.

**Can I edit a logged QSO?**
- Yes. Open Log Management, select the QSO, and edit; validation runs on save.

# Troubleshooting

**Validation keeps failing on exchange**
- Confirm the contest definition’s expected exchange (serial, grid, state, etc.). Ensure fields match the required format.

**Export file won’t open elsewhere**
- Re-export both ADIF and Cabrillo. Verify the target app supports the chosen format.

**Score looks off**
- Check contest definition, duplicates/reworks, and multipliers. Compare against the score bar and recent QSOs.

**I don’t see my contest**
- Ensure you selected a built-in definition. If missing, report via Get Involved → Reporting & Feedback with contest details.

**App feels slow with many QSOs**
- Try filtering/hiding duplicates in Log Management. If performance issues persist, report with device, OS, and log size.

**TestFlight build issues**
- Restart TestFlight, ensure network connectivity, and retry. If it persists, email a screenshot of the error and your OS version.
