# Development-Quick-Sheet

Flutter Flavor Build : 
https://medium.com/@animeshjain/build-flavors-in-flutter-android-and-ios-with-different-firebase-projects-per-flavor-27c5c5dac10b

flutter build apk --release --flavor app1 --target lib/app1/main.dart

flutter build appbundle --release --flavor app1 --target lib/app1/main.dart

# Generate Keystore 

/Applications/Android\ Studio.app/Contents/jre/jdk/Contents/Home/bin/keytool -genkey -v -keystore ~/release.jks -keyalg RSA -keysize 2048 -validity 10000 -alias tictak-grocery

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
