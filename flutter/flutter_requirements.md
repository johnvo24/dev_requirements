## Flutter in Window
1. Flutter SDK
2. Vscode hoặc Android Studio
3. Android SDK
    - Nếu sử dụng Vscode thì tải Command Line Tools
4. Java Development Kit (JDK <= 18)
    - Tạo biến JAVA_HOME tới JDK

## Flutter in Fedora (Linux)
1. Install dependencies
> sudo dnf install bash curl file git unzip which xz zip mesa-libGLU clang cmake ninja-build pkg-config gtk3-devel
2. Install Flutter extension in Vscode
3. In Vscode
> Ctrl + P -> Enter: >Flutter:New Project </br>
> Download SDK </br>
> Copy Flutter SDK path
4. Add flutter bin to PATH
> Open \~/.bashrc file and paste: export PATH="$PATH:\~/dev/flutter/bin"
5. Download Command Line Tools and download Android SDK
> <a href="https://developer.android.com/studio#command-tools">Go to download</a> </br>
> Add to ~/dev/android-sdk folder </br>
> cd ~/dev/android-sdk/cmdline-tools/bin </br>
> Run in terminal: ./sdkmanager --sdk_root=$HOME/dev/android-sdk "platform-tools" "platforms;android-33" "build-tools;33.0.0" </br>
> <b>>>> REMEMBER TO THE LEVEL OF API (android-33) <<<</b> </br>
6. Add Android SDK path to PATH
> Open ~/.bashrc file and paste: </br>
> export ANDROID_HOME=$HOME/dev/android-sdk </br>
> export PATH=$PATH:$ANDROID_HOME/platform-tools:$ANDROID_HOME/cmdline-tools/bin </br>
> Change cmdline-tools/bin to cmdline-tools/latest/bin and update to PATH
7. Install OpenJDK (version <= 18)
> sudo dnf install java-17-openjdk-devel
> Add JAVA_HOME in PATH: export JAVA_HOME=/usr/lib/jvm/java-17-openjdk
8. Run app
> flutter devices
> flutter run -d (device_id)
