# ClassicForever Android

An app for running World of Warcraft on Android ARM64 devices, with graphics support for Mali/PanVK and Adreno/Turnip.

This is the public **documentation and releases** repository. Selected APK builds are published here.

## Downloads

The first public version is **[0.0.1](https://github.com/apazosg/ClassicForever-android/releases/tag/v0.0.1)**. Download its APK from [Releases](https://github.com/apazosg/ClassicForever-android/releases).

Each release describes its changes, version-specific instructions, and known limitations. New releases are published when we decide a version is ready to share.

See the [version numbering and release notes format](docs/releases.md). Starting with `0.0.1`, the app notifies you about new versions published here and lets you read their release notes and download updates. You can also check manually under **Settings → Check for app updates**, even if you have not installed the game.

## Features

- **In-app game installation**, with an initial client download and progressive game data downloads while you play.
- **Reuse an existing installation** by selecting its folder or copying its files from a computer.
- **Game client updates** directly from the launcher.
- **Mali/PanVK and Adreno/Turnip graphics support**, depending on device compatibility. No root required.
- **Account and saved credential management**, with passwords encrypted using Android Keystore and controls to set, update, or delete them.
- **Region selection and 720p or 1080p resolution**.
- **Gamepads, on-screen controls, and the Android keyboard** during gameplay.
- **Performance overlay and diagnostic tools** accessible from the in-game menu.

The availability of a feature does not guarantee compatibility with every device or client version. Check the test results below and the release notes for the APK you install.

## Screenshots

### Game installation

![Game installation screen showing download progress and quick resolution settings](docs/images/instalacion.png)

## Requirements

- An **Android ARM64** device with a compatible GPU and drivers. On Mali devices, compatibility also depends on the kernel; having a Mali GPU alone is not enough.
- Sufficient free storage: allow around **60 GB for game data**, plus approximately **4 GB for the app and its runtime environment**. Initial usage is lower and grows as game data is downloaded progressively.
- An Internet connection; Wi-Fi is recommended for downloads.
- An account to access the game.

## Installation and getting started

### 1. Install the app

Download the APK from [Releases](https://github.com/apazosg/ClassicForever-android/releases) and install it on Android. If prompted, allow app installations from the app you use to open the APK.

If you already use an older build, install `0.0.1` manually over it without uninstalling it. From that version onward, you can check for future updates from within the app.

Current builds may appear as **WoW Forever Mali**, with the package name `app.wowforever.mali`.

### 2. Prepare the game files

Open the app and grant the requested **all files access** permission so it can manage the game folder.

- **New installation:** choose a location and tap **Download & Install**. The default folder is `/storage/emulated/0/WoW Forever/`. You do not need to download all game data before the first launch: the client downloads it as needed.
- **Existing installation:** use **Locate Existing Files** to select its folder. If you copy an installation from a computer, keep both the `Data/` folder and the hidden `.build.info` file at the root of the game folder.

### 3. Configure the app and play

1. Set up or update your account from the main screen.
2. Adjust the resolution using the quick settings and review **Settings** if needed.
3. Once the game files are ready, start the game from the launcher. The first launch sets up the runtime environment and may take a few minutes.

### 4. In-game controls and settings

- Press **Back** to open the side menu with keyboard, on-screen controls, performance, and exit options.
- Gamepads use the game's built-in controller support.
- To return to configuration when the app starts the game automatically, press Back during the startup screen or hold **Start + Select + L2 + R2**.
- Enter additional authentication codes manually when required.

## Tested devices

| Device | Tested driver | Result |
| --- | --- | --- |
| **POCO X4 GT** | PanVK — Zenith 26.3.1 | Runs at low FPS (**<20**). |
| **POCO X8 Pro Max** | PanVK — Zenith 26.3.1 | Playable (**>30 FPS**). |
| **Google Pixel 10a** | To be confirmed | Testing in progress. |

Unofficial community project, not affiliated with or endorsed by Blizzard Entertainment. This app's APKs do not include Blizzard game files.
