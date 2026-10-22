# v0.1.0-preview.2

Current sideload preview, published October 22, 2026, from the verified October 22
development build. The APK is unchanged from the signed build installed on the
development Quest 2; it has not been repacked or resigned for publication.

## Changes Since Preview 1

- Quest/OpenXR recenter handling and a Recenter player button return the tracked
  rig to the baseline facing the court, clear active balls and restart the feed
  countdown while preserving machine and racket settings.
- Less springy racket response with bounded, speed-dependent string-bed damping,
  off-center losses, tangential brushing and spin. Contact uses a finite swept
  elliptical string bed, not a single point. Individual strings and frame,
  throat and handle impacts are not modeled.
- Softer, neutral-warm night floodlights with lower glare and a corrected
  world-space analytic ball-shadow projection to reduce camera-dependent edge
  instability. This is not a claim that all headset shimmer is resolved.
- Independent Hide/Show ball machine and court-selection menu buttons on the
  always-visible rear racket panel, moved slightly farther behind the player.
  Visibility is saved without resetting other settings; hidden menus reject input.
- Retains Club, Alpine, Forest and surrounding New York Rooftop scenery, day/night
  controls, ball-machine settings and three-axis racket calibration.

## Validation And Limitations

- Full automated local suite passed on October 22: 38,996 tennis, 1,762 environment
  and 707 synthetic-XR assertions, plus tooling, shader contracts, compatibility,
  import and scene/bindings checks.
- APK v2 signature, existing signing certificate, ARM64-only libraries, OpenXR
  loader/startup, Quest manifest and source/build provenance verified again before
  publication. No engine or dependency upgrades.
- Installed in place on Quest 2 on October 22 without clearing app data. The
  automated launch observation stopped at the controllers-required system dialog.
  The user subsequently supplied [Quest gameplay footage](https://github.com/aleksmilivojevic/quest-tennis/releases/tag/gameplay-demo-2026-10-22);
  this does not establish acceptance of every feature or sustained performance.
- Desktop recenter/physics and night-lighting scenarios were visually reviewed;
  dedicated rendering of the latest menu-visibility changes was deferred by the
  user. Headless menu regressions passed.
- Standard Quest recenter behavior, physical swing feel, stereo comfort, night
  motion shimmer and sustained frame rate still need targeted headset testing.
  Other headset models remain unvalidated.
- No opponent, scoring, online multiplayer or finished match flow. Physics
  remains experimental, not a calibrated model of a particular tennis racket.

## Install Or Update

Download [quest-tennis.apk](https://github.com/aleksmilivojevic/quest-tennis/releases/download/v0.1.0-preview.2/quest-tennis.apk)
or the [complete sideload bundle](https://github.com/aleksmilivojevic/quest-tennis/releases/download/v0.1.0-preview.2/quest-tennis-sideload.zip).
Follow [installation instructions](https://github.com/aleksmilivojevic/quest-tennis/blob/main/INSTALL.md).
Install over the existing app with `adb install --no-incremental -r quest-tennis.apk`
or your desktop installer's update action. Do not uninstall first; the unchanged
signing certificate and package allow saved settings to be retained.

The installed app is **Quest VR Game**, package
`com.aleksandarmilivojevic.questvrgame`. Android still reports `0.1.0` / code `1`;
use the GitHub preview tag and checksum to identify this build. Debug-signed,
ARM64-only; intended for sideload testing, not store distribution.

APK SHA-256: `90963b260192dbdf57aac9a22ea1da0cf27accc42a9b5aff43599cdbcaba3596`.

---

# v0.1.0-preview.1

First public sideload preview, prepared October 16, 2026, from the signed
October 15 build. The APK has not been repacked or resigned for this release.

## Included

- Tennis practice with an adjustable ball machine, racket angle calibration and saved settings.
- Club, Alpine, Forest and New York Rooftop venues, with day/night controls.
- Buildings surrounding the rooftop court rather than on only one side.
- Brighter night fill, lower glare and disabled floodlight scene shadow maps.
- Frame-synchronized analytic ball shadows retained in day and night modes.

## Validation And Limitations

- APK v2 signature, ARM64 libraries, OpenXR loader and Quest manifest checked.
- Automated tests passed: 24,271 tennis checks, 1,682 environment checks, and supporting runtime/tooling checks.
- Venue render passed 63 checks and 24 input-replay steps; all 15 images reviewed. Desktop live-control smoke also passed.
- Installed successfully on the development Quest 2.
- The final startup observation was blocked by Quest's controllers-required dialog. It is not a successful final headset playtest.
- Night-motion shimmer, comfort, sustained frame rate and other Quest models remain unverified for this build.
- No opponent, scoring, online multiplayer or finished match flow. Physics tuning remains experimental.

The installed application is **Quest VR Game**, package
`com.aleksandarmilivojevic.questvrgame`, Android version `0.1.0` / code `1`.
The GitHub preview tag is more specific than the Android app version.

Download [quest-tennis.apk](https://github.com/aleksmilivojevic/quest-tennis/releases/download/v0.1.0-preview.1/quest-tennis.apk),
or the [complete ZIP](https://github.com/aleksmilivojevic/quest-tennis/releases/download/v0.1.0-preview.1/quest-tennis-sideload.zip).
Read [installation instructions](https://github.com/aleksmilivojevic/quest-tennis/blob/main/INSTALL.md).
