## IQData SDK

[![Release](https://jitpack.io/v/jitpack/android-example.svg)](https://jitpack.io/#jitpack/android-example)

This is Android SDK for IQdata. This library allows you to send user data (location, Wi-Fi networks, device info) from your Android app to IQdata. This guide explains how to integrate it to your application.

### Table of Contents
- [Requirements](#requirements)
- [Permissions](#permissions)
- [Installation](#installation)
    - [Step 1: Add JitPack repository](#step-1-add-jitpack-repository)
    - [Step 2. Add IQdata SDK](#step-2-add-iqdata-sdk)

### Requirements
|Java|Android|Gradle|Gradle Android plugin|
|---|---|---|---|
|8 or higher|4.0.3 (API Level 15) or higher|Use latest version|3.0 or higher|

### Permissions
The IQdata SDK requires at least of the following permissions: ACCESS_FINE_LOCATION or ACCESS_COARSE_LOCATION. By default IQdata SDK requires ACCESS_FINE_LOCATION but feel free to reqest ACCESS_COARSE_LOCATION if the first doesn't comply your application policy.

`android.permission.ACCESS_COARSE_LOCATION` – Allows to use WiFi or mobile cell data (or both) to determine the device's location. The API returns the location with an accuracy approximately equivalent to a city block.
`android.permission.ACCESS_FINE_LOCATION` – Allows to determine as precise location as possible from the available location providers, including the Global Positioning System (GPS) as well as WiFi and mobile cell data.

You can implement the permission request with https://developer.android.com/training/permissions/requesting#make-the-request

### Installation

To install IQData SDK you will have to make some set up in the gradle file of your project. To do so, follow the steps described below:

#### Step 2: Add JitPack repository

Open your root `build.gradle` (or `build.gradle.kts` if you are using Kotlin script) file and add JitPack as a repository:

##### Groovy
```groovy
allprojects {
    repositories {
        …
        maven { url 'https://jitpack.io' }
    }
}
```
##### Kotlin script
```kotlin
allprojects {
    repositories {
        …
        maven("https://jitpack.io")
    }
}
```
Note: we also can display the snippets like this:
<table>
<tr>
<th>Groovy</th>
<th>Kotlin script</th>
</tr>
<tr>
<td>
    
```groovy
allprojects {
    repositories {
        …
        maven { url 'https://jitpack.io' }
    }
}
```
</td>
<td>
    
```kotlin
allprojects {
    repositories {
        …
        maven("https://jitpack.io")
    }
}
```
</td>
</tr>
</table>   

#### Step 2. Add IQdata SDK

In your module `build.gradle` (or `build.gradle.kts` if you are using Kotlin script) file enable Java 8 features support and add iqdata-android-sdk to your compile dependencies:

##### Groovy
```groovy
android {
    …
    compileOptions {
        sourceCompatibility JavaVersion.VERSION_1_8
        targetCompatibility JavaVersion.VERSION_1_8
    }
}
dependencies {
    …
    implementation "com.iqdata:iqdata-android-sdk:VERSION"
}
```
##### Kotlin script
```kotlin
android {
    …
    compileOptions {
        sourceCompatibility = JavaVersion.VERSION_1_8
        targetCompatibility = JavaVersion.VERSION_1_8
    }
}
dependencies {
    …
    implementation("com.iqdata:iqdata-android-sdk:VERSION")
}
```
:small_blue_diamond: Don't forget to change the last line with the latest version of IQdata SDK for Android.

You will be hinted for a project sync as you have updated the gradle files.

:heavy_check_mark: That's it, the IQData SDK will have been installed once the sync is completed.
