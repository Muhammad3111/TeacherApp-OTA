# TeacherApp OTA Bundles

This repository hosts JavaScript bundles for over-the-air (OTA) updates of the TeacherApp mobile application.

**Do not edit files here manually.** Bundles are generated and pushed automatically by the `npm run ota:release` script in the TeacherApp source repository.

## Structure

```
output/
  main.android.jsbundle   # Android JS bundle
  main.ios.jsbundle       # iOS JS bundle
  android-assets/         # Android image/font assets
  ios-assets/             # iOS image/font assets
```

## How it works

1. Developer runs `npm run ota:release "message"` in the TeacherApp repo
2. The script builds fresh bundles and pushes them to this repo's `main` branch
3. Users' installed apps fetch the latest bundle from here on next app launch
4. App restarts with the new JavaScript code — no Play Store / App Store update required

Source: https://github.com/Muhammad3111/TeacherApp
