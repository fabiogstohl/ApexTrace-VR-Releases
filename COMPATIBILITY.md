# Compatibility

[Deutsche Version](COMPATIBILITY_DE.md)

ApexTrace VR is a Windows x64 public beta. A result marked **Verified** means that the
listed combination completed the stated test. It is not a guarantee for other drivers,
headsets, OpenXR runtimes or future LMU builds.

## Verified combinations

| Output | Runtime / connection | System | Test | Status |
| --- | --- | --- | --- | --- |
| OpenXR VR | SteamVR OpenXR with Meta Quest Link | Windows 11, NVIDIA GeForce RTX 5070 | LMU menu, in-car HUD, pause and session exit | Verified |
| Desktop | Windows desktop compositor | Windows 11, NVIDIA GeForce RTX 5070 | Demo, LMU telemetry and independent HUD windows | Verified |
| OpenXR VR | SteamVR virtual HMD | Windows 11, 72 / 90 / 120 Hz | Automated compositor submission and recovery tests | Verified (virtual HMD) |

The physical Meta Quest test required LMU's menu-background animation workaround. On
Quest Link, disabling Meta ASW for the current session can also remove black edge waves.
Both actions are explicit controls under **Status** and **Diagnostics** and can be
reverted.

## Not yet verified

- AMD and Intel graphics adapters
- Meta OpenXR used directly without SteamVR
- Vive, Pimax, Varjo, Windows Mixed Reality, Virtual Desktop and ALVR runtimes
- Every Meta Quest model and every wired or wireless Link configuration
- Online RaceControl and Easy Anti-Cheat acceptance for this exact public build
- DirectInput Set-position shortcuts across every wheel and button-box manufacturer

Unverified does not mean unsupported; it means that no reproducible result has been
recorded yet. Submit a
[Headset compatibility report](https://github.com/fabiogstohl/ApexTrace-VR-Releases/issues/new?template=headset_compatibility.yml)
to add a tested configuration.

## What to include in a report

- ApexTrace VR and LMU versions
- Headset and wired or wireless connection method
- Active OpenXR runtime
- GPU, driver and Windows versions
- Refresh rate and approximate test duration
- Menu, loading, in-car, pause and session-exit results
- Whether the session was offline or used RaceControl / Easy Anti-Cheat

Review a Diagnostics support bundle before sharing it because it can contain local paths
and system details.
