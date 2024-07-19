---
title: Steg 3 – registrera tillägg i din mobilapp
description: I den här delen lägger vi till koden för att registrera tilläggen UserProfile, Identity, Lifecycle och Signal.
feature: Push
user: Admin
level: Experienced
jira: KT-4827
doc-type: tutorial
activity: use
team: TM
exl-id: d8c0d8c6-2e04-4c27-b27a-d0de79dd953b
source-git-commit: 9be31e056800b806c49a2c5ffbf9f9f42b001d4c
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 14%

---

# Steg 3 – registrera tillägg i din mobilapp

I den här delen lägger vi till koden för att registrera tilläggen Användarprofil, Identitet, Livscykel och Signal. Vi måste också registrera Adobe Campaign Standard-tillägget enligt koden nedan.

Öppna ditt projekt i [!DNL Android] studio. Ta bort hela koden i MainApp **förutom den första raden som är din paketsats**.

Klistra in följande kod i MainApp

<!--
Removed `{.line-numbers}` below
-->

```java
import [!DNL android].app.Application;
import android.util.Log;

import com.adobe.marketing.mobile.AdobeCallback;
import com.adobe.marketing.mobile.Campaign;
import com.adobe.marketing.mobile.Identity;
import com.adobe.marketing.mobile.InvalidInitException;
import com.adobe.marketing.mobile.Lifecycle;
import com.adobe.marketing.mobile.LoggingMode;
import com.adobe.marketing.mobile.MobileCore;
import com.adobe.marketing.mobile.Signal;
import com.adobe.marketing.mobile.UserProfile;

public class MainApp extends Application {

@Override
public void onCreate() {
super.onCreate();

MobileCore.setApplication(this);
MobileCore.setLogLevel(LoggingMode.DEBUG);

try{
    Campaign.registerExtension();
    UserProfile.registerExtension();
    Identity.registerExtension();
    Lifecycle.registerExtension();
    Signal.registerExtension();
    MobileCore.start(new AdobeCallback () {
        @Override
        public void call(Object o) {
            MobileCore.configureWithAppID("copy your launch property id here");
        }
    });
} catch (InvalidInitException e) {
    Log.d("ACS Exception", "exception");
}
}
}
```

Rad 32 måste du ange [!UICONTROL  Launch]-egenskapens miljöfil-ID. Den här informationen kan nås från [!UICONTROL environment tab] för din [!UICONTROL Launch]-egenskap.

![launch-id](assets/launch-id-property.PNG)
