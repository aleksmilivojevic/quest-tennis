# Install On Your Quest

You need a Quest, both Touch controllers, a USB **data** cable and a Windows,
macOS or Linux computer for the USB installation route below.

## 1. One-Time Headset Setup

Follow [Meta's device setup guide](https://developers.meta.com/vr/documentation/native/android/mobile-device-setup/)
to register/verify your developer account, join or create a developer team, and
enable **Developer Mode** for your paired headset in the Meta Horizon phone app.
Windows may also need the Meta Quest ADB driver linked from that guide.

Connect the headset to your computer and put it on. Accept **Allow USB debugging**
inside the **headset**, not on the computer. Only select "Always allow" for a
computer you trust. A file-access prompt is not the USB-debugging prompt.

## 2. Download

Get **quest-tennis.apk** from the
[preview release](https://github.com/aleksmilivojevic/quest-tennis/releases/tag/v0.1.0-preview.1).
Alternatively, extract **quest-tennis-sideload.zip**; the APK is inside.
Do not use GitHub's "Source code (zip)" download as the game installer.

## 3A. Install With A Desktop GUI

Use [SideQuest's desktop installer](https://sidequestvr.com/setup-howto) with
local APK installation support (called the Advanced Installer in older versions).
Once it shows your headset connected and authorized, choose **Install APK** and
select `quest-tennis.apk`. Wait for its task to report successful installation.
If your version has no APK install action, use the ADB route below.

Do not simply drag the APK into the headset's Downloads folder. Do not install
another app with a similar name; use the APK linked from this repository.

## 3B. Install With ADB Instead

Download and extract Google's official
[Android SDK Platform Tools](https://developer.android.com/tools/releases/platform-tools).
Put `quest-tennis.apk` in the extracted `platform-tools` folder and open a terminal there.
Connect just the Quest you intend to update; disconnect other Android devices.

macOS / Linux:

```sh
./adb devices
./adb install --no-incremental -r quest-tennis.apk
```

Windows PowerShell:

```powershell
.\adb.exe devices
.\adb.exe install --no-incremental -r .\quest-tennis.apk
```

The device list must show one row ending in `device`, not `unauthorized` or
`offline`. Stop and resolve authorization/connection problems before installing.
Successful installation prints `Success`. See [Meta's ADB guide](https://developers.meta.com/vr/documentation/native/android/ts-adb/).

The `-r` option updates a matching signed installation while retaining app data.
There is no need to uninstall first. A different signing key can cause
`INSTALL_FAILED_UPDATE_INCOMPATIBLE`; do not uninstall casually, because that
deletes saved settings. Ask the maintainer which build you have before proceeding.

## 4. Open And Play

Wake the headset and both controllers. In the headset's app library, select
**Unknown Sources** (the filter location varies by Horizon OS version) and open
**Quest VR Game**. That is this APK's installed name, despite this repo being
called Quest Tennis. If prompted that controllers are required, press a button
on each controller and choose **Continue / Open**.

Stand safely behind the virtual baseline, then swing the racket at incoming
balls. Point at the front-left panel for machine settings, front-right for court
and lighting, or turn around for racket angle calibration. Trigger clicks operate
the buttons. Feeds pause when the headset loses focus or the racket is untracked.

## Troubleshooting

- No device or no prompt: use a data-capable cable, try another USB port, check Developer Mode, and reconnect while wearing the headset.
- Device busy: close other sideloading tools or browser tabs connected to Quest USB, then reconnect. Do not run multiple USB tools at once.
- APK certificate/parse error: redownload from the release and compare its checksum. Do not repackage, edit, or resign the APK.
- Installed but cannot find it: look for **Quest VR Game** under Unknown Sources, not "Quest Tennis" in the store.
- Black screen or controller prompt: wake both controllers, complete the system dialog, and keep the headset awake. Report persistent failures.
- Night still shimmers: report the venue, lighting mode and whether it occurs during head movement. This fix is not yet hardware-accepted.

## Optional Download Integrity Check

Compare the result below with `SHA256SUMS.txt` in the release. This verifies
download integrity, not hardware compatibility or an independent security audit.

```sh
# macOS
shasum -a 256 quest-tennis.apk
# Linux
sha256sum quest-tennis.apk
```

```powershell
# Windows
Get-FileHash .\quest-tennis.apk -Algorithm SHA256
```
