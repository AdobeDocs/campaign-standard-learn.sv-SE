---
title: Problem med att skjuta kontrollpanelen
description: På Kontrollpanelen kan du övervaka och hantera din SFTP-lagring per instans och vitlista med IP-adresser.
feature: Control Panel
topics: null
kt: 2938
doc-type: article
activity: use
team: PM
translation-type: tm+mt
source-git-commit: cb5d5bc58137fd374eafe165c6ea13288a60d7db
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---


# Det gick inte att skjuta [!UICONTROL-kontrollpanelen}

Lär dig hur du felsöker problem när du använder Kontrollpanelen.

## Inloggning och hemsida

Problem med inloggning och hemsida.

### Symptom: Det går inte att logga in på Adobe Experience Cloud

**Så här gör du:**
Användaren måste hitta sin [!DNL IMS Org ID] (xxx). Administratören måste lägga till användaren i [!UICONTROL product profile] för varje instans [!DNL “Campaign-xxx-Admins”] som han/hon vill hantera. Om användaren är administratör för alla instanser kan han eller hon fortfarande behöva lägga till sig själv som *[!UICONTROL user]*.

### Symptom: Länkarna i [!UICONTROL Adobe Experience Cloud Home] åtkomstfältet visas [!UICONTROL Control Panel] inte för en användare

**Orsak:**
Användarna ser inte länkarna förrän de läggs till som användare i [!UICONTROL product profile] `Campaign-xxx-Administrators/Admin`

**Så här gör du:**
Administratören måste lägga till användaren i [!UICONTROL product profile] för varje instans *[!DNL Campaign-xxx-Admins]* som han/hon vill hantera. Om användaren är administratör för alla instanser kan han eller hon fortfarande behöva lägga till sig själv som *[!UICONTROL user]*.

### Symptom: En instans visas inte i listan [!UICONTROL Control Panel]

**Orsak:**
Den mest troliga användaren måste läggas till som en *[!UICONTROL user]* produktprofil `!DNL Campaign-xxx-Administrators/Admin` för den instans som saknas

**Så här gör du:**
Administratören måste lägga till användaren i produktprofilen `Campaign-xxx-Admins` för varje instans som han/hon vill hantera. Om användaren är administratör för alla instanser kan han eller hon fortfarande behöva lägga till sig själv som *[!UICONTROL user]*.

### Användbara videor

>[!VIDEO](https://video.tv.adobe.com/v/27183?quality=12)
*Kontroll[!DNL IMS Org ID](00:26 min)*

>[!VIDEO](https://video.tv.adobe.com/v/27147?quality=12)
*Så här lägger du till en administratör i[!UICONTROL product profile]för *[!DNL administrators]*att kunna använda[!UICONTROL Control Panel](01:03 min)*

### Användbar dokumentation

* [Upptäck [!UICONTROL-kontrollpanelen]](https://helpx.adobe.com/campaign/kb/control-panel-overview.html)
* [Hantera behörigheter för [!UICONTROL-kontrollpanelen]](https://helpx.adobe.com/campaign/kb/control-panel-access.html)

## Upprättar anslutning till SFTP-server (klient eller API)

Anslutning till SFTP-servrar kräver:

* [!UICONTROL Whitelisting] IP-adressen som du ansluter till SFTP-servern från
* Privat/offentlig nyckel som måste registreras med Adobe Campaign
* Om du ansluter till SFTP-servern direkt behöver du också SFTP-klientprogramvara

### Användbar dokumentation

* [Logga in på SFTP-servern](https://helpx.adobe.com/campaign/kb/control-panel-sftp.html#LoggingintoyourSFTPserver)
