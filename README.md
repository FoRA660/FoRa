# Fora Music — Android project

Fora Music is a dark, Spotify-inspired Android music player starter project.

## Included
- Android app source in Kotlin + Jetpack Compose.
- Local audio import through Android's document picker.
- Playback using AndroidX Media3 / ExoPlayer.
- Search within the imported library.
- Mini-player with play/pause and seek-forward.
- Download button for direct HTTP(S) audio URLs (local files are already stored on the device).
- No subscription system and no advertising SDK.

## Important about music sources
This starter app does **not** scrape Spotify, YouTube, or other services and does not bypass DRM or download restrictions. Add audio files you own or have permission to use. For online playback/download, the app can be extended to use a licensed music catalog API or direct audio URLs whose provider explicitly permits streaming and downloading. The current local-library picker supports files on your device.

## Build an APK
1. Install Android Studio (current stable) and Android SDK Platform 35.
2. Open the `ForaMusic` folder in Android Studio.
3. Allow Gradle sync to finish. Use JDK 17 (Android Studio's bundled JBR is suitable).
4. Select **Build → Build Bundle(s) / APK(s) → Build APK(s)**.
5. Android Studio will show the APK location, normally `app/build/outputs/apk/debug/app-debug.apk`.

For a release APK: **Build → Generate Signed Bundle / APK → APK**, then create and securely store your own signing key.

## Project details
- Application ID: `com.foramusic.app`
- Minimum Android: Android 7.0 (API 24)
- Compile / target SDK: 35
- Kotlin + Jetpack Compose + Media3

## Current limitations
This is a buildable starter version, not a complete commercial streaming platform: it has no hosted catalog, user accounts, synced playlists, lyrics, or backend. Online catalog support requires a licensed provider and API credentials.


## Build APK using only an Android phone (GitHub Actions)

You can build the APK in the cloud from a phone; Android Studio is not required on the phone.

1. Sign in to GitHub in your phone browser and create a **new public or private repository** named `ForaMusic`.
2. Download and extract this ZIP. In the repository choose **Add file → Upload files** and upload the extracted project contents (including the hidden `.github` folder). If the mobile page hides hidden files, switch the browser to Desktop site or use GitHub's web upload page on a computer.
3. Commit the files to the `main` branch.
4. Open the repository's **Actions** tab. Select **Build Fora Music APK**, then **Run workflow** if it did not start automatically.
5. Wait for the workflow to finish successfully. Open the completed run, scroll to **Artifacts**, and download `Fora-Music-debug-APK`.
6. Extract the downloaded artifact ZIP and tap `app-debug.apk` to install. If Android asks, allow your browser/file manager to install apps from that source.

If the `.github` workflow folder was not uploaded, the Actions workflow will not appear. The APK is a debug build for testing; a release APK should be signed before public distribution.
