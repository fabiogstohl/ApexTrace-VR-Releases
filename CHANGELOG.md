# Changelog

## 0.2.0-beta.58 - 2026-07-21

- Adds an isolated one-click desktop HUD preview with animated simulated telemetry, without changing the selected output mode or saved layout.
- Adds an explicit Windows-startup choice to the installer and a Start-menu shortcut that disables only the OpenXR layer for recovery.
- Adds bilingual compatibility and known-issue documentation, structured GitHub bug/compatibility/feature forms, and release-ready static and animated HUD media.

## 0.2.0-beta.57 - 2026-07-20

- Adds a user-assignable Set-position shortcut for a keyboard key or DirectInput wheel button.
- Triggers the existing synchronized LMU and HUD recenter action only while LMU is foreground, the player is in the car, and the OpenXR session is ready.
- Reads wheel buttons nonexclusively without changing axes, calibration or force feedback, and packages the new native x64 input reader in installers, portable releases and support bundles.

## 0.2.0-beta.56 - 2026-07-20

- Adds confirmed Application actions to reset all ApexTrace settings while keeping personal best laps, or clear only the best-lap history.
- Adds a confirmed in-app uninstaller for installed builds.
- Full uninstall now removes local data, OpenXR registration and Windows startup, then restores only the LMU menu-animation and recenter values changed by ApexTrace.

## 0.2.0-beta.55 - 2026-07-20

- Adds a Best laps page to the Desktop and OpenXR control panels.
- Stores the fastest valid LMU lap for each track together with the vehicle used.
- Keeps the personal-best history locally across sessions and application restarts.

## 0.2.0-beta.54 - 2026-07-20

- Saves control-panel changes automatically with a short debounce to avoid slider-related disk churn.
- Saves Desktop HUD positions when mouse dragging ends.
- Moves Quit overlay into the Application page and removes the complete control-panel footer.

## 0.2.0-beta.53 - 2026-07-20

- Adds a centered Set position action to the header when OpenXR output is active.
- Uses the existing synchronized LMU and HUD straight-ahead centering flow from the new header action.
- Removes Origin, Find, reset, layout-centering, and duplicate driver-centering controls from the HUD module pages.

## 0.2.0-beta.52 - 2026-07-20

- Removes hidden control pages and inactive HUD module panels from Tk layout calculations.
- Makes live window-edge resizing smoother in both OpenXR and Desktop control panels.

## 0.2.0-beta.51 - 2026-07-20

- Prevents HUD Layout switches from being clipped when the module subnavigation is expanded.
- Gives the nested HUD labels and switches enough fixed navigation width without changing HUD rendering.

## 0.2.0-beta.50 - 2026-07-17

- Moves OpenXR positioning into each HUD module and removes the separate VR Position page.
- Adds independent distance, pitch, yaw, and roll values to all seven native OpenXR quads while preserving existing positions during migration.
- Moves the DESKTOP/OPENXR output selector into the top-right header and removes its duplicate Application setting.

## 0.2.0-beta.49 - 2026-07-17

- Replaces the general HUD tab with a focused Units page for speed-unit selection.
- Adds a Pedal & steering page for the shared direct/filtered LMU input setting.
- Keeps driving-specific controls on the Driving HUD page and moves global opacity and render dimensions to Application.

## 0.2.0-beta.48 - 2026-07-17

- Adds a dedicated Workarounds and fixes section to the live Status page.
- Explains the persistent LMU menu-animation workaround and the session-based Meta ASW black-wave fix directly below their controls.
- Keeps the two fixes visibly separate so their scope and effect are clear.

## 0.2.0-beta.47 - 2026-07-16

- Replaces the HUD-module checkboxes with compact on/off switches in the expandable HUD Layout navigation.

## 0.2.0-beta.46 - 2026-07-16

- Turns HUD Layout into an expandable navigation section with all seven HUD modules listed underneath.
- Selects each module directly from the sidebar and places its visibility switch on the same row.
- Removes the duplicate module toggle grid and dropdown from OpenXR and Desktop layout pages.

## 0.2.0-beta.45 - 2026-07-16

- Moves all seven module visibility switches into the HUD Layout page.
- Adds a visibility switch for the driving HUD in both OpenXR and Desktop modes.
- Defaults new installations and layout reset to the driving and vehicle HUDs only.

## 0.2.0-beta.44 - 2026-07-16

- Shows ABS, TC, TC Slip, and TC Cut together in one compact 2-by-2 change HUD.
- Opens the shared HUD when any of the four LMU control settings changes.

## 0.2.0-beta.43 - 2026-07-16

