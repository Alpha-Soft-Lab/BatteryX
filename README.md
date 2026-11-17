# BatteryX

A small native Android app that displays battery values reported by Android. It deliberately does **not** invent a battery-health percentage.

## What it reads
- Battery percentage, charging state, system battery-health status, temperature, voltage and battery technology from `ACTION_BATTERY_CHANGED`.
- Charge counter, instantaneous current, average current and energy counter from public `BatteryManager` properties when the device exposes them.

## Important limitation
Android's standard public battery APIs do not guarantee access to full-charge capacity, design capacity, state-of-health percentage or cycle count. This first build does not claim to read those values; it displays an unavailable message instead. The system status `Good` is not the same thing as 100% battery capacity.

## Build
Open this folder in Android Studio (JDK 17, Android SDK 35), let Gradle sync, then Build > Build Bundle(s) / APK(s) > Build APK(s). The resulting debug APK is under `app/build/outputs/apk/debug/`.

No permissions, internet access, root access, account or cloud service are used.
