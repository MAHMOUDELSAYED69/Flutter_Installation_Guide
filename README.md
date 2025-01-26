![image](https://github.com/user-attachments/assets/47091750-ef0f-4014-b471-57c0b18b975c)
# Flutter Installation Guide (Windows)

This guide provides a step-by-step process to install Flutter on your Windows system, set up Android Studio, create an Android emulator, and run your first Flutter app. Follow the instructions below in the specified sequence.

---

## Table of Contents

1. [System Requirements](#system-requirements)
2. [Install Flutter](#install-flutter)
3. [Install Java JDK](#install-java-jdk)
4. [Configure Java](#configure-java)
5. [Configure Flutter](#configure-flutter)
6. [Install Android Studio](#install-android-studio)
7. [Set Up Android Emulator](#set-up-android-emulator)
8. [Set up IDE (Optional)](#set-up-ide-optional)
   - [Visual Studio Code](#visual-studio-code)
9. [Run Your First App](#run-your-first-app)

---

## System Requirements

Before you install Flutter, ensure your system meets the following requirements:

- **Operating System**: Windows 10 or later.
- **Disk Space**: `2.8 GB` (does not include disk space for IDE/tools).
- **Tools**: `Git` and `PowerShell`.

---

## Install Flutter

1. **Download the Flutter SDK**:
   - Visit the [Flutter SDK download page](https://docs.flutter.dev/get-started/install/windows) and download the latest stable release for Windows.
   - Direct download link (latest stable version):
     ```bash
     https://storage.googleapis.com/flutter_infra_release/releases/stable/windows/flutter_windows_3.27.3-stable.zip
     ```

2. **Extract the Flutter SDK**:
   - Extract the downloaded zip file to a desired location (e.g., `C:\src\flutter`).

3. **Update Environment Variables**:
   - Open **System Properties** → **Advanced** → **Environment Variables**.
   - Under **User variables**, select `Path` and click **Edit**.
   - Add the `flutter\bin` directory to your system path (e.g., `C:\src\flutter\bin`).

4. **Verify Installation**:
   - Open a new terminal (Command Prompt or PowerShell) and run:
     ```bash
     flutter doctor
     ```
   - This command checks your environment and displays a report of the status of your Flutter installation.

---

## Install Java JDK

1. **Download the Java JDK**:
   - Visit the [Oracle JDK download page](https://www.oracle.com/java/technologies/downloads/#java17-windows) for Java 17 (or the latest version).
   - Direct download link (latest stable version):
     ```bash
     https://download.oracle.com/java/17/archive/jdk-17.0.12_windows-x64_bin.exe
     ```
   - Accept the license agreement and download the Windows installer.

2. **Install the JDK**:
   - Run the installer and follow the instructions to complete the installation.

---

## Configure Java

1. **Set the `JAVA_HOME` Environment Variable**:
   - Open **System Properties** → **Advanced** → **Environment Variables**.
   - Under **System variables**, click **New** and add:
     - Variable name: `JAVA_HOME`
     - Variable value: `C:\Program Files\Java\jdk-17` (replace `17` with the actual version number if different).

2. **Update the `Path` Variable**:
   - In the **System variables** section, find the `Path` variable and click **Edit**.
   - Click **New** and add the following entry:
     ```
     %JAVA_HOME%\bin
     ```
   - Click **OK** to save the changes.

3. **Verify Java Installation**:
   - Open a new Command Prompt or PowerShell window.
   - Run the following command to verify Java is correctly configured:
     ```bash
     java -version
     ```
   - You should see the installed Java version displayed.

---

## Install Android Studio

1. **Download Android Studio**:
   - Visit the [Android Studio download page](https://developer.android.com/studio) and download the latest version for Windows.

2. **Install Android Studio**:
   - Run the downloaded installer and follow the installation wizard.
   - During installation, ensure the following components are selected:
     - Android SDK
     - Android SDK Platform
     - Android Virtual Device (AVD)

3. **Launch Android Studio**:
   - After installation, launch Android Studio and complete the setup wizard to install the latest SDK tools.

---

## Set Up Android Emulator

1. **Open AVD Manager**:
   - In Android Studio, go to **Tools** > **Device Manager**.

2. **Create a New Virtual Device**:
   - Click **Create Device**.
   - Select a device definition (e.g., `Pixel 5`) and click **Next**.

3. **Select System Image**:
   - Choose a system image with **Android 14 (API Level 35)**.
   - If the image is not installed, click the **Download** link next to the release name and follow the prompts to install it.

4. **Configure AVD**:
   - After selecting the system image, click **Next**.
   - Configure the AVD settings (e.g., RAM, storage) and click **Finish**.

5. **Launch the Emulator**:
   - In the Device Manager, select the newly created AVD and click **Start**.

---

## Set up IDE (Optional)

### **Visual Studio Code**

1. **Install Visual Studio Code**:
   - Download and install [Visual Studio Code](https://code.visualstudio.com/).

2. **Install Flutter and Dart Extensions**:
   - Open VS Code, go to the **Extensions** view (`Ctrl+Shift+X`), and search for "Flutter" and "Dart".
   - Install both extensions.

3. **Verify Setup**:
   - Open a terminal in VS Code and run:
     ```bash
     flutter doctor
     ```

---

## Run Your First App

1. **Create a New Flutter Project**: 
   - Open a terminal and run:
     ```bash
     flutter create my_first_app
     ```

2. **Navigate to Your Project Directory**:
   - Run:
     ```bash
     cd my_first_app
     ```

3. **Run the App**:
   - Start the Android emulator or connect a physical device.
   - Run the app using:
     ```bash
     flutter run
     ```

---

## Configure Flutter

After installing the SDK, run the following command to ensure everything is configured properly:

```bash
flutter doctor
```

This command checks for any missing dependencies or tools required to complete the setup.

Example output:
```
Doctor summary (to see all details, run flutter doctor -v):
[✓] Flutter (Channel stable, 3.27.3, on Windows 11)
[✓] Android toolchain - develop for Android devices
[✓] Chrome - develop for the web
[✓] Android Studio (version 2022.1)
[✓] VS Code (version 1.80.0)
```

---

## Conclusion

Congratulations! You have successfully installed Flutter, set up Android Studio, created an Android emulator, and run your first Flutter app. You're now ready to start building beautiful and powerful applications. Explore the vast resources available in the Flutter community, and always keep learning and experimenting.

Happy coding! If you encounter any issues or have questions, feel free to reach out or check the Flutter community for support.
