# 🎮 Overlook - Control Your KVM Devices Effortlessly

## 🏷️ Overview

Overlook is a macOS-native remote console for GL.iNet GLKVM / Comet-style KVM devices. With this application, you can easily manage and interact with your KVM devices from the comfort of your Mac. Whether you need to perform maintenance or access controls from anywhere, Overlook simplifies the process.

![Overlook Screenshot](OverlookScreenshot.png)

## 🛠️ Building from Source

### Prerequisites

- **macOS 14.0 (Sonoma)** or later
- **Xcode 15** or later (available from the [Mac App Store](https://apps.apple.com/app/xcode/id497799835))
- An Apple ID (free) signed in to Xcode for code signing

### Steps

1. **Clone the repository:**

   ```bash
   git clone https://github.com/iamjairo/Glinet-KVM-Overlook.git
   cd Glinet-KVM-Overlook
   ```

2. **Open the project in Xcode:**

   ```bash
   open Overlook.xcodeproj
   ```

   Or double-click `Overlook.xcodeproj` in Finder.

3. **Resolve Swift Package dependencies:**

   Xcode automatically resolves the [WebRTC](https://github.com/stasel/WebRTC) Swift Package dependency the first time the project is opened. Wait for the package resolution to complete (visible in the progress bar at the top of the Xcode window).

4. **Configure code signing:**

   - In the Project navigator, select the **Overlook** project.
   - Select the **Overlook** target.
   - Under the **Signing & Capabilities** tab, choose your personal team from the **Team** dropdown (sign in with your Apple ID via **Xcode → Settings → Accounts** if needed).

5. **Build and run:**

   Select **My Mac** as the run destination in the toolbar, then press **⌘R** (or choose **Product → Run**).

   To build without running, press **⌘B** (or choose **Product → Build**).

### Command-line build (optional)

```bash
xcodebuild -project Overlook.xcodeproj \
           -scheme Overlook \
           -configuration Release \
           -destination 'platform=macOS' \
           CODE_SIGN_IDENTITY="-" \
           build
```

The built app will be placed in the `~/Library/Developer/Xcode/DerivedData/` directory.

---

## 🚀 Getting Started

### 🖥️ System Requirements

To run Overlook, you need the following:

- macOS 14.0 (Sonoma) or later
- At least 2 GB of RAM
- 100 MB of free disk space

### ⚙️ Usage

1. **Connect to Your KVM Device:**
   When Overlook opens, click on "Connect" to add a new device. Enter the IP address of your KVM device. If you're unsure of the IP, refer to your device's documentation.

2. **Login:**
   Input your username and password for the KVM device. Ensure these are correct to gain access.

3. **Configuration Options:**
   Explore various settings within Overlook. You can customize how the interface displays information about your KVM device. Feel free to adjust settings based on your preferences.

## 📘 Features of Overlook

- **Secure Connections:** Overlook supports SSL connections to ensure secure communication with your KVM devices.
- **User-friendly Interface:** The application presents a clean and straightforward interface, making it easy for anyone to use.
- **Multi-Device Support:** You can connect and control multiple KVM devices simultaneously using tabs.
- **Real-time Updates:** The app provides real-time updates about the status of your connected KVM devices.

## 📫 Support & FAQ

If you encounter any issues or have questions, please check the following:

- **Common Issues:**
  - If Overlook fails to connect, verify that your KVM device is powered on and connected to the same network.
  - Ensure you entered the correct IP address and credentials.

- **Where to Get Help:**
  Visit the [GitHub Issues page](https://github.com/iamjairo/Glinet-KVM-Overlook/issues) to report a problem or ask questions.

## 📅 Future Updates

We plan to regularly update Overlook with new features and improvements. Follow the GitHub repository to stay informed about the latest releases and enhancements.

## 📄 License

This project is licensed under the MIT License. You can use, modify, and distribute the code as per the license terms.
