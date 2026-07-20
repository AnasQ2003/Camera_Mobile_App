<div align="center">

# 📷 Camera Application — Native Android Camera Integration

> A clean, focused Android application that demonstrates real-time hardware camera access using the Android Intent API, built with Java and Android Studio.

🎬 **Watch the Demo Video — Camera Application:** *(https://youtu.be/dNVPOpMTvsM)*

[![Android](https://img.shields.io/badge/Android-API_24%2B-3DDC84.svg?style=flat-square&logo=android)](https://developer.android.com/)
[![Java](https://img.shields.io/badge/Java-8-ED8B00.svg?style=flat-square&logo=openjdk)](https://www.java.com/)
[![Android Studio](https://img.shields.io/badge/Android_Studio-Hedgehog-3DDC84.svg?style=flat-square&logo=android-studio)](https://developer.android.com/studio)
[![Compile SDK](https://img.shields.io/badge/Compile_SDK-34-blue.svg?style=flat-square)](https://developer.android.com/about/versions/14)

</div>

---

## 🌟 Overview

The **Camera Application** is a native Android app that demonstrates how to integrate hardware camera functionality into a mobile application using the Android `MediaStore` Intent API. It allows a user to launch the device camera directly from within the app, capture a photo, and instantly display the captured image full-screen inside the application — all within a clean, minimal single-screen interface.

This project was developed to demonstrate core Android development principles including `Intent`-based activity communication, `onActivityResult` result handling, and bitmap rendering via `ImageView`.

---

## ✨ Features

- **📸 One-Tap Camera Launch**: A single button press fires a `MediaStore.ACTION_IMAGE_CAPTURE` Intent, seamlessly delegating control to the device's native camera application.
- **🖼️ Instant Photo Preview**: Upon returning from the camera, the captured image bitmap is immediately extracted from the `Intent` extras and rendered full-screen in an `ImageView`.
- **✅ Cancel Handling**: Gracefully handles user cancellation — if the user backs out of the camera, a polite `Toast` notification is displayed rather than crashing.
- **📱 Edge-to-Edge Layout**: Uses `EdgeToEdge` support and `WindowInsetsCompat` to render content seamlessly behind system bars for a modern Android experience.
- **🔒 Permission Declaration**: Declares `READ_EXTERNAL_STORAGE` permission in the manifest for compatibility with storage-integrated camera workflows.
- **🌙 Day/Night Theme Support**: Supports both Light and Dark themes through `values/` and `values-night/` resource directories.

---

## 🛠️ Tech Stack & Architecture

| Layer | Technology |
| :--- | :--- |
| **Language** | Java 8 |
| **UI Framework** | Android XML Layouts (RelativeLayout) |
| **Camera API** | `MediaStore.ACTION_IMAGE_CAPTURE` Intent |
| **Image Rendering** | Android `ImageView` + `Bitmap` |
| **Navigation** | `startActivityForResult` / `onActivityResult` |
| **Build System** | Gradle (Kotlin DSL - `.kts`) |
| **IDE** | Android Studio |

### Core Libraries
- `androidx.appcompat` — AppCompat backward compatibility
- `com.google.android.material` — Material Design components
- `androidx.activity` — Activity result contracts support
- `androidx.constraintlayout` — Flexible layout engine

---

## 📁 Project Structure

```
CameraApp_AnasAhmedQ_Android/
│
├── app/
│   ├── src/
│   │   └── main/
│   │       ├── java/com/example/cameraapplication/
│   │       │   └── MainActivity.java        # Single-activity logic: camera launch & result handling
│   │       │
│   │       ├── res/
│   │       │   ├── layout/
│   │       │   │   └── activity_main.xml    # RelativeLayout with TextView, Button, and ImageView
│   │       │   ├── drawable/                # App vector/drawable assets
│   │       │   ├── mipmap-*/               # App launcher icon at all DPI densities
│   │       │   ├── values/                  # Colors, strings, themes (Light)
│   │       │   ├── values-night/            # Dark mode theme overrides
│   │       │   └── xml/
│   │       │       ├── backup_rules.xml     # Cloud backup configuration
│   │       │       └── data_extraction_rules.xml  # Data extraction policy
│   │       │
│   │       └── AndroidManifest.xml          # Permissions, activity declarations
│   │
│   └── build.gradle.kts                     # App-level Gradle config (SDK 24–34, Java 8)
│
├── build.gradle.kts                         # Project-level Gradle configuration
├── settings.gradle.kts                      # Module settings
├── gradle.properties                        # Gradle performance & JVM flags
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites

- **Android Studio** (Hedgehog or newer)
- **Android SDK** (API Level 24 or higher)
- A **physical Android device** or **Android Emulator** with camera support

---

### Setup Instructions

**1. Clone the Repository:**
```bash
git clone https://github.com/AnasQ2003/Camera_Application.git
cd Camera_Application
```

**2. Open in Android Studio:**
- Launch Android Studio.
- Click **"Open"** and navigate to the cloned `Camera_Application` folder.
- Wait for Gradle sync to complete.

**3. Run the App:**
- Connect a physical Android device via USB (enable **USB Debugging**), or launch an **AVD emulator**.
- Click the ▶️ **Run** button in the Android Studio toolbar, or press `Shift+F10`.

---

## 📱 How It Works

```
User taps "Camera" button
        ↓
MainActivity fires Intent:
  MediaStore.ACTION_IMAGE_CAPTURE
        ↓
Device native camera app launches
        ↓
User captures photo → taps ✅ OK
        ↓
onActivityResult() is called:
  requestCode == REQUEST_CODE (22)
  resultCode  == RESULT_OK
        ↓
Bitmap extracted from Intent extras ("data")
        ↓
imageView.setImageBitmap(photo) — preview displayed
```

---

## 🔐 Permissions

| Permission | Purpose |
| :--- | :--- |
| `READ_EXTERNAL_STORAGE` | Enables reading photos saved to external storage by the camera |

---

## ⚙️ Build Configuration

| Property | Value |
| :--- | :--- |
| Minimum SDK | API 24 (Android 7.0 Nougat) |
| Target SDK | API 34 (Android 14) |
| Compile SDK | 34 |
| Java Compatibility | Java 8 (SOURCE & TARGET) |
| Version Name | 1.0 |
| Application ID | `com.example.cameraapplication` |

---

## 📄 License

```
MIT License

Copyright (c) Camera Mobile App --- 2026 AnasQ2003

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
```

---

## 👨‍💻 Author

**Anas Ahmed Qureshi** — [@AnasQ2003](https://github.com/AnasQ2003)

---

<div align="center">

Built with ❤️ by **Anas**

Made with 🔥 and a lot of ☕

**⭐ If you found this useful, please star the repository!**

</div>
