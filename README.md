# flutter_application_1

A new Flutter project.

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://docs.flutter.dev/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://docs.flutter.dev/cookbook)

For help getting started with Flutter development, view the
[online documentation](https://docs.flutter.dev/), which offers tutorials,
samples, guidance on mobile development, and a full API reference.
##
install flutter extension (dart extension will be automatically installed)

##
setup git

##
https://stackoverflow.com/questions/46877667/how-to-add-a-new-project-to-github-using-vs-code#:~:text=(CTRL%2BSHIFT%2BP%20%2D,section%20from%20the%20left%20menu.

install visual studio along with 'desktop/web development with C++' workload

##
Setup Android SDKs without Android studio
https://proandroiddev.com/how-to-setup-android-sdk-without-android-studio-6d60d0f2812a
https://guides.codepath.com/android/installing-android-sdk-tools
https://developer.android.com/studio  -- download commandline tools only
https://developer.android.com/tools/sdkmanager

https://medium.com/@quicky316/install-flutter-sdk-on-windows-without-android-studio-102fdf567ce4
https://stackoverflow.com/questions/65262340/cmdline-tools-could-not-determine-sdk-root

https://abrialstha.medium.com/getting-started-with-flutter-without-android-studio-c7e1128330dd#:~:text=Installing%20Flutter%20In%20Windows%20(But%20without%20android%20studio)&text=Install%20Android%20SDK%20for%20windows,in%20env%20path%20as%20well.
##
Add following paths:
%JAVA_HOME%\bin
D:\flutter_windows\flutter\bin
%ANDROID_HOME%\cmdline-tools\tools\bin   --> this is for android sdkmanager
%ANDROID_HOME%\emulator  --> this folder will be created later after running sdkmanager commands, but configure it in path first
%ANDROID_HOME%\platform-tools --> this folder will be created later after running sdkmanager commands, but configure it in path first

Add the following env var:
ANDROID_HOME = C:\Android

##
sdkmanager --update
sdkmanager --install "platform-tools" "platforms;android-29" "build-tools;29.0.2" "emulator"

sdkmanager “system-images;android-27;default;x86_64”
sdkmanager “platform-tools”
sdkmanager “build-tools;27.0.3”
sdkmanager “platforms;android-27”
sdkmanager emulator
sdkmanager --licenses

##
configure flutter to know the dir of Android sdk path
flutter config --android-sdk "C:\Android\cmdline-tools\"
flutter doctor --android-licenses

avdmanager -s create avd -n nexus -k “system-images;android-27;default;x86_64”

flutter emulators --launch nexus

flutter doctor -v

cd C:\Android\flutter\examples\hello_world --> not required if you are running all these commands from inside the project
flutter run


##
https://flutteragency.com/set-up-an-emulator-for-vscode/
https://stackoverflow.com/questions/63817988/i-try-to-make-android-studio-emulator-work-with-vs-code-but-have-an-error-avd
https://github.com/flutter/flutter-intellij/issues/3146