# Support

Check [Known issues](KNOWN_ISSUES.md) and [Compatibility](COMPATIBILITY.md) before opening
a report.

## Before Reporting a Problem

1. Confirm LMU plugins are enabled under `Settings -> Gameplay -> Enable Plugins`.
2. Fully restart LMU after enabling, disabling or updating the OpenXR layer.
3. Open the **Status** tab and follow the first stage that is not ready: application,
   layer, telemetry, OpenXR session, or HUD frames.
4. For a portable ZIP only, confirm it was completely extracted and the `openxr`
   folder is next to `ApexTrace VR.exe`.
5. Open **Diagnostics** and note the active runtime, GPU transport and submitted HUD
   frames.
6. Use **Support bundle** and inspect the resulting ZIP before sharing it.

## Bug Report Contents

- ApexTrace VR version
- LMU version and whether the issue occurs in menus, in the car or both
- Headset, connection method and active OpenXR runtime
- GPU model and Windows version
- Exact reproduction steps
- Whether desktop mode works
- Diagnostics support bundle, when it is safe to share

Never publish account credentials or unrelated personal files. Easy Anti-Cheat and
online-session reports should state whether the binaries were signed.

## Open a report

- [Bug report](https://github.com/fabiogstohl/ApexTrace-VR-Releases/issues/new?template=bug_report.yml)
- [Headset compatibility report](https://github.com/fabiogstohl/ApexTrace-VR-Releases/issues/new?template=headset_compatibility.yml)
- [Feature request](https://github.com/fabiogstohl/ApexTrace-VR-Releases/issues/new?template=feature_request.yml)