- Shows the current ABS and TC settings together in one control-change HUD.
- Keeps distinct orange ABS and blue TC values for quick recognition in VR.

## 0.2.0-beta.42 - 2026-07-16

- Adds separate fuel/hypercar-energy, warning, and ABS/TC-change HUD modules.
- Reads LMU fuel capacity, virtual energy, battery state, ABS, TC, TC Slip, and TC Cut settings.
- Adds independent size and opacity controls for all seven HUD modules.
- Adds one-click centering for the complete VR layout while preserving relative module offsets.
- Extends the desktop mode with separately draggable windows for the three new HUD modules.

## 0.2.0-beta.41 - 2026-07-16

- Split the OpenXR HUD into independently positioned driving, start-light, race, and vehicle modules.
- Changed the race HUD to a compact vertical list and moved the race start lights into their own HUD.
- Added a HUD Layout settings page with separate horizontal and vertical controls for every VR module.
- Added separate draggable desktop windows for the start lights, race data, and vehicle status.
- Kept the low-overhead single-atlas renderer and one GPU texture copy per frame.

## 0.2.0-beta.40 - 2026-07-16

- Adds the player's best lap time to the left of the delta scale.
- Adds the running current-lap time to the right of the delta scale.
- Narrows the centered pink delta bar while preserving its configured range and direction.

## 0.2.0-beta.39 - 2026-07-16

- Adds a separately configurable race-status HUD between the driving HUD and vehicle panel.
- Shows overall position and field size, gap ahead, flag, race phase, start lights, pit state and stops, and outstanding penalties.
- Reads the race values from LMU scoring shared memory and keeps the desktop and native OpenXR renderers visually aligned.

## 0.2.0-beta.38 - 2026-07-16

- Removes the tyre, brake and damage explanation blocks from the live HUD.
- Centers and narrows the lower vehicle-status panel around its actual telemetry content.
- Adds a bilingual Vehicle data page to the settings window with compact color legends.
- Updates the native visual smoke test for the intentionally transparent outer status area.

## 0.2.0-beta.37 - 2026-07-16

- Rounds the upper HUD's left corners to match the lower vehicle-status panel.
- Preserves the circular right edge and seamless shift-light pod transition.

## 0.2.0-beta.36 - 2026-07-16

- Adds a subtle outer border around the complete upper HUD surface.
- Continues the border around the shift-light pod without an internal horizontal seam.
- Matches the upper outline color and weight to the lower vehicle-status panel.

## 0.2.0-beta.35 - 2026-07-16

- Adds the average tread temperature in degrees Celsius beside every tyre.
- Keeps pressure, temperature and remaining tyre life in a compact three-line readout.
- Removes the additional pedal-trace low-pass delay while retaining stable time-grid interpolation.

## 0.2.0-beta.34 - 2026-07-16

- Replaces separate window damage rings with single connected side and rear body panels.
- Joins adjacent front, side, rear-fender and center-rear zones at shared boundary vertices.
- Removes duplicate colored frames and neutral gaps while retaining clear panel outlines.

## 0.2.0-beta.33 - 2026-07-16

- Restores both rear-fender damage panels down to the tail-light contours.
- Runs only the center-rear damage zone as a closed frame along the rear glass.
- Draws all panel fills before a dedicated outline pass so every zone boundary remains complete.
- Adds bordered telemetry frames around the side and rear windows in both renderers.

## 0.2.0-beta.32 - 2026-07-16

- Extends each side damage zone as a closed telemetry-colored frame around its side window.
- Draws the damage frame behind the glass so the color remains confined to the bodywork.
- Keeps the desktop and native OpenXR representations symmetric and visually identical.

## 0.2.0-beta.31 - 2026-07-16

- Reduces the vertical height of the windscreen, side windows and rear glass.
- Reassigns the area below the rear glass to one continuous center-rear damage panel.
- Keeps left- and right-rear damage zones beside the glass instead of splitting the rear bumper into three parts.

## 0.2.0-beta.30 - 2026-07-16

- Narrows the windscreen, both side windows and the rear glass horizontally.
- Exposes more telemetry-colored damage surface around every glass panel.
- Realigns all adjacent damage boundaries while preserving exact left-right symmetry.

## 0.2.0-beta.29 - 2026-07-16

- Reshapes the rear body contour to follow the tail-light perimeter precisely.
- Keeps both tail lights fully inside the vehicle silhouette without protruding corners.
- Aligns the rear damage zones with the revised symmetric body outline.

## 0.2.0-beta.28 - 2026-07-16

