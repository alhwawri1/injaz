# INJAZ — Codemagic iOS IPA Package

Developed by **Al Hawari Al Naabi**.

## Contents
- `codemagic.yaml`: Codemagic iOS workflow (`ios-ipa-workflow`) using `npx cap sync ios` and `xcode-project build-ipa` to generate `*.ipa`.
- `capacitor.config.json`: Capacitor configuration for `com.alhawari.injaz` (`webDir: "www"`).
- `package.json`: Dependencies for `@capacitor/core` and `@capacitor/ios`.
- `www/index.html`: INJAZ web application connected to Supabase with iOS safe-area and home-screen icon metadata.
- `www/manifest.json` & `www/icons/*`: Web manifest and icon assets.

## How to Use in Codemagic
1. Upload this repository/folder to Git (GitHub / GitLab / Bitbucket) connected to Codemagic.
2. In Codemagic, configure iOS code signing (App Store Connect API key or manual `.p12` certificate + `.mobileprovision` profile) for bundle ID `com.alhawari.injaz`.
3. Run the `INJAZ iOS IPA Build` workflow to download the generated `.ipa` artifact and install via Sideloadly or your preferred signing tool.
