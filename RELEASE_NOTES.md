# FCCD Prestige-Based Dynasty — v1.0.0

**First stable public release · RC7 gameplay code frozen**

## Features

- Prestige-adjusted team roster caps from **34 to 85** players.
- Human and AI recruiting-target allowances scaled to team prestige.
- Scaled recruiting points, scholarship allowances, preseason recruiting camps and automatic official visits.
- AI roster planning that preserves capacity for required positional depth.
- Improved AI recruiting for critical positions, including realistic backup prospects and scholarship-offer priorities; no forced commitments.
- All required prestige-related roster cuts occur during **Players Transferring**, with additional integrity-safe cut allowances when prestige decreases.
- No automatic cuts at Signing Day, year advance or preseason to fix roster overages.
- Incoming signees, transfers and eligible returning players preserved during rollover.
- Emergency position-depth walk-ons used where recruiting still leaves shortages, without exceeding caps or removing established players.
- Generic **FCCD Prestige-Based Dynasty** scope, not tied to any Ohio or high-school universe.

## Live RC7 validation

A complete 1982–1983 season cycle in a 112-regular-school college universe recorded:

- **112 / 112** schools within their actual 1983 prestige caps.
- **112 / 112** schools meeting positional minimums after Position Changes.
- **4,375 / 4,375** eligible returning players preserved.
- **1,726 / 1,726** committed high-school, junior-college and transfer players arriving at their schools.
- **0** unplanned cuts during rollover and Position Changes.
- **41** generated walk-ons across **30** schools (compared with 50 across 32 schools in the prior RC6 test).

These are results of one full test cycle, not a guarantee that every universe or future game version will behave identically. Small schools may still require some walk-ons.

## Public installer validation

- The distributed ZIP is **patch-only**. It includes no full commercial-game binaries.
- An independent reconstruction from verified original FCCD files reproduced both RC7 output files **byte-for-byte**.
- Installer checks SHA-256 hashes for original files, unpacked dependencies and the patch payload.
- **A Windows installation and restore using a separate copied `resources` folder was reported successful.**
- The packaged script creates original-file backups and refuses incompatible game versions.
- The resulting public-patch files match the private RC7 gameplay files already live-tested. An independent Steam game-launch smoke test using the patch-only installer itself was not performed in the test-copy environment.

## Installing and restoring

Extract the ZIP, run **`INSTALL.bat`** and follow its prompts. To remove the mod and return to the original files, run **`RESTORE.bat`** from the same extracted release. See `README.md` for compatibility notes and detailed instructions.

## Known limitations

- This patch is locked to a **specific verified version** of the game's original files. A Steam update may require a new patch.
- RC7 improves AI positional recruiting but cannot eliminate all emergency walk-ons, especially at low prestige.
- The patch cannot be layered over another modded `app.asar` or worker file.
- The installer is intended for Windows Steam installations.