# Les nombres 1–20: iOS app project

The app is the "Type it" web page in `www/index.html`, wrapped with Capacitor.
You need a Mac with Xcode and Node.js. An .ipa can only be built and signed on a Mac.

## Build steps
1. In this folder run:
   npm init -y
   npm install @capacitor/core @capacitor/cli @capacitor/ios
   npx cap add ios
   npx cap sync ios
   npx cap open ios
2. In Xcode: click the "App" target > Signing & Capabilities > choose your Apple ID team.
   Change the bundle identifier (com.albertting.frenchnumbers) if Xcode says it is taken.
3. Run on your iPhone or the simulator with the Play button.
4. To get the .ipa: Product > Archive, then Distribute App and pick the option that fits
   (Development or Ad Hoc for your own devices, App Store Connect to publish).

## Notes
- A free Apple ID can install on your own device for testing (the install expires after 7 days).
  Publishing on the App Store needs the paid Apple Developer Program.
- Apple may reject apps that are only a website in a wrapper, so add native value before submitting.
- The page loads its font from Google Fonts; offline it falls back to the system font.

Copyright © Albert Ting 2026.10
