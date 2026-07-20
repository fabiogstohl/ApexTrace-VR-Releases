# Known Issues

[Deutsche Version](KNOWN_ISSUES_DE.md)

## Public beta limitations

- The current binaries are not Authenticode-signed. Windows SmartScreen can therefore
  show an unknown-publisher warning. Download only from this repository's Releases page
  and compare the provided SHA-256 checksum.
- Online RaceControl and Easy Anti-Cheat acceptance must be checked for every ApexTrace
  and LMU build. The current public build is not advertised as universally online-safe.
- Some LMU VR menus can show flickering geometry or dark edge waves. Use **Fix menu
  flicker** first. Quest Link users can then try **Disable Meta ASW** for the current
  Meta session. Restore automatic ASW when it is no longer needed.
- An OpenXR API layer remains loaded until LMU is fully restarted. Close LMU before
  installing, updating, enabling or disabling the layer.
- The Set-position wheel shortcut uses nonexclusive DirectInput. Wheel models not listed
  in the compatibility reports remain unverified.
- HUD placement is stored per application, not separately per vehicle or headset.

## Recovery

Use **ApexTrace VR - Disable OpenXR layer (recovery)** from the Windows Start menu if LMU
cannot reach the menu after an update. This disables only the VR layer; it does not delete
the application, settings or personal best laps. Fully restart LMU afterwards.

See [Support](SUPPORT.md) before opening a bug report.