- Narrows the windscreen horizontally while preserving its centered, symmetric shape.
- Insets both side windows farther from the outer body edge for a clearer body-colored sill.
- Realigns adjacent damage panels so glass, pillars and telemetry colors remain seamless.

## 0.2.0-beta.27 - 2026-07-16

- Reshapes all eight telemetry damage zones as recognizable vehicle body panels.
- Aligns damage boundaries with the windscreen, side glass, rear glass and outer body contour.
- Keeps the desktop and native OpenXR HUD geometry visually identical.

## 0.2.0-beta.26 - 2026-07-16

- Insets both side windows so a continuous body-colored outer sill remains visible.
- Shortens the side glass to end around the longitudinal midpoint of the rear glass/engine cover.
- Keeps the front window edge parallel to the windscreen and preserves exact left-right symmetry.

## 0.2.0-beta.25 - 2026-07-16

- Gives the decorative front lights a subtle cool-white finish.
- Gives the decorative rear lights a muted red finish.
- Keeps mirrors, body panels and all eight damage zones on the telemetry color scale.

## 0.2.0-beta.24 - 2026-07-16

- Refines the vehicle schematic against a normalized, equally scaled comparison with the supplied reference.
- Replaces the trapezoidal windscreen with the reference's wide-shouldered six-sided shape.
- Extends the side glass alongside the windscreen and preserves slim parallel A-pillars plus broad parallel C-pillars.
- Matches the flatter headlights, thicker mirrors, larger tail wedges and three split rear-louver rows.
- Straightens the outer body sides while preserving all LMU damage colors and exact vertical symmetry.

## 0.2.0-beta.23 - 2026-07-15

- Rebuilt the vehicle schematic around the supplied wedge-shaped supercar top-view reference.
- Adds the pointed nose, chamfered body, mirrors, widening windscreen, long side glass and broad parallel rear pillars.
- Adds a polygonal rear engine cover with four louvers plus outlined front and tail details.
- Widens the body to match the reference proportions while retaining all eight LMU damage zones and exact symmetry.

## 0.2.0-beta.22 - 2026-07-15

- Added clearly outlined borders around all four glass areas.
- Separates the windscreen and side glass with a slim pair of parallel A-pillar edges.
- Separates the side and rear glass with a wider pair of parallel C-pillar edges.

## 0.2.0-beta.21 - 2026-07-15

- Removed the separately outlined roof insert so the center reads as one continuous body surface.
- Widened the side glass and made its inner and outer edges parallel.
- Uses a slim front A-pillar and a stronger rear C-pillar while preserving exact left-right symmetry.

## 0.2.0-beta.20 - 2026-07-15

- Reworked the damage schematic into a closed, rounded GT-style top view based on the new visual reference.
- Mirrors every body, windscreen, side-window, roof and rear-window coordinate across the vertical center line.
- Uses a centered front-zone damage sample so geometry remains visually symmetric in previews.

## 0.2.0-beta.19 - 2026-07-15

- Removed the redundant damage-status text from the center of the vehicle schematic.
- Redesigned the silhouette with distinct front and rear bodywork, wheel arches, bonnet, windscreen, roof and rear glass.
- Preserved the eight LMU damage-zone mappings and color-only overheating/part-loss warnings.

## 0.2.0-beta.18 - 2026-07-15

- Removed the unavailable brake-wear readout and its reserved legend row.
- Rebalanced the brake-temperature and damage legend vertically.
- Removed the unused brake-wear field from the internal renderer frame.

## 0.2.0-beta.17 - 2026-07-15

- Added LMU pit-speed-limiter telemetry to the HUD data path.
- Changes the speed number from white to yellow while the limiter is active in both desktop and OpenXR VR modes.
- Leaves the speed unit and all other HUD colors unchanged.

## 0.2.0-beta.16 - 2026-07-15

- Replaced the text-heavy wheel cards with an LMU-style color schematic.
- Shows all three tread-temperature zones directly in each tyre and uses the tyre outline for carcass temperature.
- Shows remaining tyre life as a side bar, brake temperature as an inner disc and all eight damage zones directly on the car body.
- Keeps exact pressure and tyre-life values next to each wheel and one honest brake-wear `N/A` indicator.

## 0.2.0-beta.15 - 2026-07-15

- Added a configurable vehicle-status panel below the HUD for all four tyres and brakes.
- Added three surface temperatures, carcass temperature, pressure, remaining tyre life, brake temperature, flat tyres and detached wheels.
- Added an eight-zone body-damage display with detached-part and overheating warnings.
- Displays brake wear as unavailable because LMU's current built-in telemetry does not provide it.
- Extended the OpenXR GPU protocol while preserving the position of the existing HUD content.

