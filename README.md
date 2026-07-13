# ApexTrace VR

**Telemetry HUD for Le Mans Ultimate**

[Deutsche Anleitung](README_DE.md)

> Public beta software. Read the beta limitations before using it in online sessions.

## Download

Open the repository's **Releases** page and download the latest
`ApexTrace-VR-...-windows-x64.zip` file. Do not use GitHub's automatically generated
`Source code` archives; they do not contain the application.

Each release includes a `.sha256` file so the download can be verified before it is
started.

## What It Shows

- Brake and throttle traces with live brake peak
- Steering direction and current speed
- Gear, ABS and traction-control activity
- Progressive RPM shift lights and shift flash
- Delta to the best lap with a configurable range
- English and German control-panel text

The same HUD can be displayed as a desktop overlay or as a native OpenXR composition
layer in VR. The VR mode follows the OpenXR runtime already used by LMU and does not
change the system runtime.

## Requirements

- Windows 10 or Windows 11, 64-bit
- Le Mans Ultimate with shared-memory plugins enabled
- For VR: a working 64-bit OpenXR runtime and a D3D11 LMU VR session

## Install

1. Close LMU.
2. Extract the complete ZIP to a permanent folder, for example
   `Documents\ApexTrace VR`. Do not run the EXE from inside the ZIP.
3. Start `ApexTrace VR.exe` once. No administrator rights should be requested.
4. In LMU, enable `Settings -> Gameplay -> Enable Plugins`.
5. Start Meta Quest Link, Steam Link or SteamVR as usual, then start LMU normally.
6. Enter the car. ApexTrace VR opens its settings on the desktop and renders the HUD
   in the active output mode.

The first start installs a per-user OpenXR API layer and can enable a per-user Windows
startup entry. Keep the extracted folder in place while that startup entry is enabled.

## Update

Close LMU and ApexTrace VR, replace the extracted files with the new release, then
start `ApexTrace VR.exe` once so the per-user OpenXR files are refreshed.

## Uninstall

Open **Diagnostics**, choose **Uninstall OpenXR layer**, disable Windows startup, and
close ApexTrace VR. The extracted application folder can then be deleted.

## Beta Limitations

- The current beta may be unsigned, so Windows SmartScreen can show a warning.
- Online and Easy Anti-Cheat compatibility must be rechecked for every public build.
- Headset and runtime combinations not listed in a release's test notes are unverified.
- Create a support bundle from **Diagnostics** when reporting a problem. Review the ZIP
  before sharing it because diagnostics can contain local paths and system details.

## Source Availability

The beta binaries are free to use under the included binary license. The application
source code is currently not published. Third-party components retain their own
licenses and notices.

ApexTrace VR is an independent, unofficial tool and is not affiliated with or endorsed
by Studio 397, Motorsport Games, Le Mans Ultimate, Valve or Meta.
