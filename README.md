# NIGHTFALL: LAST NIGHT -> Android APK

Single-file HTML game (www/index.html). Capacitor project is already configured.

## Build (Android Studio installed, Node 18+)
    npm install
    npx cap add android
    npx cap sync android
    npx cap open android      # then Build > Build APK(s)
Or from the command line: cd android && ./gradlew assembleDebug
APK: android/app/build/outputs/apk/debug/app-debug.apk

## Quick alternative (no Android Studio)
Host the www/ folder on any HTTPS site, then use https://www.pwabuilder.com to generate the Android package.

## Important
- Solo practice works fully offline inside the APK.
- Room multiplayer uses claude.ai's built-in room feature (window.claude). It is NOT available inside an APK, so multiplayer needs a different backend (Supabase / WebSocket server) before it works there.
- Add android:screenOrientation if you want to lock orientation; audio needs a first tap (already handled).
