# video-editor

An empty Flutter Desktop-only app (Windows/Mac/Linux) using FVM for Flutter version management.

## Prerequisites

1. Install FVM (Flutter Version Manager):
   ```bash
   dart pub global activate fvm
   ```

2. Install Flutter stable version using FVM:
   ```bash
   fvm install stable
   fvm use stable
   ```

## Getting Started

1. Get dependencies:
   ```bash
   fvm flutter pub get
   ```

2. Run the app on your desktop platform:
   ```bash
   # For Linux
   fvm flutter run -d linux
   
   # For Windows
   fvm flutter run -d windows
   
   # For macOS
   fvm flutter run -d macos
   ```

## Project Structure

This is a Flutter desktop-only application configured for:
- Windows
- macOS
- Linux

Mobile (iOS/Android) and web platforms are not included.

## FVM Configuration

The project uses FVM with the stable Flutter channel. The configuration is stored in `.fvmrc`.

## Notes

- App icons: You'll need to add appropriate icon files to:
  - `windows/runner/resources/app_icon.ico` (Windows)
  - `macos/Runner/Assets.xcassets/AppIcon.appiconset/` (macOS - PNG files)
  - Linux uses the app icon from the window manager
  
- This is a minimal Flutter desktop app setup. Run `fvm flutter pub get` to download dependencies before building.