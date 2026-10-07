# Agent Instructions

This repository is a Unity performance bug repro, not a game. Changes to rendering, XR, scene, or build settings can change the measurement; preserve the intended repro unless the user explicitly asks to alter it.

The comparison is Unity `6000.7.0b3` on `main` versus Unity `2022.3.4f` on `2022.3.4f`. Do not assume the branches are otherwise identical: the current snapshots differ in MSAA level, enabled build scenes, and package versions. Verify these and other relevant settings before attributing a performance difference solely to the Unity version. Keep both branches aligned when changing a setting that is not the variable under test.

Build and measure from the Unity Editor version specified by `ProjectSettings/ProjectVersion.txt`, with the Android target, on Meta Quest. This repository has no C# test suite or build script; generated `.csproj` and `.sln` files are not authoritative project configuration.

For the reproduction steps, see [README.md](README.md). For the key settings/assets, XR setup, Android manifest caveat, and Unity YAML editing notes, see [CLAUDE.md](CLAUDE.md). Preserve Unity `.meta` files and GUIDs when editing assets manually.