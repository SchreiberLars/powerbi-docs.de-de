---
title: Herstellen einer Verbindung mit Microsoft Azure Consumption Insights mithilfe von Power BI
description: Microsoft Azure Consumption Insights für Power BI
author: SarinaJoan
manager: kfile
ms.reviewer: maggies
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 10/16/2017
ms.author: sarinas
LocalizationGroup: Connect to services
ms.openlocfilehash: 987b6998823119fa8aa85d2aabe4d37608a6a671
ms.sourcegitcommit: 0ff358f1ff87e88daf837443ecd1398ca949d2b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/21/2018
ms.locfileid: "46549866"
---
# <a name="connect-to-microsoft-azure-consumption-insights-with-power-bi"></a>Herstellen einer Verbindung mit Microsoft Azure Consumption Insights mithilfe von Power BI
Untersuchen und überwachen Sie Ihre Microsoft Azure-Nutzungsdaten in Power BI mit dem Power BI-Inhaltspaket. Die Daten werden automatisch einmal täglich aktualisiert.

Stellen Sie eine Verbindung mit dem [Microsoft Azure Consumption Insights-Inhaltspaket](https://app.powerbi.com/getdata/services/azureconsumption) für Power BI her.

## <a name="how-to-connect"></a>Herstellen der Verbindung
1. Wählen Sie unten im linken Navigationsbereich **Daten abrufen** aus.
   
    ![](media/service-connect-to-azure-consumption-insights/getdata.png)
2. Wählen Sie im Feld **Dienste** die Option **Abrufen**aus.
   
   ![](media/service-connect-to-azure-consumption-insights/services.png)
3. Wählen Sie **Microsoft Azure Consumption Insights-Inhaltspaket** \> **Abrufen** aus. 
   
   ![](media/service-connect-to-azure-consumption-insights/mazureconsumption.png)
4. Geben Sie die Anzahl der Monate, für die Sie Daten importieren möchten, und Ihre Azure Enterprise-Registrierungsnummer ein. Nachstehend finden Sie weitere Informationen zum [Suchen dieser Parameter](#FindingParams).
   
    ![](media/service-connect-to-azure-consumption-insights/azureconsumptionparams.png)
5. Geben Sie zum Herstellen der Verbindung Ihren Zugriffsschlüssel ein. Den Schlüssel für Ihre Registrierung finden Sie in Ihrem Azure EA-Portal. 
   
    ![](media/service-connect-to-azure-consumption-insights/msazureconsumptioncreds.png)
6. Der Importvorgang startet automatisch. Nach Abschluss des Vorgangs werden im Navigationsbereich ein neues Dashboard, ein Bericht und ein Modell angezeigt. Wählen Sie das Dashboard aus, um die importierten Daten anzuzeigen.
   
   ![](media/service-connect-to-azure-consumption-insights/msazureconsumptiondashboard.png)

**Was nun?**

* Versuchen Sie, am oberen Rand des Dashboards [im Q&A-Feld eine Frage zu stellen](consumer/end-user-q-and-a.md).
* [Ändern Sie die Kacheln](service-dashboard-edit-tile.md) im Dashboard.
* [Wählen Sie eine Kachel aus](consumer/end-user-tiles.md), um den zugrunde liegenden Bericht zu öffnen.
* Zwar ist Ihr Dataset auf tägliche Aktualisierung festgelegt, jedoch können Sie das Aktualisierungsintervall ändern oder über **Jetzt aktualisieren** nach Bedarf aktualisieren.

## <a name="whats-included"></a>Inhalt
Das Microsoft Azure Consumption Insights-Inhaltspaket enthält monatliche Berichtsdaten für den Bereich der Monate, den Sie während des Verbindungsflows angeben. Der Bereich ist ein bewegliches Fenster, sodass die enthaltenen Datumgangaben bei Aktualisierung des Datasets aktualisiert werden.

## <a name="system-requirements"></a>Systemanforderungen
Das Inhaltspaket erfordert Zugriff auf die Enterprise-Features im Azure-Portal. 

<a name="FindingParams"></a>

## <a name="finding-parameters"></a>Suchen von Parametern
Die Power BI-Berichterstellung steht für direkte EA, Partner und indirekte Kunden zur Verfügung, die Abrechnungsinformationen anzeigen können. Im folgenden Abschnitt finden Sie Informationen dazu, wie Sie die zum Herstellen der Verbindung erforderlichen Werte ermitteln können.

**Anzahl Monate**

* Dies sollte eine Zahl zwischen 1 und 36 sein, die die Anzahl der Monate (ab heute) darstellt, für die Sie Daten importieren möchten.

**Registrierungsnummer**

* Dies ist Ihre Azure Enterprise-Registrierungsnummer, die sich auf dem Startbildschirm des [Azure Enterprise-Portals](https://ea.azure.com/) unter „Registrierungsdetails“ befindet.
  
    ![](media/service-connect-to-azure-consumption-insights/params2.png)

**Zugriffsschlüssel**

* Ihren Schlüssel finden Sie im Azure Enterprise Portal unter „Nutzung herunterladen“ > „API-Zugriffsschlüssel“.
  
    ![](media/service-connect-to-azure-consumption-insights/creds2.png)

**Zusätzliche Hilfe**

* Um zusätzliche Hilfe zum Einrichten des Azure Enterprise Power BI-Pakets zu erhalten, melden Sie sich am Azure Enterprise-Portal an, um unter „Hilfe“ die API-Hilfedatei sowie weitere Anweisungen unter „Berichte -> Nutzung herunterladen -> API-Zugriffsschlüssel“ anzuzeigen. 

## <a name="next-steps"></a>Nächste Schritte
[Erste Schritte mit Power BI](service-get-started.md)

[Abrufen von Daten in Power BI](service-get-data.md)

