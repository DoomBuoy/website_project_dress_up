# Dressie website

The download page for the Dressie Android app (source: https://github.com/DoomBuoy/Project_dress_up).
Plain HTML and CSS, no build step. Hosted with GitHub Pages from the `main` branch.

## Releasing a new app version
1. In the app: raise `version:` in `pubspec.yaml` and `appVersion` / `appBuild` in
   `lib/features/update/update_check.dart`.
2. Build: `flutter build apk --release --target-platform android-arm64`.
3. Copy `build/app/outputs/flutter-apk/app-release.apk` to `downloads/dressie.apk` here.
4. Update `version.json` (`build` must match `appBuild`) and push.

The app reads `version.json` from this repository when it opens and tells people when `build` is higher than
their own.
