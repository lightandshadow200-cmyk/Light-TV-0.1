# Light Aqua Launcher 0.1

A lightweight Android launcher with an Apple TV-inspired *dark navy, large hero panel, and app tiles* layout. It is an original design and does not use Apple assets.

## Targets
- Android phones/tablets: standard launcher entry
- Android TV: Leanback launcher entry
- Full Android watches: compact layout when the screen is narrow

## Build in AndroidIDE
1. Extract this ZIP to a folder such as `Download/Light_Aqua_Launcher`.
2. In AndroidIDE, use **Open** / **Import project** if available and select the extracted project folder (the folder containing `settings.gradle`).
3. Allow Gradle sync. This project uses Android Gradle Plugin 8.6.1, Kotlin 2.0.20, compile SDK 35.
4. Build the debug APK from the Build menu / Gradle task `:app:assembleDebug`.
5. APK output: `app/build/outputs/apk/debug/app-debug.apk`.

## Install and select
- Install the APK on the target device.
- Press Home. If Android asks which Home app to use, select **Light Aqua Launcher**. Choose **Always** only if you want it as default.
- On Android TV, remote navigation support depends on the device firmware; the tiles are focusable.
- On watches, this is intended for *full Android*, not Wear OS. Some watch firmware blocks replacement of the system launcher.

## Notes
- This ZIP is source code, not a ready-to-install APK.
- First build requires internet access to download Gradle dependencies.
- This is a starter project, not a full streaming service: the hero card opens the first available supported video app.
