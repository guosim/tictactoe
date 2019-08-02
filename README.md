
**Environment Setup for Mac and Android**  
These steps can be found on [https://facebook.github.io/react-native/docs/getting-started.html](https://facebook.github.io/react-native/docs/getting-started.html)  
If all else fails, follow the troubleshooting guide here: [https://facebook.github.io/react-native/docs/troubleshooting](https://facebook.github.io/react-native/docs/troubleshooting)1. We need to install Node, Watchman and JDK (Same steps for iOS and Android)

> • `brew install node`  
> • `brew install watchman`  
> • `brew tap AdoptOpenJDK/openjdk`  
> • `brew cask install adoptopenjdk8`

2. Install the React Native CLI (Same steps for iOS and Android)

> • `npm install -g react-native-cli`

3. Install Android Studio

> • Choose 'Custom' setup when prompted to select an installation type.  
> • Make sure the boxes next to all of the following are checked:
```
Android SDK  
Android SDK Platform  
Performance (Intel ® HAXM) (See here for AMD)  
Android Virtual Device
```
4. Install the Android SDK  
  
• The SDK Manager can be accessed from the "Welcome to Android Studio" screen. Click on "Configure", then select "SDK Manager".  
• The SDK Manager can also be found within the Android Studio "Preferences" dialog, under Appearance & Behavior → System Settings → Android SDK.  
• Select the "SDK Platforms" tab from within the SDK Manager, then check the box next to "Show Package Details" in the bottom right corner. Look for and expand the Android 9 (Pie) entry, then make sure the following items are checked:

> • Android SDK Platform 28  
> • Intel x86 Atom_64 System Image or Google APIs Intel x86 Atom System Image

• Next, select the "SDK Tools" tab and check the box next to "Show Package Details" here as well. Look for and expand the "Android SDK Build-Tools" entry, then make sure that 28.0.3 is selected.  
• Finally, click "Apply" to download and install the Android SDK and related build tools.5. Configure the ANDROID_HOME environment variable

> • Add the following lines to your $HOME/.bash_profile or $HOME/.bashrc config file:
```
export ANDROID_HOME=$HOME/Library/Android/sdk  
export PATH=$PATH:$ANDROID_HOME/emulator  
export PATH=$PATH:$ANDROID_HOME/tools  
export PATH=$PATH:$ANDROID_HOME/tools/bin  
export PATH=$PATH:$ANDROID_HOME/platform-tools  
```
6. Type source $HOME/.bash_profile to load the config into your current shell. Verify that ANDROID_HOME has been added to your path by running echo $PATH.  
  
  
**Environment Setup for Mac and iOS**  
These steps can be found on [https://facebook.github.io/react-native/docs/getting-started.html](https://facebook.github.io/react-native/docs/getting-started.html)  
  
If all else fails, follow the troubleshooting guide here: [https://facebook.github.io/react-native/docs/troubleshooting](https://facebook.github.io/react-native/docs/troubleshooting)1. We need to install Node, Watchman and JDK (Same steps for iOS and Android)

> • `brew install node`  
> • `brew install watchman`  
> • `brew tap AdoptOpenJDK/openjdk`  
> • `brew cask install adoptopenjdk8`

2. Install the React Native CLI (Same steps for iOS and Android)

> • `npm install -g react-native-cli`

3. Install Xcode via Mac App Store  
4. After Xcode is done installing, install Xcode Command Line Tools by opening Xcode > Preferences > Locations and selecting the most recent version in the Command Line Tools dropdown  
  
**Existing App Setup**  
1. Clone the repo  
2. Navigate to project folder, then `npm install`  
  
**Production Build Steps**  
Android:  
1. Start in root of project folder  
2. `cd android`  
3. `./gradlew assembleRelease`  
4. APK file will be generated at `../android/app/build/outputs/apk/release/app-release.apk`iOS:  
1. Open the app in XCode (.xcworkspace or .xcodeproj)  
2. Select 'Generic iOS Device' in the list of simulators dropdown  
3. Click on Product -> Archive  
4. Select the newly created archive in Organizer (⌥⇧⌘O)  
5. Click the 'Validate App' button and go through the the prompts (use default settings)  
6. After the app is successfully validated, click the 'Distribute App' button

> • Distribute through the iOS App Store  
> • Upload instead of Export  
> • Keep both distribution options checked  
> • Automatically manage signing  
> • Click Upload

5. Log in to [https://itunesconnect.apple.com](https://itunesconnect.apple.com/)  
6. Select the app, then choose the build that was uploaded
