# JARVIS Android starter (v0.1)

This is a native Kotlin Android Studio starter project, configured for Android 6.0+ and targeting Android 11-era behavior.

## Included in this prototype
- JARVIS-style dark voice-console screen
- UK English Android text-to-speech voice (voice availability depends on installed Android TTS voices)
- Tap-to-start speech recognition; recognizes the phrase "Hey Jarvis" while the app is active
- Opens YouTube, WhatsApp, Instagram and Android Settings
- Web search
- Prepares an SMS in the system messaging app; the user reviews and sends it

## Important limitations
- This is **not an APK**. The build environment used to prepare this project does not contain the Android SDK/Gradle, so an APK could not be compiled or tested here.
- Wake-word listening is active only while this app is open and START LISTENING is enabled. It does not listen continuously in the background or while the phone is locked.
- Android's standard speech recognizer may use the device's speech service/network and its own language settings.
- This prototype does not perform secure speaker verification. A spoken wake phrase alone is not proof of identity.
- Sending messages, placing calls, changing secure settings, or executing consequential commands should require review/confirmation and Android permissions.

## Build the APK
1. Install Android Studio on a computer.
2. Open this `JarvisAndroid` folder.
3. Let Android Studio install the Android Gradle Plugin/SDK components it requests (compile SDK 35).
4. Connect an Android phone with USB debugging enabled, or use an emulator.
5. Select **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
6. Android Studio will show the generated APK location. Install it on your phone and grant microphone permission.

## Next engineering milestones
1. Add a foreground microphone service and a dedicated offline wake-word engine for background wake detection (with a persistent notification and battery-use controls).
2. Add enrolled speaker verification as a convenience gate; do not use it as the sole security control.
3. Add explicit confirmation flows for calls/messages and per-action permissions.
4. Add a configurable command router, contact picker, and app list.
