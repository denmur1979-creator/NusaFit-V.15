# NusaFit V14.1 - Build fix

## Fix
- Added missing Android color resource `nf_red` (`#D32F2F`) to `app/src/main/res/values/colors.xml`.
- This resolves `Unresolved reference 'nf_red'` at `MainActivity.kt:629`, where code calls `color(R.color.nf_red)`.

## Validation
- Confirmed the referenced resource now exists in the resource XML and the Kotlin call matches its name.
- Full Gradle Release build/device testing was not run in this environment. Re-run GitHub Actions to verify the complete build and signing setup.
