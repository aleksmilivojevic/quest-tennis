# Quest Tennis

A standalone VR tennis practice prototype for Meta Quest. Hit balls from an
adjustable ball machine on a club, mountain, forest, or New York rooftop court.

## Gameplay Video

**[Download the gameplay demo (MP4, 1080p)](https://github.com/aleksmilivojevic/quest-tennis/releases/download/gameplay-demo-2026-10-22/tennis-gameplay-demo-edited.mp4)**

[Video details](https://github.com/aleksmilivojevic/quest-tennis/releases/tag/gameplay-demo-2026-10-22).

## Download And Play

**[Download the APK](https://github.com/aleksmilivojevic/quest-tennis/releases/download/v0.1.0-preview.1/quest-tennis.apk)**

[Download the complete sideload bundle](https://github.com/aleksmilivojevic/quest-tennis/releases/download/v0.1.0-preview.1/quest-tennis-sideload.zip)
includes the same APK, instructions, checksum, build details, and license notices.
No Godot, Android Studio, project checkout, or game compilation is needed.

1. Set up USB sideloading on your Quest: Developer Mode and USB debugging authorization.
2. Install `quest-tennis.apk` using a desktop APK installer or ADB.
3. In your headset, open **Library / Applications > Unknown Sources > Quest VR Game**.
4. Wake both Touch controllers and choose **Continue / Open** if Quest asks for controllers.

**[Step-by-step installation](INSTALL.md)** | [Release notes](RELEASE_NOTES.md)

Use the **Install APK** action, not a file-transfer action. Downloading or copying
an APK onto the headset does not install it. GitHub's automatically generated
"Source code" downloads contain this documentation, not the game.

## What You Can Test

- Tennis ball and moving-racket contact physics with repeated machine feeds.
- Front-left machine controls: height, aim, elevation, speed, release interval and pause.
- Rear racket controls: pitch, yaw and roll calibration.
- Front-right court and day/night controls, including a surrounding New York skyline.
- Saved settings on your own headset. Point either controller at a button and squeeze/release its trigger.

## Preview Status

This is an early **practice prototype**, not a scored match or finished game.
Quest 2 is the development target; other Quest models are not yet validated.
Touch controllers are required; hand-only input is not supported.
The included build is debug-signed and intended for sideloaded testing, not store distribution.

The latest build passed automated desktop checks and APK signature verification
and was installed on Quest 2. Its final VR startup check stopped at the headset's
controllers-required dialog; night-shimmer improvements still need in-headset
confirmation. Prior builds had working court controls and racket contacts.

Keep a clear play area, use controller wrist straps, and respect the Quest boundary.
The virtual court is not an instruction to run across your physical room.

## Feedback And Notices

[Report a problem](https://github.com/aleksmilivojevic/quest-tennis/issues) with the
headset model, release tag, selected court, day/night setting, and reproduction steps.
Do not post device serial numbers, account details, or complete system logs publicly.

This repository contains downloads and setup documentation, not the development
workspace. [Third-party notices](THIRD_PARTY_NOTICES.md) cover the bundled engine
and libraries. This is an independent prototype, not a Meta or Eleven Table Tennis product.
