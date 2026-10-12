# FCCD Prestige-Based Dynasty

**Version 1.0.0 — public patch-only release**

An unofficial modification for **Football Coach: College Dynasty** that scales roster capacity, recruiting resources and roster planning according to each school's prestige. It works with compatible standard college and custom universes. **The Ohio high-school universes used for development are not required.**

## What you need

- A legally installed, compatible, **unmodified** Steam copy of Football Coach: College Dynasty.
- Windows with PowerShell, included in standard Windows installations.
- The game fully closed while installing or restoring.
- Enough free disk space to reconstruct game files and retain backup copies.

**Important:** This installer only supports the exact original game-file version identified by its built-in SHA-256 hashes. It does not overwrite a different game version or another mod. This is intentional. Steam updates may make this patch incompatible until a new release is verified.

The ZIP contains a compact binary patch and scripts, **not complete commercial-game binaries**. No Python, Node.js, Git or separate patcher is required.

## Install

1. Download and **extract the entire ZIP** to a normal folder.
2. Close the game.
3. Double-click **`INSTALL.bat`**.
4. Press **Enter** when asked for the game `resources` folder if you use the normal Steam location. If your game is elsewhere, enter its full `resources` directory (the folder with `app.asar`).
5. The installer verifies the vanilla game files, unpacked dependencies and patch payload **before making any changes**.
6. When prompted, type **`INSTALL`** and press Enter (capitalization does not matter).
7. Wait for **`PASS: FCCD Prestige-Based Dynasty v1.0.0 installed and verified.`**

The installer reconstructs the verified release from your own original files, then creates a backup before replacing anything. Backups are stored in `resources\FCCD_PrestigeBasedDynasty_v1_Backup`.

Your dynasty saves are **not modified by the installer**, but keeping independent backups of important saves is still recommended.

## Restore the original game

1. Close FCCD.
2. Double-click **`RESTORE.bat`** from the same extracted release folder.
3. Select the same `resources` folder used for installation.
4. Type **`RESTORE`** and press Enter.
5. Look for **`PASS: Unmodified original game files restored and verified.`**

The restore tool verifies both the modded files and the original backups before restoring them. It retains the backups afterward.

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

## Compatibility and troubleshooting

- The installer changes only `resources\app.asar` and `resources\app.asar.unpacked\dist\main\coreWorker.js`.
- If it reports an unrecognized original hash, **do not override the check**. Use Steam's file-integrity verification (after preserving any personal mod backups) and ensure you have the supported game version.
- If your game is installed in a nonstandard Steam library, enter its `resources` directory when prompted.
- If you have RC7 or another test mod installed, first restore its original backed-up files; this public installer does **not** install on top of another mod.
- If the game updates, this patch may no longer install or may be replaced by the update. Wait for a compatible release if necessary.
- If Windows security policy blocks PowerShell scripts, review the source scripts or use an environment that permits running them. Do not disable organizational security rules without authorization.
- Keep your original backup folder and extracted release ZIP until you are finished with the mod.

## Verification and scope

This patch reconstructs the **exact gameplay files of the RC7 build selected for v1.0.0**. Their reconstructed bytes were independently compared with the tested RC7 files.

The installer and restore were successfully exercised on Windows against a **separate copy of a compatible game `resources` folder**. The RC7 gameplay build completed a live in-game annual-cycle test. A separate in-game Steam launch using this final public patch installer has not been independently reported; the resulting game binaries match RC7 byte-for-byte.

This mod is community-made and is not affiliated with the developer of Football Coach: College Dynasty, Steam or Valve.