# Troubleshooting / verification

**Before anything else:** close the game and make sure you extracted the whole ZIP.

| Installer message / behavior | Meaning and what to do |
|---|---|
| Original file hash mismatch | Your game version or existing mod is incompatible. Do not bypass the check. Restore unmodified supported game files or wait for a new patch. |
| Missing unpacked dependency | The game copy is incomplete or does not match the verified version. Verify Steam files and retry. |
| Patch payload hash mismatch | Redownload the release ZIP and extract it again. Do not install using a damaged patch. |
| Access denied / file in use | Close the game and other programs locking the game directory. Check directory permissions. |
| Public patch already installed and verified | Nothing more is required. |
| Original game files already installed | Restore already completed or the mod is not installed. |
| Restore fails because backups are missing | Keep the folder as-is. Steam's file-integrity verification can restore original game files, but may overwrite other mods. |

The scripts check expected hashes and create backups before changing files. Do not remove `resources\FCCD_PrestigeBasedDynasty_v1_Backup` while the mod is installed.

For support or bug reports, provide the game build/version, the exact installer error, your Windows version and whether your game was previously modified. **Do not upload copyrighted game files publicly.**