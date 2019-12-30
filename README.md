![](https://wiki.spicymobile.pl/wiki/mobigatesdk/download/Main/WebHome/MobienceSDK_Mobigate.png?width=300&height=300)
# React Native Mobigate SDK plugin for Android
MobigateSDK is a tool for gathering users phone data and events tracking. 

## Overview

[![Library version](https://img.shields.io/badge/npm%20package-1.0.2-brightgreen)](https://www.npmjs.com/package/react-native-mobigate) [![Platforms](https://img.shields.io/badge/platforms-android-lightgrey)](https://developer.android.com/)

  - [Plugin installation](#plugin-installation)
  - [SDK Initialization](#sdk-initialization)
  - [Guides](#guides)

## Plugin installation
```
yarn add react-native-mobigate
or
npm install react-native-mobigate --save
```
### React Native >= 0.60
Starting from React Native 0.60, [autolinking](https://github.com/react-native-community/cli/blob/master/docs/autolinking.md) makes the installation process simpler

### React Native <= 0.59
**Mostly automatic installation:**
```
react-native link react-native-mobigate
```
**Manual installation:**
<details>
<summary>Manually link the library on Android</summary>

`android/settings.gradle`
```groovy
include ':react-native-mobigate'
project(':react-native-mobigate').projectDir = new File(rootProject.projectDir, '../node_modules/react-native-mobigate/android')
```
`android/app/build.gradle`
```groovy
dependencies {
   ...
   implementation project(':react-native-mobigate')
}
```
`android/app/src/main/.../MainApplication.java`
<br />On top, where imports are:
```java
import pl.spicymobile.reactmobigate.MobigatePackage;
```
Add the MobigatePackage class to your list of exported packages.
```java
@Override
protected List<ReactPackage> getPackages() {
    return Arrays.<ReactPackage>asList(
        new MainReactPackage(), 
        new MobigatePackage()
    );
}
```

</details>

## SDK Initialization

## Guides
