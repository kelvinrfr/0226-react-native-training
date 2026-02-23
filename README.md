# Setting up instructions

This guide helps you set up your Mac **before** the lecture so we can create and run a first React Native app with **Expo** on the **iOS Simulator**.

Allow **about 30–45 minutes** for a full install if you are starting from scratch (Xcode takes the longest).

---

## 1. Node.js

- **Required:** Node **18.0.0 or newer** (LTS recommended, 22.x is fine).
- Install via [Homebrew]([https://brew.sh/](https://brew.sh/)): `brew install node`
- **Check:** `node -v` and `npm -v`

## 2. Homebrew (if not installed)

- Install: [[https://brew.sh](https://brew.sh)]([https://brew.sh](https://brew.sh))
- **Check:** `brew --version`

## 3. Watchman (recommended)

- `brew install watchman`
- Improves file-watching performance during development.

## 4. Xcode (required for iOS Simulator)

- Install **Xcode** from the **Mac App Store** (large download, ~12 GB+).
- After installation:
  - Open **Xcode**.
  - Go to **Xcode → Settings… (or Preferences…) → Locations**.
  - Set **Command Line Tools** to the latest version (e.g. "Xcode 16.x").
- **Simulator:** In **Xcode → Settings → Platforms**, add an **iOS** simulator version if needed.
- **Check:** Open Xcode once and accept the license if prompted.

## 5. Expo Go (optional – physical device only)

- If you want to test on a **real iPhone**, install **Expo Go** from the App Store.
- For the simulator, Expo Go is **not required**.

## 6. Install the Expo CLI

```bash
npm install -g expo-cli
```

Or use `npx` directly without a global install (shown in verification below).

---

## Quick verification before the lecture

```bash
node -v          # 18.x or higher
npm -v
watchman -v
xcodebuild -version
npx expo --version
```

Then create a project and run it:

```bash
npx create-expo-app AwesomeProject
cd AwesomeProject
npx expo start
# Press i to open the iOS Simulator
```

---

## What we'll do in the lecture

1. Create a new app: `npx create-expo-app AwesomeProject`
2. Start the dev server: `npx expo start` (keep it running)
3. Press **`i`** in the terminal to launch the iOS Simulator
4. Make a small change in `app/index.tsx` (or `App.tsx`) and see it reload instantly.

---

## If something doesn't work

- **Official setup:** [Expo – Get started]([https://docs.expo.dev/get-started/introduction/](https://docs.expo.dev/get-started/introduction/))
- **Install Expo Go:** [[https://expo.dev/go](https://expo.dev/go)](https://expo.dev/go]\(https://expo.dev/go\))
- **Troubleshooting:** [Expo – Common issues]([https://docs.expo.dev/troubleshooting/overview/](https://docs.expo.dev/troubleshooting/overview/))

---

## Summary checklist

| Step                                     | Done |
| ---------------------------------------- | ---- |
| Node 18+                                 | X    |
| Homebrew                                 | X    |
| Watchman                                 | X    |
| Xcode + Command Line Tools               | ☐ ~~ |
| Expo CLI (`npm install -g expo-cli`)     | ☐    |
| Expo Go (optional, physical device only) | ☐    |

After completing the checklist, run the verification commands and try creating `AwesomeProject` with `npx create-expo-app`. If it launches in the iOS Simulator with **`i`**, you're ready for the lecture.