<div align="center">

# 🌾 Agri India

**A single Android app that brings India's farmers everything they need — in one place.**

[![Platform](https://img.shields.io/badge/Platform-Android-3DDC84?logo=android&logoColor=white)](https://developer.android.com)
[![Language](https://img.shields.io/badge/Kotlin-1.3.72-7F52FF?logo=kotlin&logoColor=white)](https://kotlinlang.org)
[![Backend](https://img.shields.io/badge/Backend-Firebase-FFCA28?logo=firebase&logoColor=black)](https://firebase.google.com)
[![Min SDK](https://img.shields.io/badge/minSdk-21-blue)](https://developer.android.com)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

<img src="Agri%20India.png" alt="Agri India app design" width="720" />

</div>

---

## 📖 About

Indian farmers juggle multiple apps and accounts to get basic information and services. Agri India combines
every useful feature into a **single, easy-to-use application**, so a farmer can check market prices, read
government schemes, buy supplies, forecast weather and connect with a community — without switching apps.

> The technology has become part and parcel of everyone's life and is helping us make daily tasks easy.
> We identified that in the agriculture sector, farmers are still lacking the best technology use cases, so
> we built Agri India as a one-stop solution.

## ✨ Features

| Feature | Description |
| --- | --- |
| 🏛️ **Government Yojna Awareness** | Browse government schemes and their details |
| 🛒 **E-commerce Platform** | Shop farming products, manage a cart and place orders |
| 📈 **Daily APMC Price Updates** | Live mandi/market prices by state and district |
| 👥 **Community Network** | A social feed to create posts and engage with other farmers |
| 📰 **Articles** | Read agriculture articles by category |
| 🌦️ **Weather Forecasting** | Current conditions and forecast for your location |
| 👤 **User Accounts** | Sign up / sign in, profile and order history |

## 🛠️ Tech Stack

| Layer | Tools |
| --- | --- |
| **Language** | Kotlin |
| **Platform** | Android (minSdk 21, targetSdk 29) |
| **Build** | Gradle 6.1.1 · Android Gradle Plugin 4.0.1 |
| **Backend** | Firebase — Auth, Firestore, Realtime Database, Storage |
| **Networking** | Retrofit + Gson · Kotlin Coroutines |
| **Architecture** | MVVM — AndroidX ViewModel + LiveData, Kodein DI, Room |
| **UI** | AndroidX, Material Components, Data Binding, Navigation, ViewPager carousel |
| **Payments** | Razorpay |

## 📂 Project Structure

```
Farming-App/
├── app/
│   └── src/main/
│       ├── java/com/project/farmingapp/
│       │   ├── adapter/       # RecyclerView adapters (APMC, cart, weather, posts…)
│       │   ├── model/         # Repositories + API data classes
│       │   ├── utilities/     # Helpers and click listeners
│       │   ├── view/          # Screens grouped by feature
│       │   │   ├── apmc/  articles/  auth/  dashboard/  ecommerce/
│       │   │   ├── introscreen/  socialmedia/  user/  weather/  yojna/
│       │   └── viewmodel/     # Feature ViewModels
│       └── res/               # Layouts (40+), drawables, menus, values
├── gradle/wrapper/            # Gradle wrapper
├── build.gradle               # Root build config
└── settings.gradle
```

## 🚀 Getting Started

### Prerequisites

- [Android Studio](https://developer.android.com/studio) 4.x or newer
- JDK 8
- A Firebase project (for Auth / Firestore / Storage features)

### Build & run

```bash
git clone https://github.com/sanjay-offl/agri-india.git
cd agri-india

# Point Gradle at your local Android SDK
echo "sdk.dir=$ANDROID_HOME" > local.properties

./gradlew assembleDebug      # build the debug APK
# or open the project in Android Studio and press Run
```

### Firebase setup

The app reads Firebase config from `app/google-services.json`. To run against **your own** Firebase project:

1. Create a project at [console.firebase.google.com](https://console.firebase.google.com).
2. Add an Android app with package name `com.project.farmingapp`.
3. Download the generated `google-services.json` and replace `app/google-services.json`.
4. Enable **Authentication**, **Cloud Firestore**, **Realtime Database** and **Storage**.

## 🌿 Git Workflow

Feature work happens on topic branches, e.g. `apmc`, `weather`, `ecommerce`, `social-media`,
`user-authentication`, `dashboard`, `articles`, `introscreen`. Merge into `master` via pull request.

```bash
git checkout -b my-feature
# … commit your changes …
git push -u origin my-feature
gh pr create --fill
```

## 🤝 Contributing

Contributions are welcome! Please read [CONTRIBUTING.md](CONTRIBUTING.md) before opening a pull request.

## 📄 License

Released under the [MIT License](LICENSE).

## 🙏 Credits

Originally created by **[Het Suthar](https://github.com/hetsuthar028)**. Maintained at
[sanjay-offl/agri-india](https://github.com/sanjay-offl/agri-india).

---

<div align="center">

**If you find this project useful, please give it a ⭐ and fork the repository.** 🌱

</div>
