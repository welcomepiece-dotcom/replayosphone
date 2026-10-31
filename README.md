# Android 16 GSI Build (TrebleDroid / AOSP base)

This repository contains a GitHub Actions workflow that builds a minimal, clean
Android 16 (AOSP/TrebleDroid base) ARM64 GSI (`system.img.xz`).

## Operational notes

- Runner: `ubuntu-24.04`.
- Swap: 32 GB allocated via `easimon/maximize-build-space`.
- Build target: `treble_arm64_bvN-userdebug`.
- Manifest: `https://github.com/ponces/treble_aosp.git` branch `android-16.0`.
- Output artifact: `system.img.xz`.

## Trigger the build

```bash
gh workflow run build_gsi.yml
```

## Download the compiled system.img.xz

```bash
gh run download --name android-16-gsi-system-img
```