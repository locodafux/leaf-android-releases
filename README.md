# Leaf Android releases

Public download location for Leaf's Android APK updates. The Leaf source repository remains private.

The app reads `latest.json` from this repository's `main` branch and installs the APK attached to the referenced GitHub release. Only publish APKs that use package ID `com.leaf.reader`, have a higher Android `versionCode`, and are signed with the same certificate as the previously distributed Leaf APK. Android rejects in-place updates signed by a different certificate.

Release steps:

1. Build and sign the APK from the private Leaf source repository.
2. Create a GitHub release here and attach the APK as `leaf-VERSION.apk`.
3. Update `latest.json` with the new version and the release download URL, then commit it to `main`.

The manifest URL is `https://raw.githubusercontent.com/locodafux/leaf-android-releases/main/latest.json`.
