# ApexTrace VR

**Telemetry HUD for Le Mans Ultimate**

[Deutsche Anleitung](README_DE.md) | [Compatibility](COMPATIBILITY.md) | [Known issues](KNOWN_ISSUES.md) | [Support](SUPPORT.md)

> Public beta software. Read the beta limitations before using it in online sessions.

### [Download ApexTrace VR 0.2.0-beta.60 installer](https://github.com/fabiogstohl/ApexTrace-VR-Releases/releases/download/v0.2.0-beta.60/ApexTrace-VR-v0.2.0-beta.60-setup.exe)

[View all release files and checksums](https://github.com/fabiogstohl/ApexTrace-VR-Releases/releases)

![ApexTrace VR HUD preview](media/hud-preview.png)

The preview uses simulated telemetry. Verified LMU and OpenXR combinations are listed on
the [compatibility page](COMPATIBILITY.md). Open the
[30-second animated HUD preview](media/hud-demo.webp) to see the live transitions.

## Download

Download the [current Windows installer](https://github.com/fabiogstohl/ApexTrace-VR-Releases/releases/download/v0.2.0-beta.60/ApexTrace-VR-v0.2.0-beta.60-setup.exe). This is the normal
per-user installer and does not require administrator rights. Older versions and checksums
remain available on the [Releases page](https://github.com/fabiogstohl/ApexTrace-VR-Releases/releases).

The portable `windows-x64.zip` is available for advanced use. Do not use GitHub's
automatically generated `Source code` archives; they do not contain the application.
Each installer and portable ZIP has a matching `.sha256` file.

## What It Shows

- Brake and throttle traces with live brake peak
- Steering direction and current speed
- Yellow speed readout while the pit-speed limiter is active
- Gear, ABS and traction-control activity
- Progressive RPM shift lights and shift flash
- Delta to the best lap with a configurable range, best lap and running lap time
- Race position and field size, gap ahead, flag, race phase and start lights
- Fuel level and hybrid energy for supported hypercars
- Separate warning and ABS/TC setting-change HUDs
- Pit request/state, completed stops and outstanding penalties
- Three surface temperatures, carcass temperature, pressure and remaining life for every tyre
- Brake temperature, flat tyre and detached-wheel warnings for every corner
- Eight-zone body damage, detached-part and overheating warnings
- Compact LMU-style vehicle schematic with color-coded tyres, brakes, wear and damage
- English and German control-panel text

The same HUD can be displayed as a desktop overlay or as a native OpenXR composition
layer in VR. The VR mode follows the OpenXR runtime already used by LMU and does not
change the system runtime.

Switch between `DESKTOP` and `OPENXR` with the output selector at the top right. ApexTrace
saves the choice, updates Windows startup, and restarts in the selected mode.

Use **Units** to select the speed unit and **Pedal & steering** to choose direct or
filtered LMU input signals. Global opacity and render dimensions are under
**Application**, together with the **Set-position shortcut**, **Quit overlay**, confirmed
reset actions and full uninstall.
Select **HUD preview** there to open every HUD with animated simulated data on the desktop.
The preview uses a temporary configuration and does not change the selected output mode or
saved layout.
**Reset application** restores every ApexTrace setting and HUD layout while keeping the
personal-best history. **Clear best laps** deletes only that history. Settings that affect
only one HUD remain on that module's page. Every setting is saved automatically after it changes.
**Best laps** keeps the fastest valid LMU lap for each track and the vehicle used for it.
The history is stored locally and survives session and application restarts.

The driving HUD, start lights, vertical race list, vehicle status, fuel/energy, warnings,
and ABS/TC changes are separate modules. Expand **HUD Layout** in the left navigation to
select or show/hide each module, then move, resize, and fade it independently. In Desktop mode,
disable click-through and drag each module directly with the mouse.
In OpenXR mode, every module also has its own distance, pitch, yaw, and roll controls.
New installations enable only the driving and vehicle-status HUDs; all other modules
can be enabled from the switches below **HUD Layout**.

### Center LMU and the HUD straight ahead

ApexTrace prepares a free LMU keyboard recenter binding on its first start while LMU is
closed. Existing keyboard and wheel assignments are preserved. In the desktop control
panel, select **Set position** in the center of the OpenXR header. Wait until
**LMU + HUD centered straight ahead** appears.

For use from the cockpit, open **Application -> Set-position shortcut**, select **Bind**,
then press one keyboard key or wheel button. **Clear** removes the assignment. The assigned
input runs the same synchronized action only while LMU is in the foreground, the player is
in the car and the OpenXR session is ready. Wheel buttons are read through nonexclusive
DirectInput and remain available to LMU.

The one action recenters LMU and captures the same OpenXR view for the HUD, so both use
the same driver-forward direction. Repeat it after restarting LMU or whenever the driving
position needs to be centered again. The captured pose is kept only for the current
OpenXR session.

## Requirements

- Windows 10 or Windows 11, 64-bit
- Le Mans Ultimate with shared-memory plugins enabled
- For VR: a working 64-bit OpenXR runtime and a D3D11 LMU VR session

## Install

1. Close LMU.
2. Run `ApexTrace-VR-...-setup.exe` and finish the setup. It installs only for the
   current Windows user. The installer visibly lets you choose whether the ApexTrace
   background service starts with Windows.
3. In LMU, enable `Settings -> Gameplay -> Enable Plugins`.
4. Start Meta Quest Link, Steam Link or SteamVR as usual, then start LMU normally.
5. Enter the car. ApexTrace VR opens its settings on the desktop and renders the HUD
   in the active output mode.

Setup installs the per-user OpenXR API layer and enables the per-user background
service only when that installer option is selected. Both can be changed later in the
control panel. Existing HUD settings and the current startup choice are preserved during
upgrades.

The **Status** and **Diagnostics** pages detect LMU's VR-menu background-animation
setting. If menu flicker protection is not active, **Fix menu flicker** can disable that
single setting after confirmation. Close LMU first; ApexTrace creates a dated
`Settings.JSON` backup before writing the change.

For Quest Link systems where black waves still appear at the edge of the LMU VR menu,
**Status** and **Diagnostics** provide explicit **Disable Meta ASW** and **Restore
automatic** controls. They affect only the current Meta Link session, require LMU to be
running, and do not change the selected OpenXR runtime.

## Update

The control panel checks GitHub Releases after startup and also provides **Check for
updates**. When a newer version is available, use **Open GitHub release** and download
the installer manually from the official release page. ApexTrace VR never downloads or
installs updates automatically.

## Uninstall

Close LMU, then select **Uninstall ApexTrace VR** under **Application**, or remove
**ApexTrace VR** under Windows **Installed apps**. After confirmation, the uninstaller
removes the per-user OpenXR layer, Windows startup entry, configuration, diagnostics and
personal best laps. It also restores only the LMU menu-animation and recenter-binding
values changed by ApexTrace, preserving unrelated LMU settings and assignments.

For a portable installation, use **Diagnostics -> Uninstall OpenXR layer**, disable
Windows startup, close the application, and delete the portable folder.

If LMU cannot reach its menu after an OpenXR or LMU update, use **ApexTrace VR - Disable
OpenXR layer (recovery)** from the Windows Start menu. It disables only the VR layer and
keeps ApexTrace settings and personal best laps. Fully restart LMU afterwards.

## Beta Limitations

- The current beta may be unsigned, so Windows SmartScreen can show a warning.
- Online and Easy Anti-Cheat compatibility must be rechecked for every public build.
- Headset and runtime combinations not listed in a release's test notes are unverified.
- Create a support bundle from **Diagnostics** when reporting a problem. Review the ZIP
  before sharing it because diagnostics can contain local paths and system details.

See the complete [known-issues and recovery list](KNOWN_ISSUES.md).

## Source Availability

The beta binaries are free to use under the included binary license. The application
source code is currently not published. Third-party components retain their own
licenses and notices.

ApexTrace VR is an independent, unofficial tool and is not affiliated with or endorsed
by Studio 397, Motorsport Games, Le Mans Ultimate, Valve or Meta.
