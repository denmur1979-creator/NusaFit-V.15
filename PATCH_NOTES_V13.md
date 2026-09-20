# NusaFit V13 follow-up patch

Based on the supplied NusaFit V12 ZIP.

## Changes
- Hardened GPS tracking service to ignore low-accuracy fixes (>50m) and implausible GPS jumps (>45m/s).
- Added asynchronous location-request failure handling and app-visible GPS error broadcasts.
- Persisted active/paused tracking flags consistently on service start and permission failure.
- MainActivity now listens for GPS service errors and shows a visible status/toast instead of leaving tracking marked active.
- Updated Android versionCode to 4 and versionName to 1.3.0.

## Verification limitation
- Source-level checks only. This environment does not have Gradle/Android SDK configured, so no APK build, emulator run, physical GPS test, or end-to-end UI test was performed.
- The supplied project still relies on a valid `GOOGLE_MAPS_API_KEY` GitHub Secret for Google Maps tiles, and runtime location permission plus device Location being enabled.
