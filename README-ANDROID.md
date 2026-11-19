# Poker Clock Android APK build

This Android project wraps the existing Poker Clock in a local Android WebView.
The timer HTML, styling, JavaScript and icons are bundled inside the APK, so it works offline and does not depend on GitHub Pages or a browser.

## Build the APK using GitHub Actions

1. Create a new GitHub repository (or use a separate branch/repository).
2. Upload the **contents** of this folder, keeping the `.github/workflows/build-apk.yml` file.
3. Open the repository's **Actions** tab.
4. Select **Build Poker Clock APK** and choose **Run workflow** (or wait for the push build).
5. When the run finishes, open it and download the artifact named **Poker-Clock-Android-APK**.
6. Extract the artifact ZIP. It contains `app-debug.apk`. Open that APK on your Samsung phone to install it. Android may ask you to allow installation from that source.

The APK is a debug-signed installable build. For personal use, that is sufficient; a release/store build would need a private signing key.

## App details

- Offline HTML is loaded from the APK's assets.
- JavaScript and local storage are enabled for the timer and saved reset buttons.
- Screen stays awake while the app is open.
- Supports portrait and landscape.
