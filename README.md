# jr_legacy_c

The original C implementation of [jr](https://github.com/jarrunner/jr), the Java launcher exe: `launcher.c` (the launcher, `.jrc` config, AOT cache, in-process JVM), `javainstall.c` (Java auto-install), `resedit.c` (icon, version and resource editing, signing), and a POSIX variant under `posix/`.

**The maintained jr is the Java/TeaVM port in [jarrunner/jr](https://github.com/jarrunner/jr).** It does everything this one does plus an embedded JSON config, self-update, jar download and verification, and a Maven plugin. New work goes there. This repository keeps the C launcher buildable for reference and for launchers made from it, which keep working as they are.

## Build

Windows, from a Visual Studio developer prompt: `build-win.bat` gives `jr.exe`. Pushing a tag `vX.Y.Z` builds, optionally signs (SignPath), and publishes a release of this repository (`.github/workflows/release.yml`).

## History

These files moved here from `jarrunner/jr` on 2026-10-01. They were at that repository's root until its PRP-21 reorganisation and under `jr_legacy_c/` after it; the full history is in [jarrunner/jr](https://github.com/jarrunner/jr). jr's own `v1.0.0` release asset was built from this code.
