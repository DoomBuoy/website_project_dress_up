# Dressie website

The download page for the Dressie Android app. Plain HTML and CSS, no build step.
Hosted with GitHub Pages from the `main` branch.

## Releases are automatic
Every push to `main` in the app repository runs its "Build and publish APK" workflow, which:
- force-pushes the new `dressie.apk` to the `apk` branch of this repository, and
- updates `version.json` on `main` (build number, version, notes, APK link).

The page and the app's update check both read `version.json`. Do not edit it by hand.
