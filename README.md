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

1. Get dependencies (REQUIRED before building):
   ```bash
   fvm flutter pub get
   ```
   
   **Important:** This step is required as it generates necessary build files for the CMake build system.

2. Run the app on your desktop platform:
   ```bash
   # For Linux
   fvm flutter run -d linux
   
   # For Windows
   fvm flutter run -d windows
   
   # For macOS
   fvm flutter run -d macos
   ```

## Building Manually with CMake (Linux)

If you want to build manually using CMake on Linux:

```bash
# First, ensure you've run flutter pub get
fvm flutter pub get

# Create build directory
cd linux
mkdir -p build
cd build

# Configure and build
cmake ..
cmake --build .
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

- **Build files:** The `flutter/CMakeLists.txt` files in platform directories are placeholders. When you run `fvm flutter pub get`, Flutter will generate the proper build configuration files. You must run `flutter pub get` before attempting to build the project manually with CMake.

- App icons: You'll need to add appropriate icon files to:
  - `windows/runner/resources/app_icon.ico` (Windows)
  - `macos/Runner/Assets.xcassets/AppIcon.appiconset/` (macOS - PNG files)
  - Linux uses the app icon from the window manager
  
- This is a minimal Flutter desktop app setup. Run `fvm flutter pub get` to download dependencies before building.