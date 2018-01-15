<b>Steps to Run App on Android and IOS platform</b>

1) Checkout from Repository
2) Goto project directory
3) Run 
`npm install`

4) Run
`react-native run-android` to run app on Android Devices
`react-native run-ios` to run app on IOS Simulator

<b>Android Specific : </b>

React-Native Prepare unsigned APK : 

You need to manually create the bundle for a debug build.

Bundle debug build:
	
Run :

`react-native bundle --dev false --platform android --entry-file index.android.js --bundle-output ./android/app/build/intermediates/assets/debug/index.android.bundle --assets-dest ./android/app/build/intermediates/res/merged/debug`

Create debug build:

`cd android`

Then 

`./gradlew assembleDebug`

Generated apk will be located at android/app/build/outputs/apk


<b>IOS Specific</b>

You need to manually create the bundle for a debug build.
	
Run : 
`react-native bundle --dev false --entry-file index.ios.js --bundle-output ios/main.jsbundle --platform ios`

Go to XCode open Xcodeproject file 

Go to Product -> Archive in Xcode and follow the steps based on your desired release

Done !!!

