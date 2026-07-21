# Privacy

ApexTrace VR processes LMU shared-memory telemetry locally on the PC. The current beta
does not contain analytics, advertising, accounts, cloud synchronization or automatic
network telemetry.

Configuration, personal best laps, rotating logs and runtime diagnostics are stored in the
current user's application-data directory. Personal-best records contain the LMU track name,
vehicle name, lap time and update timestamp and are never transmitted. A support bundle is
created only when the user selects the corresponding diagnostics action or command-line
option. That bundle can contain local
file paths, runtime names, graphics-adapter information, configuration values and recent
application logs. Users should inspect it before uploading it to a public issue.

Opening an external help or project link uses the system's default browser. ApexTrace VR
does not transmit the support bundle automatically.

Version 0.2.0-beta.59 checks the public GitHub Releases API in the background when the
control panel starts and when the user selects **Check for updates**. The request contains
the application name and version in the standard HTTP user-agent header. No LMU telemetry,
configuration, diagnostics, account identifier or support bundle is sent.

When an update is available, the user can open the official GitHub release page in the
system browser. ApexTrace VR does not download or install updates itself.

The application reads LMU's local `Settings.JSON` to report whether the known VR-menu
flicker workaround is active. It changes the menu background-animation setting only after
the user selects the repair action, confirms it, and closes LMU. A dated backup is stored
next to the original LMU settings file. This information is not transmitted.

To synchronize LMU and HUD centering, ApexTrace VR creates or updates LMU's local custom
`keyboard.json` while LMU is closed and enables that keyboard profile in
`current controls.json`. It adds only a free recenter key and preserves existing keyboard
and wheel assignments. Dated backups of files that already existed are stored next to the
originals. Pressing the centering action sends that local key to LMU and captures the same
OpenXR headset pose for the HUD. The pose remains only in LMU process memory for the current
OpenXR session and is not transmitted.

An optional Set-position shortcut stores only its keyboard key code or the selected local
DirectInput device GUID, device name and button number in `config.json`. ApexTrace reads
that one key or button without exclusive device access and does not change wheel axes,
calibration or force feedback. The assignment is not transmitted; it appears only in a
support bundle the user explicitly creates.

The Meta ASW controls are available only after an explicit user action. They send Meta's
ASW off or automatic keyboard command to the running LMU window and record the last command
in local diagnostics. They do not change the selected OpenXR runtime or transmit data.

Selecting **HUD preview** starts a second local Desktop-mode process with simulated
telemetry and a temporary copy of the current HUD configuration. It does not read LMU
telemetry, change the saved output mode or transmit data. ApexTrace deletes the temporary
configuration when the preview closes.

The Application page provides separately confirmed actions to reset ApexTrace settings
while retaining personal best laps, clear only the personal-best history, or uninstall the
application. Full uninstall deletes ApexTrace configuration, logs, diagnostics and personal
best laps, removes its OpenXR and Windows-startup registrations, and restores only the LMU
menu-animation and recenter-binding values changed by ApexTrace. Unrelated LMU values and
bindings are preserved.

This document describes version 0.2.0-beta.59. A future release that adds an online service,
analytics or automatic uploads must update this document before release.
