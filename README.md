## iqdata-android-sdk

An Android SDK for [enter purposes here]

### Table of Contents
- [Requirements](#requirements)
- [Permissions](#permissions)
- [Installation](#installation)

### Requirements
|Product|Version|
|---|---|
|Java|8 or higher|
|Android|4.0.3 (API Level 15) or higher|
|Gradle|Use latest version|
|Gradle Android plugin|3.0 or higher|

### Permissions
SDK uses `ACCESS_FINE_LOCATION` and `ACCESS_COARSE_LOCATION`. You should ask one of these permissions in your app.

### Installation

Follow the steps below to add IQData SDK to your app.

1. Add JitPack repository

Open your root `build.gradle` file and add JitPack as a repository:

Groovy
```groovy
allprojects {
    repositories {
        ...
        maven { url 'https://jitpack.io' }
    }
}
```
Kotlin script
```kotlin
allprojects {
    repositories {
        ...
        maven("https://jitpack.io")
    }
}
```
2. Add IQdata SDK

Add in app build.gradle:

Groovy
```groovy
android {
    ...
    compileOptions {
        sourceCompatibility JavaVersion.VERSION_1_8
        targetCompatibility JavaVersion.VERSION_1_8
    }
}
dependencies {
    ...
    implementation "com.iqdata:iqdata-android-sdk:VERSION"
}
```
Kotlin script
```kotlin
android {
    ...
    compileOptions {
        sourceCompatibility = JavaVersion.VERSION_1_8
        targetCompatibility = JavaVersion.VERSION_1_8
    }
}
dependencies {
    ...
    implementation("com.iqdata:iqdata-android-sdk:VERSION")
}
```

You will be hinted for a project sync as you have updated the gradle files. The IQData SDK will have been installed once the sync is completed.
