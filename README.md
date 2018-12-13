## iqdata-android-sdk

An Android SDK for iqdata. This library helps you send analytics/usage/whatever data from your Android app to [insert where].

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
The IQData Android SDK uses following permissions: ACCESS_COARSE_LOCATION and ACCESS_FINE_LOCATION You should ask one of these permissions in your app.
The permission you choose determines the accuracy of the location returned by the API. You only need to request one of the Android location permissions, depending on the level of accuracy you need:

`android.permission.ACCESS_COARSE_LOCATION` – Allows the API to use WiFi or mobile cell data (or both) to determine the device's location. The API returns the location with an accuracy approximately equivalent to a city block.
`android.permission.ACCESS_FINE_LOCATION` – Allows the API to determine as precise a location as possible from the available location providers, including the Global Positioning System (GPS) as well as WiFi and mobile cell data.

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
Don't forget to change the line below with the latest version of IQDara SDK for Android!

You will be hinted for a project sync as you have updated the gradle files. The IQData SDK will have been installed once the sync is completed.
