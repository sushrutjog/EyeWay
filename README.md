# EyeWay

EyeWay is a lightweight macOS menu-bar utility that reminds users to take a short break every 25 minutes by displaying a semi-transparent full-screen overlay with a countdown timer. It helps reduce eye strain and encourages healthier screen habits without blocking interaction.

## Features

* Runs silently in the menu bar (no Dock icon).
* Automatically triggers a 2-minute break every 25 minutes.
* Full-screen, semi-transparent overlay with a live countdown.
* "Skip Break" button to dismiss the overlay at any time.
* Universal binary for both Apple Silicon and Intel Macs.
* No Apple Developer Program membership required for distribution (unsigned ad-hoc build).

## Download & Install (Unsigned)

1. Go to the [Releases page](https://github.com/your-username/EyeWay/releases).
2. Download the latest `EyeWay.app.zip` asset.
3. Double-click the ZIP to unzip.
4. Drag **EyeWay.app** into your `/Applications` folder.
5. **Control-click** (or right-click) **EyeWay.app** → **Open** → **Open** again to bypass Gatekeeper's "unidentified developer" warning.
6. The EyeWay icon will appear in your menu bar. The app is now running and will remind you every 25 minutes.

## Usage

* **Break Overlay:** After each 25‑minute work period, a dimmed full-screen overlay appears with a countdown (2:00 → 0:00).
* **Skip Break:** Click the **Skip Break** button on the overlay or select **Skip Break** from the menu-bar icon to dismiss early.
* **Quit:** Select **Quit** from the menu-bar dropdown to exit EyeWay.

## Auto‑Launch at Login (Optional)

To have EyeWay start automatically on system login:

1. Open **System Settings** → **General** → **Login Items**.
2. Under **Open at Login**, click **+**, navigate to `/Applications`, and add **EyeWay.app**.

## Building from Source

If you want to build EyeWay yourself (Xcode 16.3 required):

```bash
# Clone the repo
git clone https://github.com/your-username/EyeWay.git
cd EyeWay

# Open in Xcode
open EyeWay.xcodeproj
```

1. Select **Any Mac (Universal)** as the build destination.
2. Build and Run (⌘R) to test.
3. Follow the sections in the Xcode project’s **Signing & Capabilities** to export an unsigned build:

   * Product → Clean Build Folder (⇧⌘K)
   * Product → Archive
   * In Organizer, right-click the archive → Show in Finder → Show Package Contents → Products/Applications/EyeWay.app
   * Copy and compress for distribution.
