---
title: Power BI-URLs
description: In diesem Artikel werden die Endpunkte beschrieben, die für Power BI-Kunden zugänglich sein sollten.
author: mgblythe
ms.author: mblythe
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 10/22/2018
ms.openlocfilehash: e62d39f13e2b171456d667ec9683acd4ebdc5516
ms.sourcegitcommit: 46f1ba3f972f6e64bce05ad0fd527b27c49aedd6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2018
ms.locfileid: "52157124"
---
# <a name="power-bi-urls"></a>Power BI-URLs

**Der Power BI-Onlinedienst**, auch als SaaS-App von Power BI bezeichnet, erfordert eine Verbindung mit dem Internet. Die unten aufgeführten Endpunkte sollten für Kunden, die den Power BI-Onlinedienst verwenden, erreichbar sein.

Um den Online-Dienst in Power BI zu verwenden, müssen Sie Verbindungen zu den in den Tabellen unten als **erforderlich** und auf den verknüpften Websites als **erforderlich** markierten Endpunkten herstellen können. Wenn sich der Link zu einer externen Website auf einen bestimmten Abschnitt bezieht, müssen Sie in diesem Abschnitt nur die Endpunkte überprüfen.

Endpunkte, die als **optional** markiert sind, können **auf die Whitelist gesetzt werden**, wenn die Nutzung bestimmter Funktionen erforderlich ist.

Der Power BI-Onlinedienst setzt nur voraus, dass für die aufgeführten Endpunkte der TCP-Port 443 geöffnet wird.

Platzhalter (*) stellen alle Ebenen unterhalb der Stammdomäne dar, und N/V wird verwendet, wenn keine Informationen verfügbar sind. Die Spalte **Ziel(e)** ist eine Liste mit FQDN/Domänen und Links zu externen Websites, die weitere Informationen zu den Endpunkten enthalten.

>[!Important]
>Die Informationen in den Tabellen unten gelten nicht für die  **Government Cloud**, **die Cloud Deutschland** oder **die Cloud China**.

## <a name="authentication"></a>Authentifizierung

Power BI ist auf die verschiedenen Endpunkte in den Office 365-Abschnitten zur Authentifizierung und Identität angewiesen. Zum Verwenden von Power BI müssen Sie eine Verbindung zu den Endpunkten herstellen können, die auf der unten verknüpften Website aufgeführt sind.

