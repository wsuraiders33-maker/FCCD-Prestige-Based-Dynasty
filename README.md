# FCCD Prestige-Based Dynasty

**v1.0.3 — Adaptive Recruiting and Positional Balance**

**Download:** [GitHub Releases](https://github.com/wsuraiders33-maker/FCCD-Prestige-Based-Dynasty/releases/latest). For v1.0.3, choose `FCCD_Prestige_Based_Dynasty_v1_0_3_Public_Release.zip` from **Assets** after the release asset has been uploaded. Do **not** download GitHub's automatically generated source-code ZIP.

An unofficial modification for **Football Coach: College Dynasty** that scales roster capacity, recruiting resources and roster planning to school prestige. It works with standard college and compatible custom universes, not exclusively Ohio high-school universes.

## What's new in v1.0.3

- **Adaptive recruit supply:** Each year's generated or imported custom recruiting class is capped at `min(original class count, round(sum of non-FCS schools' prestige-adjusted roster caps * 30 / 85))`. Targets adapt to team count and annual prestige.
- **Oversized imported classes:** Randomly trim source recruits without forced quotas for positions, states, star ratings or potential. Retained prospects keep their source attributes.
- **Position-balanced AI recruiting:** AI teams account for returning players and commitments before chasing recruits at positions with limited room, including kickers.
- **User auto-recruiting protections:** Those same safeguards apply when automatic recruiting is enabled for the user team. Manual recruiting remains unchanged.
- **Previous features preserved:** RC7 prestige scaling, the v1.0.1 AI depth repair, the v1.0.2 transfer shortlist and Top Five + User recruiting previews. Normal college redshirts and eligibility are unchanged.

## Requirements

- Exact supported **Windows/Steam FCCD 1.6.5** file version, enforced with SHA-256 checks.
- Close the game and independently back up saves before installing or restoring.
- At least **1 GB** free on the Steam game drive.
- **Do not stack** this mod with an Ohio high-school or other unrelated FCCD mod.
- Patch-only download; the ZIP does not redistribute complete commercial game binaries.

## Install

1. Download and **extract the complete v1.0.3 release ZIP** outside the Steam game directory.
2. Close FCCD. Back up important saves.
3. **From v1.0.2 or earlier public releases:** run your *previous* release's `RESTORE.bat` first, or use Steam Verify Integrity to return to clean game files. The v1.0.3 installer intentionally refuses to overwrite v1.0.2 directly.
4. **From a verified v1.0.3 one-click private build:** the installer recognizes the existing completed installation; don't stack older patches.
5. Double-click the **top-level `INSTALL.bat`**, type `INSTALL` and look for `PASS`.
6. Run **`VERIFY.bat`** to verify both the mod files and original-game backup.

The package stages a patched build separately, checks SHA-256 hashes and preserves stock backups. Do **not** run individual scripts from the `Engine` folder.

## Restore stock game files

Close FCCD, run the **v1.0.3 ZIP's top-level `RESTORE.bat`**, type `RESTORE` and confirm `PASS`. Run `VERIFY.bat` afterward; it should report **stock files** and say v1.0.3 is not installed. This restores the original Steam game, **not v1.0.2**. Do not bypass hash mismatches or delete verified backup files.

## Prestige scaling

| Prestige | Roster cap | Human recruiting targets | AI recruiting targets |
|---|---:|---:|---:|
| 1 | 34 | 16 | 24 |
| 2 | 40 | 19 | 28 |
| 3 | 45 | 21 | 32 |
| 4 | 51 | 24 | 36 |
| 5 | 57 | 27 | 40 |
| 6 | 62 | 29 | 44 |
| 7 | 68 | 32 | 48 |
| 8 | 74 | 35 | 52 |
| 9 | 79 | 37 | 56 |
| 10 | 85 | 40 | 60 |

The mod also scales scholarship allowances, recruiting resources, preseason camp invitations and automatic official-visit selection. AI recruiting prioritizes positional needs and can pursue fallback scholarship recruits when primary targets are unavailable.

### Important roster rules

- Human coaches make required roster cuts during **Players Transferring**. AI programs make their own required cuts during that phase.
- The upcoming season's prestige-based cap governs those decisions. Coaches whose school's prestige falls receive additional penalty-free cuts to accommodate the smaller cap.
- Later commitments cannot take a program over its allowed roster capacity.
- **There are no hidden roster-cap cuts at Signing Day, year advance or preseason.**
- Recruiting reserves the space needed to satisfy minimum depth. Preseason Position Changes may generate emergency walk-ons at deficient positions **without cutting existing players or exceeding the cap**.

Some walk-ons are intentional, particularly at very small programs. The mod does not guarantee that every school signs players at every desired position.


## Testing and limitations

Live v1.0.3 custom-class tests: 2025 Northmont imported **2,500 → 1,579** recruits and 2026 Northmont imported **3,500 → 1,571**, with targets changing as roster capacity changed. Retained imported recruits were matched to the source JSON and checked for attribute preservation and sampling characteristics. A separate 148-school Dartmouth dynasty tested generation, rollover, roster caps and kicker coverage. The public ZIP's gameplay patch payload is identical to the tested one-click private package; a separate Windows installation and restore test of the newly relabeled ZIP has not been observed here.

See [release notes](RELEASE_NOTES.md) and the public ZIP's `README_FIRST.md` and `VALIDATION.md` for full validation and compatibility guidance.

*Unofficial fan-made mod; not affiliated with Football Coach: College Dynasty, Steam or Valve.*
