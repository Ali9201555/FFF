# Dragontwin — Early Access (Windows build)

Packaged Unreal Engine Windows build of **Dragontwin** (early access), stored as a
multi-part archive attached to this repository's **Releases** page.

The build is 7.4 GB with a single 7.1 GB `.ucas` pak file, which exceeds every
GitHub per-file limit (100 MB in git, 2 GB in LFS / release assets), so the build
is stored as split 7-Zip volumes under 2 GB each.

## Download & reassemble

1. Download **all** `dragontwin-early-access-win.7z.00*` parts from the latest
   release into one folder.
2. Extract the **first** part — 7-Zip finds the rest automatically:

   ```
   7z x dragontwin-early-access-win.7z.001
   ```

   (Or right-click `…7z.001` → 7-Zip → Extract here.)
3. Run `dragontwin-early-access-win\Dragontwin.exe`.

## Integrity

SHA-256 checksums for each part are in [`SHA256SUMS.txt`](SHA256SUMS.txt) and on
the release notes. Verify with:

```
Get-FileHash .\dragontwin-early-access-win.7z.001 -Algorithm SHA256
```

## Contents

- `Dragontwin/` — game content, binaries (`Dragontwin-Win64-Shipping.exe`), paks
- `Engine/` — UE runtime redistributables (incl. `UEPrereqSetup_x64.exe`)
- `Dragontwin.exe` — launcher
