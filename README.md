# CandleWick

An interactive Android candle app built with **Kotlin** and **Jetpack Compose** featuring physics-based interactions, customizable styles, and purposeful modes.

## Features

* **Interactive Wick & Matchstick:** Tap the wick to toggle the flame, or extinguish it and relight it by swiping a matchstick across the strike strip and dragging the lit tip onto the wick.
* **Sensor & Microphone Physics:** Uses the accelerometer so the flame (and rising smoke) leans with device tilt, plus optional real-time local microphone blow detection (`RECORD_AUDIO`) to blow out the flame without recording or uploading audio.
* **Customizable Styles:** Switch between selectable candle themes (*Beeswax Pillar*, *Lavender Jar*, *Midnight Taper*, *Sage Wax*), flame colors (*Warm Gold*, *Emerald*, *Mystic Violet*, *Cobalt Blue*), and backdrop scenes (*Pitch Dark*, *Warm Room*, *Twilight Slate*).
* **Modes & Screen Options:** Choose from *Free Flame*, *Focus Timer* (wax melts as time runs down), *Sleep Dimmer* (gradual flame dimming), and *Wish Log*, along with a **Keep Screen Awake** toggle in the menu.

## Project Setup (Android Studio)

1. Open the project in **Android Studio** and set your unique `namespace` and `applicationId` in `app/build.gradle.kts` (replacing `com.example.candle`).
2. Ensure `app/build.gradle.kts` enables Compose (`buildFeatures { compose = true }`) and includes compatible Compose and test dependencies.
3. Keep `<uses-permission android:name="android.permission.RECORD_AUDIO" />` in `app/src/main/AndroidManifest.xml` (microphone access is only requested after showing an in-app explanation when the user opts in).
4. Connect an Android device via USB with **USB Debugging** enabled (or select an emulator) and press **Run**.

## Privacy

* All sensor, timer, wish-log, and blow-detection logic runs locally on the device.
* Microphone audio amplitude is evaluated temporarily in memory only when enabled and is never recorded, saved, or sent to a server.
