# Cone Player (Android)

A media player modeled on VLC, with an ad break after 1 hour of playback.
The app is the web player in `www/index.html`, wrapped as an Android app with Capacitor.

## Get the APK with no Android tools (GitHub builds it)
1. Create a free account at github.com and make a new empty repository (private is fine).
2. Upload everything in this folder to it, including the hidden `.github` folder.
3. Open the repository's **Actions** tab. The **Build APK** run starts by itself (about 5 minutes).
4. Open the finished run and download **ConePlayer-debug-apk** from the Artifacts section. Unzip it to get `app-debug.apk`.
5. Copy the APK to your phone and open it. Allow "Install unknown apps" when Android asks.

## Settings
- Ad interval and the Continue delay: `AD` at the top of the script in `www/index.html`.
- App name and ID: `capacitor.config.json`. Change `com.example.coneplayer` to your own ID before publishing.

## Before publishing on Google Play
- Debug APKs cannot be published. Create a signed release build (Android Studio: Build > Generate Signed Bundle).
- Real ads need an Android ad SDK such as AdMob, added with a Capacitor plugin. The current ad box is a placeholder.