## 0.2.0-beta.14 - 2026-07-15

- Reversed the two lower shift-cap curves so the trapezoid opens smoothly into the HUD surface.
- Kept both transitions horizontally tangent to the HUD top edge.
- Preserved the cap height, centered lights and original HUD layout.

## 0.2.0-beta.13 - 2026-07-15

- Removed the visible lower trapezoid seam and blended the rounded sides tangentially into the HUD top surface.
- Locked the shift-light row and trapezoid geometry to the same horizontal center.
- Preserved the cap height, original HUD geometry and OpenXR anchor.

## 0.2.0-beta.12 - 2026-07-15

- Increased the shift-light cap height and added balanced space above and below the lights.
- Added small rounded corners to the trapezoid backdrop in both desktop and OpenXR rendering.
- Preserved the original HUD block geometry and in-car anchor.

## 0.2.0-beta.11 - 2026-07-15

- Added a compact trapezoid backdrop behind the raised shift-light row.
- Matched the backdrop to the HUD opacity and kept its upper edge only slightly wider than the four lights.
- Kept the original HUD geometry and OpenXR anchor unchanged.

## 0.2.0-beta.10 - 2026-07-15

- Restored the telemetry diagram and every existing HUD element to their previous layout.
- Added the centered shift lights as a transparent cap above the original HUD boundary.
- Added OpenXR anchor compensation so the original HUD block stays at the configured in-car position.

## 0.2.0-beta.9 - 2026-07-15

- Raised the centered shift-light row to the upper edge of the HUD.
- Reserved a clear header above the telemetry diagram so its lines no longer pass behind the shift lights.
- Applied the same separated layout to the desktop and native OpenXR renderers.

## 0.2.0-beta.8 - 2026-07-15

- Moved the three blue shift lights and blinking red shift flash to the top center of the HUD.
- Increased shift-light size consistently in the desktop and native OpenXR renderers.
- Kept the gear-number red flash synchronized with the red shift flash.

## 0.2.0-beta.7 - 2026-07-15

- Replaced gaze-only driver centering with one synchronized **Center LMU + HUD straight ahead** action.
- Added backup-first setup of a free LMU keyboard recenter binding without replacing existing keyboard or wheel controls.
- Added local diagnostics and automated tests for binding setup, input delivery and OpenXR HUD centering.

## 0.2.0-beta.6 - 2026-07-14

- Added explicit Meta ASW controls to the Status and Diagnostics pages for Quest Link users affected by black VR-menu edge artifacts.
- Added English/German status, guarded LMU foreground handling and local diagnostics for the last ASW command.
- Confirmed that the workaround changes only the current Meta Link session and does not alter the OpenXR runtime.

## 0.2.0-beta.5 - 2026-07-14

- Added a calibrated driver-view origin that matches the HUD to LMU's recentered driving position.
- Added an English/German centering action with native OpenXR acknowledgement and live status.
- Extended the virtual compositor tests to verify driver-view capture at 72, 90 and 120 Hz and during GPU-resource recovery.

## 0.2.0-beta.4 - 2026-07-14

- Added LMU VR-menu flicker status to the Status and Diagnostics pages.
- Added a confirmed, backup-first repair for LMU's menu background-animation setting.
- Added Steam-library discovery for LMU installations outside Steam's default folder.

## 0.2.0-beta.3 - 2026-07-14

- Added an update check that links to the official GitHub release page for manual downloads.
- Redesigned the English and German control panel with clearer status, application,
  VR-position and diagnostics views.

## 0.2.0-beta.2 - 2026-07-14

- Added a per-user Windows installer and clean uninstaller.
- Added a background update check that links only to official GitHub releases.
- Added a first-start and live health chain for telemetry, OpenXR and HUD rendering.
- Added a persistent `kph` / `mph` display option.
- Added a guarded release-signing pipeline for the EXE, native DLLs, installer and uninstaller.
- Split update, unit and health logic into independently tested modules.
- Removed obsolete OpenVR overlay and Steamworks packaging paths.

## 0.2.0-beta.1 - 2026-07-14

- Renamed the application to ApexTrace VR.
- Added native OpenXR HUD output alongside desktop overlay output.
- Added brake and throttle history, live brake peak, steering, speed, gear, ABS and TC.
- Added progressive RPM shift lights and a flashing shift indicator.
- Added best-lap delta with a configurable display range.
- Added English and German settings UI.
- Added local diagnostics, support bundles and per-user OpenXR installation controls.
- Added migration from existing `vrLMU Pedals` user settings and layer registration.
