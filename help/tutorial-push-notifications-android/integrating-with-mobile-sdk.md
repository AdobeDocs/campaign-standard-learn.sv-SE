---
title: Steg 2 – integrera en mobil SDK
description: I den här delen integrerar vi Android-appen med Mobile SDK. Integrera mobil-SDK med Android-appen
feature: Push
kt: 4826
doc-type: tutorial
activity: use
team: TM
recommendations: noDisplay
exl-id: 0fa53536-8330-4e96-be2f-afc078609bcd
source-git-commit: 57dbf456625d22cd2e4526d92e5a8c20a048d339
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 3%

---

# STEG 2 - Integrera [!UICONTROL Mobile SDK] med Android-app

I den här delen kommer vi att integrera [!DNL Android] app med [!UICONTROL Mobile SDK]. Integrera [!UICONTROL mobile SDK] med [!DNL Android] app, följ följande steg:

* Öppna *ACSPushTutorial* projekt i [!DNL Android Studio]
* Skapa en ny java-klass som kallas *MainApp* som utökar [!DNL android.app.Application]
* Projektstrukturen bör nu se ut så här

![huvudprogram](assets/android-main-app.PNG)

* Expandera [!DNL Gradle Scripts] mapp. Dubbelklicka på [!DNL build.gradle] för modulen. Klistra in följande beroenden i beroendeavsnittet i [!DNL build.gradle] -fil. Dina [!DNL build.gradle] filen ska nu se ut så här

<!--
Removed `{.line-numbers}` below
-->

```java
implementation 'com.adobe.marketing.mobile:campaign:1.+'
implementation 'com.adobe.marketing.mobile:userprofile:1.+'
implementation 'com.adobe.marketing.mobile:sdk-core:1.+'
```

![modul-gradle](assets/module-build-gradle.PNG)

* Synkronisera [!DNL Android] genom att klicka på knappen Synkronisera nu för att synkronisera ditt projekt

## Ändra [!DNL AndroidManifest.xml]{#modify-android-manifest}

Öppna *AndroidManifest.xml* och klistra in följande två rader efter manifest-elementet och före application-elementet. Detta gör att appen kan kommunicera med andra användare

<!--
Removed `{.line-numbers}` below
-->

```xml
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```

Kopiera följande rad i elementet application
[!DNL android:name=".MainApp"]
Spara [!DNL AndroidManifest.xml]
Dina [!DNL AndroidManifest.xml] ser ut så här

<!--
Removed `{.line-numbers}` below
-->

```xml
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="com.example.acspushtutorial">
    <uses-permission android:name="android.permission.INTERNET" />
    <uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />

<application
    android:name=".MainApp"
    android:allowBackup="true"
    android:icon="@mipmap/ic_launcher"
    android:label="@string/app_name"
    android:roundIcon="@mipmap/ic_launcher_round"
    android:supportsRtl="true"
    android:theme="@style/AppTheme">

<activity android:name=".MainActivity">
<intent-filter>
    <action android:name="android.intent.action.MAIN" />
    <category android:name="android.intent.category.LAUNCHER" />
</intent-filter>
</activity>
</application>

</manifest>
```
