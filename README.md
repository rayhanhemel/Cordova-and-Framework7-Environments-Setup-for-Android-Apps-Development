# Cordova-and-Framework7-Environments-for-Android-App-Development

Instruction: Cordova and Framework7 Environments Setup for Android Apps Development

Requirements: Good Internet, Enough Space of C Drive, CMD, Node.js, JAVA JDK & JRE, Android Studio with Android SDK, Android SDK Command Line Tools, Gradle, Cordova, Framework7, Genymotion Emulator

 
1) Please see below video and links first
- https://www.youtube.com/watch?v=nQ498PINsws
- https://gist.github.com/prof3ssorSt3v3/957d91b166ef58b19631439e0447cd01
- https://gist.github.com/prof3ssorSt3v3/957d91b166ef58b19631439e0447cd01


2) Create a Project folder 
- Do not use '@','_', etc. special character at folder name


3) Do not open or use Multiple CMD
- Just use a single cmd at your project location
- Use CMD at the project location 
	Example: I:\ResearchProject\CordovaProject>


4) Find the Environment Variables option
- System -> Advanced System Settings -> System Properties -> Environment Variables
- Find the two segments "User Variables for User" and "System Variables"


5) Install Node.js and check it at CMD
- Check the NPM path "C:\Users\Rayhan\AppData\Roaming\npm" at the Path option of Environment Variables (User Variable)
- Check the Node.js path "C:\Program Files\nodejs" at the Path option of Environment Variables (System Variables) 
- If you not found, add these paths


6) Install JAVA JDK and JRE
- Setup JAVA_HOME at Environment variables (User Variables)
	JAVA_HOME -> C:\Program Files\Java\jdk1.8.0_172
- Also, set the path (System Variables)
	Path -> C:\Program Files\Java\jre1.8.0_172\bin
- Check "javac" at CMD


7) Install 'Android Studio' for 'Android SDK'


8) Install 'Android SDK Command Line Tools from SDK Manager of Android Studio
(If Android SDK Command-Line not installed)
- Accept License during installation


9) Set Android SDK location at Environment variables by following rules
- Setup 'ANDROID_HOME' and 'ANDROID_SDK_ROOT' at Environment variables (User Variable)
ANDROID_SDK_ROOT -> C:\Users\Rayhan\AppData\Local\Android\Sdk
	ANDROID_HOME -> C:\Users\Rayhan\AppData\Local\Android\Sdk
- Set up the Android SDK path at Environment variables (System Variable)
	PATH -> %ANDROID_HOME%\platform-tools


10) Set below paths Environment variables (System Variable)
- %ANDROID_SDK_ROOT%\emulator
- %ANDROID_SDK_ROOT%\cmdline-tools
- %ANDROID_SDK_ROOT%\cmdline-tools\bin
- %ANDROID_SDK_ROOT%\platform-tools
- %ANDROID_SDK_ROOT%\build-tools


11) Install Gradle
- Setup GRADLE_HOME at Environment variables (User Variable)
	GRADLE_HOME -> C:\Program Files\Gradle\gradle-6.3
- Set the path of Gradle (System Variable)
	PATH -> C:\Program Files\Gradle\gradle-6.3\bin


12) Open or run an Emulator from Android Studio
- Install "Genymotion (personal edition)", configure Genymotion with Android Studio and use this emulator for working faster
	Video Link: https://www.youtube.com/watch?v=9d3ucMIK5H8
- Click on Emulator for running
- If you get an error "VT-x is disabled in the bios", watch this video: https://youtu.be/vP71TkSh67M
- If you get an error "INTEL HAXM is required" error, watch this video: https://youtu.be/G-NAR4-X8sY
- If you do not find "UEFI BIOS Setup", watch this video: https://youtu.be/074Qf5nUzeY
- Maybe you will need to restart Computer or Android Studio and try to open Emulator.


13) Open new CMD at project directory location (Close Other CMD)


14) Framework7 CLI and Cordova Installation. Link: https://framework7.io/cli/installation.html
- npm install -g cordova
- npm install -g framework7-cli
- npm install -g framework7-cli --unsafe-perm=true --allow-root
- do not afraid about "npm WARN deprecated", it is just a warning, it is not an error.


15) Create App with Framework7 CLI. Link: https://framework7.io/cli/create-app.html
- framework7 create --ui


16) After opening http://localhost:3001/create/
- I have selected the Cordova App (Targets Native iOS and Android Apps....)
- Created Destination Name, Project APP Name, Package Name
- -Do not use '@','_', etc. special character
- Automatically selected 'iOS' and 'Android' at Cordova section
- selected 'Framework7 with Vue.js' at Framework section
- selected 'Tabbed Views (Tabs)' at Choose starter template option
- then clicked 'Create App'


17) After creating the app, the process showed below notes:
Please Note these commands but do not use these at early stages !!!!
!!!!!!!!!!! 
  - "npm run start" -> run development server
  - "npm run dev" -> run development server
  - "npm run build-dev" -> build web app using development mode (faster build without minification and optimization)
  - "npm run build-prod" -> build web app for production
  - "npm run build-dev-cordova" -> build cordova app using development mode (faster build without minification and optimization)
  - "npm run build-prod-cordova" -> build cordova app
  - "npm run build-dev-cordova-ios" -> build cordova iOS app using development mode (faster build without minification and optimization)
  - "npm run build-prod-cordova-ios" -> build cordova iOS app
  - "npm run build-dev-cordova-android" -> build cordova Android app using development mode (faster build without minification and optimization)
  - "npm run build-prod-cordova-android" -> build cordova Android app
  - Visit documentation at https://framework7.io/docs/
  - Check README.md in project root folder with further instructions


18) Open new CMD at project directory location (Close Other CMD) and type below commands
- npm run start (for opening the app at http://localhost:8080/) 
- npm run build-dev-cordova-android


19) Run Framework7:
- framework7 cordova run android
- Do not afraid about "No target specified and no makefile found...", it is not an error
- The app will run at Emulator.


20) For Error "Unexpected token in JSON at position 0" :
- Try to create a new project and follow the 13 to 19 steps again
- do not afraid about 'npm WARN deprecated', it is just a warning, it is not an error.


21) For Error "Application Error. Connection to server was unsuccessful (file://android_asset/www/index.html)"
- add "<preference name="loadUrlTimeoutValue" value="120000" />"  at "confg.xml" file of "cordova" folder
- Restart Android Studio and Emuletor
- framework7 cordova run android
- App will show at Emulator.


Thank You. 

Regards,
S. Rayhan Kabir
https://www.linkedin.com/in/s-rayhan-kabir/

