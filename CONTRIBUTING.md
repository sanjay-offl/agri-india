# Contributing to Agri India

Thanks for your interest in improving Agri India! 🌾 This document explains how to propose changes.

## Code of conduct

Be respectful and constructive. This project aims to help farmers, so keep discussions focused and kind.

## Getting set up

See the **Getting Started** section of the [README](README.md). In short:

```bash
git clone https://github.com/sanjay-offl/agri-india.git
cd agri-india
echo "sdk.dir=$ANDROID_HOME" > local.properties
./gradlew assembleDebug
```

## Branching model

- `master` is the stable branch — never commit to it directly.
- Create a topic branch for your work:
  - `feature/<short-description>` — new functionality
  - `fix/<short-description>` — bug fixes
  - `chore/<short-description>` — tooling, docs, refactors

```bash
git checkout -b feature/weather-alerts
```

## Making a change

1. Keep changes focused — one feature/fix per pull request.
2. Match the existing Kotlin style (`kotlin.code.style=official`) and MVVM structure.
3. Build before pushing: `./gradlew assembleDebug`.
4. Write a clear commit message describing **what** changed and **why**.

## Pull requests

1. Push your branch and open a PR against `master`.
2. Fill in a short description, screenshots for UI changes, and the steps to test.
3. Link any related issue.

```bash
git push -u origin feature/weather-alerts
gh pr create --fill
```

## Reporting bugs

Open an issue with:

- Device/emulator and Android version
- Steps to reproduce
- Expected vs. actual behaviour
- Logcat output or screenshots if relevant

## Never commit

- `local.properties`
- `.idea/` files
- Private signing keystores
- Your personal `google-services.json` (see README for Firebase setup)
