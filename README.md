# Development-Quick-Sheet

Flutter Flavor Build : 
https://medium.com/@animeshjain/build-flavors-in-flutter-android-and-ios-with-different-firebase-projects-per-flavor-27c5c5dac10b

flutter build apk --release --flavor app1 --target lib/app1/main.dart

flutter build appbundle --release --flavor app1 --target lib/app1/main.dart

# Generate Keystore 

keytool -genkey -v -keystore /Applications/Android\ Studio.app/Contents/jre/jdk/Contents/Home/bin/keytool -genkey -v -keystore ~/release.jks -keyalg RSA -keysize 2048 -validity 10000 -alias daqueen

# Run the generator,

# dart
pub run build_runner build
# flutter
flutter pub run build_runner build

# ProcessException: ProcessException: Operation not permitted command gradlew -v #41486
cmd ->    xattr -d com.apple.quarantine android/gradlew

#Release apk 
https://flutter.dev/docs/deployment/android

Generate keystore in mac 
#/Applications/Android\ Studio.app/Contents/jre/jdk/Contents/Home/jre/bin/keytool  -genkey -v -keystore ~/release.jks -keyalg RSA -keysize 2048 -validity 10000 -alias aliasName
app->build.gradle 
def keystoreProperties = new Properties()
def keystorePropertiesFile = rootProject.file('key.properties')
if (keystorePropertiesFile.exists()) {
    keystoreProperties.load(new FileInputStream(keystorePropertiesFile))
}

In keystore file
storePassword=
keyPassword=
keyAlias=
storeFile=\\keystore\\release.jks

gitlab issue

https://username@gitlab.com/single-vendor-e-commerce-flutter.git

# Generate sha1 with cmd 
gradlew signingReport

#No Null Safety
flutter build apk --release --no-sound-null-safety

#Cocopods issue for M1 
https://github.com/CocoaPods/CocoaPods/issues/9890
sudo arch -x86_64 gem install ffi

Then

arch -x86_64 pod install

#IOS pod installing problem solution 
https://github.com/invertase/react-native-firebase/issues/321

# How to change the package name ? 
flutter pub run rename --bundleId com.daqueen.app 
flutter pub run rename --appname "Daqueen"

# Problem - Password for 'https://git@github.com': 
remote: Invalid username or password.
fatal: Authentication failed for 'https://git@github.com/eurydyce/MDANSE.git/'

cmd : git config credential.helper ""


