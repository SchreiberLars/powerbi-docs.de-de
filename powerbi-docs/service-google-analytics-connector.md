---
title: 'Drittanbieterdienst: Google Analytics-Connector für Power BI Desktop'
description: 'Drittanbieterdienst: Google Analytics-Connector für Power BI Desktop'
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 11/28/2018
ms.author: davidi
LocalizationGroup: Connect to data
ms.openlocfilehash: a0c98a8f65529575cb70fccec927c1ee00d9a089
ms.sourcegitcommit: 2ae660a7b70fce23eb58b159d049eca44a664f2c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/30/2018
ms.locfileid: "52669426"
---
# <a name="google-analytics-connector-for-power-bi-desktop"></a>Google Analytics-Connector für Power BI Desktop
> [!NOTE]
> Das Google Analytics-Inhaltspaket und der Connector in Power BI Desktop basieren auf der Google Analytics Core Reporting-API. Daher können Funktionen und Verfügbarkeit im Laufe der Zeit variieren.
> 
> 

Sie können mithilfe des **Google Analytics**-Connectors eine Verbindung zu Google Analytics-Daten herstellen. Gehen Sie dazu folgendermaßen vor:

1. Wählen Sie in **Power BI Desktop** auf der Registerkarte des Menübands **Start** den Eintrag **Daten abrufen**.
2. Wählen Sie im Fenster **Daten abrufen** aus den Kategorien im linken Bereich **Onlinedienste**.
3. Wählen Sie **Google Analytics** aus der Auswahl im rechten Bereich aus.
4. Wählen Sie am unteren Rand des Fensters **Verbinden**aus.  
   ![](media/service-google-analytics-connector/tps_googleanalytics_1.png)

Es erscheint ein Dialogfeld, in dem neben anderen Klarstellungen erläutert wird, dass der Connector ein Dienst von Drittanbietern ist, und in dem davor gewarnt wird, wie Funktionen und Verfügbarkeit sich im Laufe der Zeit ändern können.  
![](media/service-google-analytics-connector/tps_googleanalytics_2.png)

Wenn Sie **Weiter** wählen, werden Sie dazu aufgefordert, sich bei Google Analytics anzumelden.  
![](media/service-google-analytics-connector/tps_googleanalytics_3.png)

Wenn Sie Ihre Anmeldeinformationen eingeben, wird Ihnen mitgeteilt, dass Power BI den Offlinezugriff möchte. So nutzen Sie **Power BI Desktop** zum Zugriff auf Ihre Google Analytics-Daten.  

Sobald Sie dies akzeptiert haben, zeigt **Power BI Desktop** an, dass Sie derzeit angemeldet sind.  
![](media/service-google-analytics-connector/tps_googleanalytics_5.png)

Wählen Sie **Verbinden**. Ihre Google Analytics-Daten sind mit **Power BI Desktop** verbunden, und die Daten werden geladen.  
![](media/service-google-analytics-connector/tps_googleanalytics_6.png)

## <a name="changes-to-the-api"></a>Änderungen an der API
Obwohl wir versuchen, gemäß allen Änderungen Updates zu veröffentlichen, könnte die API so abgeändert werden, dass sich dies auf die Ergebnisse der generierten Abfragen auswirkt. In einigen Fällen könnten bestimmte Abfragen nicht mehr unterstützt werden. Aufgrund dieser Abhängigkeit können wir die Ergebnisse Ihrer Abfragen nicht garantieren, wenn Sie diesen Connector verwenden.

Weitere Informationen zu Änderungen an der Google Analytics-API finden Sie im [Änderungsprotokoll](https://developers.google.com/analytics/devguides/changelog).

