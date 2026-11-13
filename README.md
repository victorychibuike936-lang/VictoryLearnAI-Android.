# Victory Learn AI — Android Studio project

Developer credit: Chibuike Victory  
Package ID: `ai.victorylearn.app`  
Minimum Android version: Android 6.0 (API 23)

## Important status
This is an Android Studio **source project**, not a compiled or signed APK.
The app shell opens the existing Victory Learn AI web app inside Android WebView.
It needs an internet connection for its first load and to fetch updated web content.
The web app may cache some content after loading, but this wrapper is not a fully
self-contained offline APK and does not bundle the web app's full source/assets.

## Build an APK
1. Install Android Studio on a computer.
2. Extract this ZIP.
3. In Android Studio choose **Open** and select this extracted `VictoryLearnAI-Android` folder.
4. Allow Gradle sync to finish (Android SDK Platform 35 and JDK 17 are required).
5. Choose **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
6. Android Studio will show the generated APK location, usually
   `app/build/outputs/apk/debug/app-debug.apk`.

For a shareable release APK, use **Build > Generate Signed Bundle / APK** and
create a signing key. Keep that key private and backed up.

## Low-memory phone notes
The wrapper itself is lightweight and uses Android System WebView. Actual memory
use depends mostly on the web app and the phone's available memory. Close other
apps if the device runs short of memory.

## App URL
https://victory-learn-ai-bwd9cr.v2.appdeploy.ai/

## Next step for a fully offline APK
Bundle the compiled Vite `dist/` assets inside the Android project (rather than
loading the hosted URL), verify all required libraries work offline, then build
and sign the APK.
