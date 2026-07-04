# Nexus Keyboard

A clone-ready Android keyboard starter built for a Samsung/Gboard-style feel, with:
- offline typing
- persistent clipboard history
- theme settings
- delete-repeat speed control
- modifier key visibility and behavior settings

## What is included
- `InputMethodService` keyboard
- settings screen
- persistent clipboard store
- light / dark / AMOLED themes
- qwerty and symbols keyboard layouts

## Termux build notes
This project is designed to be edited in Termux, but Android builds still require the Android SDK.

Install the basics in Termux:
```bash
pkg update && pkg upgrade -y
pkg install git openjdk-21 gradle unzip zip -y
```

Then build:
```bash
chmod +x gradlew
./gradlew assembleDebug
```

If your environment does not have the Android SDK configured yet, set up `ANDROID_HOME` / `ANDROID_SDK_ROOT` first and install the required platform and build tools.

## Repo layout
- `app/src/main/java/...` — Kotlin source
- `app/src/main/res/layout` — UI layouts
- `app/src/main/res/xml` — IME metadata
- `app/src/main/res/values` — strings, colors, themes

## Notes
- Clipboard history is stored locally and does not expire by default.
- The keyboard is fully offline.
- This is a starter project, not a copy of Samsung Keyboard or Gboard.


The keyboard toolbar includes quick access to clipboard, emoji, layout switching, and settings.
