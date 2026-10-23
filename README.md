# Light TV 0.1 — Android TV Launcher

A starter Android launcher with a minimalist, Apple TV-inspired dark interface. This is an installable **launcher app**, not a replacement Android operating system or Apple software.

## Features
- Home screen branded Light TV 0.1
- D-pad / remote focus and OK/Enter activation
- Opens supported installed apps (YouTube TV, Netflix, Prime Video, Disney+, Spotify when present)
- App list discovered from launchable packages
- Opens Android system Settings
- Home/launcher intent filters so Android may offer Light TV as a home app

## Build with Android Studio
1. Install Android Studio (current stable) and its Android SDK Platform 35.
2. Extract this folder and open `LightTV01` in Android Studio.
3. Allow Gradle sync. Use JDK 17 if prompted.
4. Select **Build > Build APK(s)**.
5. The debug APK is normally written to `app/build/outputs/apk/debug/app-debug.apk`.

## Install on a TV
- For a TV with USB debugging enabled, connect using ADB and run:
  `adb install -r app/build/outputs/apk/debug/app-debug.apk`
- Or copy the APK to the TV and install it if the device permits sideloading.
- Press Home and choose **Light TV** if the system displays a home-app chooser. TV manufacturers may restrict changing the default launcher.

## Notes / limitations
- Source project is provided; an APK is not prebuilt here because Android SDK/Gradle build tools are not available in this environment.
- The layout is a functional starter UI, not yet a polished production launcher. Some app package IDs vary by region/device; missing apps are simply omitted from the home row.
- Android 11+ package visibility is declared to let the launcher discover installed apps. Review Google Play policy requirements before publishing.
- Branding uses a generic circle mark to avoid bundling Apple's trademark logo. The visual direction is inspired by minimalist streaming interfaces, not affiliated with Apple.

## Build using only an Android phone (GitHub Actions)

This repository includes `.github/workflows/android.yml` so the APK can be built on GitHub's cloud runner without installing Android Studio on your phone.

1. Create a repository on GitHub and upload the **contents** of this project (keep the `app/`, `gradle.properties`, `settings.gradle.kts`, `build.gradle.kts`, and `.github/workflows/android.yml` paths intact). The project root must contain `settings.gradle.kts` and `app/`.
2. Open the repository on GitHub in your phone browser. Go to **Actions** and select **Build Light TV APK**. If prompted, enable Actions, then tap **Run workflow**.
3. Wait for the workflow run to finish with a green check.
4. Open that run, scroll to **Artifacts**, and download `LightTV01-debug-apk`. Extract the downloaded ZIP to get `app-debug.apk`.
5. Copy the APK to the TV (USB drive, local network, or a trusted file-transfer method), then open it on the TV and allow installation from that source if Android asks. Only install APKs you built or trust.

The workflow builds a **debug APK**. It has not been tested on your particular TV. Some TV manufacturers restrict third-party launchers or changing the default Home app.
