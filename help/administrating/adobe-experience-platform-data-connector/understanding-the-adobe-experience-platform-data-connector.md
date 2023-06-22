---
title: Förstå Adobe Experience Platform Data Connector
description: Adobe Experience Platform Data Connector hjälper befintliga kunder att göra sina data tillgängliga på Adobe Experience Platform genom att mappa XTK-data (data som importerats i Campaign) till Experience Data Model-data (XDM) på Adobe Experience Platform.
feature: People Core Service Integration
jira: KT-2826
thumbnail: 27304.jpg
doc-type: feature video
activity: understand
team: TM
exl-id: 686961f9-5374-4cc6-8b36-7ee0584ea720
source-git-commit: c84867ef59a10448a377a959d0b67ae71343a4aa
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 4%

---

# Förstå Adobe Experience Platform [!UICONTROL Data Connector]

>[!NOTE]
>
>Funktionen är i betaversion och kan uppdateras ofta och ändras utan föregående meddelande.
>
>Kontakta [!UICONTROL Adobe Customer Support] om du tänker implementera den här funktionen.

## Översikt

Adobe Experience Platform [!UICONTROL Data Connector] hjälper befintliga kunder att göra sina data tillgängliga på Adobe Experience Platform genom att mappa XTK-data (data som hämtas i Adobe Campaign) till [!DNL Experience Data Model] (XDM) på Adobe Experience Platform.

Kopplingen är enkelriktad och skickar data från Adobe Campaign Standard till Adobe Experience Platform. Data skickas aldrig från Adobe Experience Platform till Adobe Campaign Standard.

Adobe Experience Platform [!UICONTROL Data Connector] är avsett för datatekniker som förstår Adobe Campaign Standard [!UICONTROL custom resources] och ha en förståelse för hur kundens övergripande dataschema ska vara inuti Adobe Experience Platform.

>[!VIDEO](https://video.tv.adobe.com/v/27304?quality=12&learn=on)

*Den här videon ger en översikt över Adobe Experience Platform [!UICONTROL Data Connector] (09:35 min)*

>[!NOTE]
>
>Enkel överföring av [!UICONTROL subscription events] stöds inte. Till överföring [!UICONTROL subscription events]kan du skapa motsvarande XDM och datauppsättning på Adobe Experience Platform och sedan konfigurera en anpassad datamappning för dessa data.
>
>Befintlig [!UICONTROL experience events] kan inte importeras till Adobe Experience Platform, men pågående generering [!UICONTROL experience events] strömmas till Adobe Experience Platform.

## Viktiga steg för datamappning

I följande självstudier beskrivs de viktigaste stegen för att utföra en datamappning mellan Campaign Standard och Adobe Experience Platform:

1. [Mappa anpassade resurser](/help/administrating/adobe-experience-platform-data-connector/mapping-custom-resources.md)
2. [Kartlägga upplevelsehändelser](/help/administrating/adobe-experience-platform-data-connector/mapping-experience-events.md)
3. [Mappa starttabelldata](/help/administrating/adobe-experience-platform-data-connector/mapping-seed-table-data.md)
4. [Ändra datamappningen](/help/administrating/adobe-experience-platform-data-connector/modifying-data-mapping.md)
5. [Kontrollera statusen för ett datainmatningsjobb](/help/administrating/adobe-experience-platform-data-connector/checking-status-of-data-ingestion-jobs.md)

