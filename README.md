# KINOVA Android MVP

A starter Android app built with Kotlin, Jetpack Compose and AndroidX Media3.

## Included in v0.1
- Custom dark AMOLED-style interface
- Home, Anime, Movies, Series and Search tabs
- Demo content detail screen
- Embedded ExoPlayer demo playback
- GitHub Actions workflow that builds and uploads a debug APK

## Important content note
The catalog entries are placeholder demo data. The player uses Google's public Big Buck Bunny sample video to test playback. This project does not include MovieBox endpoints or copyrighted movie/TV/anime streams. Connect only metadata APIs and video sources you are authorized to use.

## Build in the cloud with GitHub Actions
1. Create a new empty GitHub repository named `KINOVA-Android`.
2. Upload the contents of this project folder to the repository root (not the ZIP file itself).
3. Make sure the default branch is named `main`.
4. Open the repository's **Actions** tab and enable Actions if prompted.
5. Open **Build KINOVA APK** and choose **Run workflow**, or push a commit to `main`.
6. When the workflow finishes, open the run and download the `KINOVA-debug-apk` artifact.
7. Extract the downloaded artifact ZIP. It contains `app-debug.apk`.

## Build locally (optional)
- Install Android Studio with Android SDK Platform 35 and JDK 17.
- Open this folder in Android Studio.
- Let Gradle sync finish.
- Run the `app` configuration on an Android device/emulator, or use Build > Build APK(s).

## Project structure

```text
KINOVA-Android/
├── .github/workflows/android.yml
├── app/
│   ├── build.gradle.kts
│   ├── proguard-rules.pro
│   └── src/main/
│       ├── AndroidManifest.xml
│       └── java/com/kinova/app/MainActivity.kt
├── build.gradle.kts
├── gradle.properties
└── settings.gradle.kts
```

## Next development phases
1. Replace placeholder catalog data with TMDB and AniList metadata clients.
2. Add persistent watchlist and history with Room.
3. Add backend account sync if required.
4. Add authorized HLS/DASH sources, subtitle selection and playback resume.
5. Add release signing and production build configuration.