| Zeile | Zweck | Ziel(e) | Port(s) |
| --- | --- | --- | --- |
| 1 | **Erforderlich**: Authentifizierung und Identität | In der Office 365-Dokumentation finden Sie [allgemeine und Office Online-URLs](https://docs.microsoft.com/office365/enterprise/urls-and-ip-address-ranges#microsoft-365-common-and-office-online).  | N/V |

## <a name="general-site-usage"></a>Allgemeine Verwendung der Website

Für die allgemeine Verwendung von Power BI müssen Sie eine Verbindung zu den in der Tabelle aufgeführten Endpunkten und zu den Endpunkten, die auf den verknüpften Websites aufgeführt sind, herstellen können.

| Zeile | Zweck | Ziel(e) | Port(s) |
| --- | --- | --- | --- |
| 1 | **Erforderlich**: Backend-APIs | *.analysis.windows.net | TCP 443 |
| 2 | **Erforderlich**: Office 365-Integration | In der Office 365-Dokumentation finden Sie [allgemeine und Office Online-URLs](https://docs.microsoft.com/office365/enterprise/urls-and-ip-address-ranges#microsoft-365-common-and-office-online). | N/V |
| 3 | **Erforderlich**: Portal | app.powerbi.com | TCP 443 |
| 4 | **Erforderlich**: Diensttelemetrie | dc.services.visualstudio.com | TCP 443 |
| 5 | **Optional**: Informationsmeldungen | dynmsg.modpim.com | TCP 443 |
| 6 | **Optional**: NPS-Umfragen | nps.onyx.azure.net | TCP 443 |
| | | |

## <a name="administration"></a>Verwaltung

Zum Ausführen administrativer Funktionen in Power BI müssen Sie eine Verbindung zu den Endpunkten auf den unten verknüpften Websites herstellen können.

| Zeile | Zweck | Ziel(e) | Port(s) |
| --- | --- | --- | --- |
| 1 | **Erforderlich**: Zum Verwalten von Benutzern und Anzeigen von Überwachungsprotokollen | In der Office 365-Dokumentation finden Sie [allgemeine und Office Online-URLs](https://docs.microsoft.com/office365/enterprise/urls-and-ip-address-ranges#microsoft-365-common-and-office-online). | N/V |
| | | |

## <a name="getting-data"></a>Abrufen von Daten

Zum Abrufen von Daten aus bestimmten Datenquellen wie OneDrive müssen Sie eine Verbindung zu den Endpunkten unten in der Tabelle herstellen können. Es kann sein, dass der Zugriff auf zusätzliche Internetdomänen und URLs für bestimmte Datenquellen erforderlich ist, die in Ihrer Organisation verwendet werden.

| Zeile | Zweck | Ziel(e) | Port(s) |
| --- | --- | --- | --- |
| 1 | **Erforderlich**: AppSource (interne oder externe Apps in Power BI) | appsource.microsoft.com </br> *.s-microsoft.com  | TCP 443 |
| 2 | **Optional:** Melden Sie sich an, und rufen Sie Daten für Inhaltspakete ab | Von verwendeten Inhaltspaketen abhängig | Von verwendeten Inhaltspaketen abhängig |
| 3 | **Optional**: Importieren von Dateien aus OneDrive (privat) | Weitere Informationen finden Sie auf der Website [Required URLs and ports for OneDrive site (Erforderliche URLs und Ports für OneDrive)](https://docs.microsoft.com/onedrive/required-urls-and-ports). | N/V |
| 4 | **Optional**: Power BI in 60 Sekunden, Videotutorial | *.doubleclick.net </br> *.ggpht.com </br> *.google.com </br> *.googlevideo.com </br> *.youtube.com </br> *.ytimg.com </br> fonts.gstatic.com | TCP 443 |
| 5 | **Optional**: PubNub-Streamingdatenquellen | Weitere Informationen finden Sie in der [PubNub-Dokumentation](https://support.pubnub.com/support/solutions/articles/14000043522). | N/V |
| | | |

## <a name="dashboard-and-report-integration"></a>Dashboard- und Berichtsintegration

Zur Unterstützung von Dashboards und Berichten ist Power BI auf bestimmte Endpunkte angewiesen. Sie müssen eine Verbindung zu den Endpunkten in der Tabelle und den unten verknüpften Websites herstellen können.

| Zeile | Zweck | Ziel(e) | Port(s) |
| --- | --- | --- | --- |
| 1 | **Erforderlich**: Excel-Integration | In der Office 365-Dokumentation finden Sie [allgemeine und Office Online-URLs](https://docs.microsoft.com/office365/enterprise/urls-and-ip-address-ranges#microsoft-365-common-and-office-online). | N/V |
| | | |

## <a name="custom-visuals"></a>Benutzerdefinierte Visuals

Power BI ist auf bestimmte Endpunkte angewiesen, um benutzerdefinierte Visuals anzeigen und darauf zugreifen zu können. Sie müssen eine Verbindung zu den Endpunkten in der Tabelle und den unten verknüpften Websites herstellen können.

| Zeile | Zweck | Ziel(e) | Port(s) |
| --- | --- | --- | --- |
| 1 | **Erforderlich**: Importieren eines benutzerdefinierten Visuals über die Marketplace-Schnittstelle und aus einer Datei | *.azureedge.net </br> *.blob.core.windows.net </br> store.office.com | TCP 443 |
| 2 | **Optional**: Bing Karten | bing.com </br> platform.bing.com </br> *.dynamic.tiles.virtualearth.net </br> *.virtualearth.net | TCP 443 |
| 3 | **Optional**: PowerApps | Weitere Informationen finden Sie im Abschnitt [Erforderliche Dienste](https://docs.microsoft.com/powerapps/maker/canvas-apps/limits-and-config#required-services) auf der Website mit den PowerApps-Systemanforderungen. | N/V |
| 4 | **Optional**: Visio | In der Office 365-Dokumentation finden Sie [allgemeine und Office Online-URLs](https://docs.microsoft.com/office365/enterprise/urls-and-ip-address-ranges#microsoft-365-common-and-office-online) sowie [URLs von SharePoint Online und OneDrive for Business](https://docs.microsoft.com/office365/enterprise/urls-and-ip-address-ranges#sharepoint-online-and-onedrive-for-business). | N/V |
| | | |

## <a name="related-external-sites"></a>Verwandte externe Websites

Power BI verlinkt zu verwandten Websites. Das können z.B. Dokumentationen, Supportwebsites oder Websites für Anforderungen neuer Features sein. Diese Websites wirken sich nicht auf die Funktionalität von Power BI aus und können deshalb optional einer Whitelist hinzugefügt werden.

| Zeile | Zweck | Ziel(e) | Port(s) |
| --- | --- | --- | --- |
| 1 | **Optional:** Communitywebsite | community.powerbi.com </br> oxcrx34285.i.lithium.com | TCP 443 |
| 2 | **Optional:** Dokumentationswebsite | docs.microsoft.com </br> img-prod-cms-rt-microsoft-com.akamaized.net </br> statics-uhf-eas.akamaized.net </br> cdnssl.clicktale.neting-district.clicktale.net | TCP 443 |
| 3 | **Optional:** Downloadwebsite (für Power BI Desktop usw.) | download.microsoft.com | TCP 443 |
| 4 | **Optional:** Externe Weiterleitungen | aka.ms </br> go.microsoft.com | TCP 443 |
| 5 | **Optional:** Website für Vorschläge| ideas.powerbi.com </br> powerbi.uservoice.com | TCP 443 |
| 6 | **Optional:** Power BI-Website: Landing Page, Links zu weiteren Informationen, Supportwebsite, Downloadlinks, Partnershowcases usw. | powerbi.microsoft.com | TCP 443 |
| 7 | **Optional:** Power BI Developer Center | dev.powerbi.com | TCP 443 |
| 8 | **Optional:** Supportwebsite | support.powerbi.com </br> s3.amazonaws.com </br> *.olark.com </br> logx.optimizely.com </br> mscom.demdex.net </br> tags.tiqcdn.com | TCP 443 |
| | | |