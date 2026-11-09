# Publishing an Android release

GitHub Releases in this repository distribute **Android APKs only**. The browser
extension is distributed through the Chrome Web Store and is never attached to a
release. There is no workflow: the APK is built and signed locally from the
`prizo Android` repository (the signing key lives only on the owner's machine), so a
CI job would need the keystore as a secret for no gain. Publishing is one command.

## Naming

- Tag: `android-v<versionName>` (for example `android-v1.0.3`), matching the tags in the
  Android repository. The existing `v1.0.0` tag and release are historical and stay.
- Title: `پرایزو اندروید <versionName>`
- Asset: `prizo-android-<versionName>.apk`

## Steps

1. In the Android repository, bump `versionCode` and `versionName` in `app/build.gradle.kts`
   and build with `./gradlew :app:assembleRelease`. `keystore.properties` must be present;
   without it the build is unsigned and Android refuses to install it.
2. Verify the APK before uploading:
   ```bash
   BT=~/Android/Sdk/build-tools/36.1.0
   $BT/apksigner verify --print-certs prizo.apk   # must print Verifies
   $BT/aapt2 dump badging prizo.apk | head -1      # package ir.prizo.android, expected versionCode/versionName
   ```
   The certificate SHA-256 must be
   `c7ff6e6ed4176450212ade0a11efd528eb923718d6222ffcc1ce5240d208f6a0` (the key of every APK
   published so far). A different key cannot update installed copies.
3. Write the release notes in Persian (see the template), then publish:
   ```bash
   cp prizo-<...>.apk prizo-android-1.0.3.apk
   gh release create android-v1.0.3 prizo-android-1.0.3.apk \
     --repo zanasaed/prizo-extension --target main \
     --title "پرایزو اندروید ۱.۰.۳" --notes-file notes.md --latest
   ```

## Release notes template (`notes.md`)

Only changes a user can see. No internal ids, no commit hashes.

```markdown
## تغییرات این نسخه

- <تغییر اول>
- <تغییر دوم>

## نصب

۱. فایل `prizo-android-<نسخه>.apk` را از بخش Assets همین صفحه دانلود کنید.
۲. فایل را باز کنید و اگر اندروید خواست، اجازهٔ نصب بدهید.
۳. اگر نسخهٔ قبلی نصب است، همین فایل روی آن نصب می‌شود و اطلاعاتتان می‌ماند.

نیازمند اندروید ۱۰ یا بالاتر.

SHA-256: `<hash>`
```

Notes for 1.0.3 (from the Android repository's `v1.0.3.md`):

- خروج از پرایزو و بازگشت به آن در اندروید ۱۶ اصلاح شد.
- نمایش کمترین قیمت ۳۰ روز اخیر در صفحه‌های بعدی دسته‌بندی‌ها و برندها اصلاح شد.

## Things to know

- The extension and Android releases are independent. The Android release is a normal GitHub
  Release and may be marked Latest; its `android-v…` tag scheme does not interact with extension versions.
- Do not attach `.zip`/`.xpi` extension packages to releases.
- `src/data/gadget-store-config.json` is fetched by the extension from `main` at runtime.
  Do not move or delete it.
