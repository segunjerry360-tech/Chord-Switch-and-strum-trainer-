# Chord Switch and Strum Trainer — Android build pack

This repository pack contains the supplied HTML trainer and the files needed to build it as an Android APK with GitHub Actions.

## Files

- `index.html` — the original supplied trainer HTML (renamed only; its contents are unchanged).
- `assets/icon.png` — the supplied app icon converted to a genuine PNG for Android icon generation.
- `package.json` — pinned Capacitor dependencies.
- `capacitor.config.json` — Android app identity and web directory.
- `.github/workflows/build.yml` — GitHub Actions APK build.

## Create the GitHub repository

1. Create a new repository named `chord-switch-strum-trainer`.
2. Set it to **Private**.
3. Add the files and folders from this ZIP to the repository root. Keep the `.github/workflows/build.yml` path exactly as shown.
4. Use the `main` branch.
5. You do not need to add a README, licence, or `.gitignore` separately; this pack already includes a README.

## Get the APK

After uploading the files, open the repository's **Actions** tab.
Open the workflow named **Build Chord Switch Trainer APK**.
When the run finishes successfully, open that run and download the artifact named `chord-switch-strum-trainer-apk`. It contains `app-debug.apk`.

The first build may take several minutes. A successful workflow run is required before an APK exists.

## Build configuration

The project uses Capacitor 6.2.1, Node.js 20 and Java 17. The workflow creates the Android project during the build, generates launcher icons from `assets/icon.png`, and builds a debug APK.

The workflow has not been executed in this pack-generation step. The APK is therefore not yet built or tested on a device.
