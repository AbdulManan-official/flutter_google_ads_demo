# Flutter Google Ads Demo

A Flutter demo app demonstrating **Google Mobile Ads integration** including **Banner Ads**, **Interstitial Ads**, and **Rewarded Ads**.
This project also includes smooth UI animations, a counter system, and reward points for rewarded ads. Perfect for learning monetization in Flutter apps.

---

## 🚀 Features

* Banner Ad implementation
* Interstitial Ad shown automatically after every 5 taps
* Rewarded Ad with bonus points
* Smooth UI animations using `AnimationController`
* Easy to customize and extend
* Test ads for safe testing

---

## 📦 Project Structure

```
flutter_google_ads_demo/
├─ lib/
│  ├─ main.dart       # Main app with ads integration
├─ android/
│  ├─ app/src/main/AndroidManifest.xml  # AdMob App ID configuration
├─ pubspec.yaml       # Flutter dependencies
```

---

## 🛠 Prerequisites

* Flutter SDK installed
* Android Studio / VS Code
* Basic knowledge of Flutter widgets and animations

---

## ⚡ Step 1: Create New Flutter Project

```bash
flutter create flutter_google_ads_demo
cd flutter_google_ads_demo
```

---

## ⚡ Step 2: Add Dependencies

Open `pubspec.yaml` and add:

```yaml
dependencies:
  flutter:
    sdk: flutter
  google_mobile_ads: ^5.0.0
```

Then run:

```bash
flutter pub get
```

---

## ⚡ Step 3: Configure AndroidManifest.xml

Open `android/app/src/main/AndroidManifest.xml` and add the AdMob App ID **inside the `<application>` tag**:

```xml
<meta-data
    android:name="com.google.android.gms.ads.APPLICATION_ID"
    android:value="ca-app-pub-3940256099942544~3347511713"/>
```

> This is a **test AdMob ID**. Replace it with your own when publishing.

---

## ⚡ Step 4: Initialize Google Mobile Ads

In `lib/main.dart`:

```dart
void main() async {
  WidgetsFlutterBinding.ensureInitialized();
  await MobileAds.instance.initialize();
  runApp(const MyApp());
}
```

---

## ⚡ Step 5: Implement Banner, Interstitial, and Rewarded Ads

* **Banner Ad:** Displayed at the bottom using `BannerAd` + `AdWidget`
* **Interstitial Ad:** Loaded and shown after every 5 taps
* **Rewarded Ad:** Gives bonus points to users

All implemented in `main.dart`.

---

## ⚡ Step 6: Add UI Animations

* Tap counter button with scale animation
* Rotating number animation
* Pulsing “Tap Me” button
* Gradient and shadow effects for UI cards

---

## ⚡ Step 7: Running the App

1. Connect your Android device / emulator
2. Run:

```bash
flutter run
```

3. Tap the button to see interstitial ads every 5 taps
4. Watch rewarded ads to earn bonus points

---

## 📁 Step 8: Create GitHub Repository

1. Go to GitHub → New Repository → Name: `flutter_google_ads_demo`
2. Initialize locally:

```bash
git init
git add .
git commit -m "Initial commit: Google Ads Demo"
git branch -M main
git remote add origin https://github.com/yourusername/flutter_google_ads_demo.git
git push -u origin main
```

---

## 🧩 Customization

* Replace test Ad Unit IDs with your real AdMob IDs
* Change counter logic or animations
* Add more UI components or tabs

---

## 📌 Notes

* Uses **test AdMob IDs** – do not click real ads during testing
* Compatible with Flutter 3.10+ and Android 10+
* Reward points are just for demo purposes

---

## 🏷 Tags

#Flutter #GoogleAds #MobileDevelopment #Dart #AdMob #FlutterDev #AppMonetization

---

## 📄 License

This project is **MIT Licensed** – feel free to use and modify.

---
