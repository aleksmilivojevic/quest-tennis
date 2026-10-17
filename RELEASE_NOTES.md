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
