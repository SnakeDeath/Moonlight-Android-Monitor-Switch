# Moonlight Android with Monitor Switch

> **This is NOT the official Moonlight app.** It is an unofficial, modified copy of
> [Moonlight Android](https://github.com/moonlight-stream/moonlight-android) that I edited
> for my own personal use. The only change is a floating button on the stream screen that
> switches the host between two monitors. It sends the Ctrl+Alt+Shift+F1/F2 shortcut that
> Sunshine already supports.
>
> All credit goes to the original authors of Moonlight and the Moonlight team. This project
> is licensed under the GNU GPL v3, the same as the original. See `LICENSE.txt`.
> Please don't report problems with this version to the official project.

---

## What I changed

A small draggable button appears on the stream screen. Tap it to switch the host between
monitor 1 and monitor 2, and drag it to move it out of the way.

* It works by pressing Ctrl+Alt+Shift+F1 (first display) or F2 (second display), which
  [Sunshine](https://github.com/LizardByte/Sunshine) already uses to switch the captured display.
  No changes to Sunshine are needed.
* The app can't ask the host which monitor is active, so it assumes the stream starts on the first one.
* The number of monitors is the `HOST_MONITOR_COUNT` constant near the top of
  `app/src/main/java/com/limelight/Game.java`.
* Only `Game.java` and `strings.xml` were changed.

---

# Original Moonlight Android README

[Moonlight for Android](https://moonlight-stream.org) is an open source client for NVIDIA GameStream and [Sunshine](https://github.com/LizardByte/Sunshine).

Moonlight for Android will allow you to stream your full collection of games from your Windows PC to your Android device,
whether in your own home or over the internet.

Moonlight also has a [PC client](https://github.com/moonlight-stream/moonlight-qt) and [iOS/tvOS client](https://github.com/moonlight-stream/moonlight-ios).

You can follow development on their [Discord server](https://moonlight-stream.org/discord) and help translate Moonlight into your language on [Weblate](https://hosted.weblate.org/projects/moonlight/moonlight-android/).

## Official Moonlight downloads
These links are for the official Moonlight app, not this modified version.

* [Google Play Store](https://play.google.com/store/apps/details?id=com.limelight)
* [Amazon App Store](https://www.amazon.com/gp/product/B00JK4MFN2)
* [F-Droid](https://f-droid.org/packages/com.limelight)
* [APK](https://github.com/moonlight-stream/moonlight-android/releases)

## Building
* Install Android Studio and the Android NDK
* Run ‘git submodule update --init --recursive’ from within moonlight-android/
* In moonlight-android/, create a file called ‘local.properties’. Add an ‘ndk.dir=’ property to the local.properties file and set it equal to your NDK directory.
* Build the APK using Android Studio or gradle

## Authors

* [Cameron Gutman](https://github.com/cgutman)  
* [Diego Waxemberg](https://github.com/dwaxemberg)  
* [Aaron Neyer](https://github.com/Aaronneyer)  
* [Andrew Hennessy](https://github.com/yetanothername)

Moonlight is the work of students at [Case Western](http://case.edu) and was
started as a project at [MHacks](http://mhacks.org).
