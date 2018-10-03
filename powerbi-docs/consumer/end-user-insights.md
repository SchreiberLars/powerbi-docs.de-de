---
title: Automatisches Erstellen von Einblicken in Daten mit Power BI
description: Hier erfahren Sie, wie Sie Einblicke in Ihre Datasets und Dashboardkacheln erhalten.
author: mihart
manager: kvivek
ms.reviewer: ''
featuredvideoid: et_MLSL2sA8
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 05/25/2018
ms.author: mihart
LocalizationGroup: Dashboards
ms.openlocfilehash: be2f1997fe27878967ac22435c0a6dbe94ffc5a2
ms.sourcegitcommit: 70192daf070ede3382ac13f6001e0c8b5fb8d934
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/22/2018
ms.locfileid: "46565289"
---
# <a name="automatically-generate-data-insights-with-power-bi"></a>Automatisches Erstellen von Einblicken in Daten mit Power BI
Sie besitzen ein neues Dataset und wissen nicht, womit Sie beginnen sollen?  Sie müssen schnell ein Dashboard erstellen?  Sie möchten nach Einblicken suchen, die Sie möglicherweise übersehen haben?

Führen Sie schnelle Einblicke aus, um interessante interaktive Visualisierungen auf Grundlage Ihrer Daten zu generieren. Schnelle Einblicke können für ein gesamtes Dataset (schnelle Einblicke) oder eine bestimmte Dashboard-Kachel (bereichsbezogene Einblicke) ausgeführt werden. Sie können sogar Einblicke für einen Einblick ausführen.

> **HINWEIS:** Einblicke funktionieren nicht mit DirectQuery. Das Feature kann nur für in Power BI hochgeladene Daten verwendet werden.
> 

Das Feature „Einblicke“ basiert auf einer wachsenden Reihe [erweiterter analytischer Algorithmen](end-user-insight-types.md), die in Verbindung mit Microsoft Research entwickelt wurden. Wir möchten damit auch in Zukunft noch mehr Benutzern auf neue und intuitive Weise Einblicke in ihre Daten bieten.

## <a name="run-quick-insights-on-a-dataset"></a>Ausführen von schnellen Einblicken für ein Dataset
Lassen Sie sich von Amanda zeigen, wie Sie das Feature „Schnelle Einblicke“ auf ein Dataset anwenden, einen Einblick im Fokusmodus öffnen, einen der Einblicke als Kachel an das Dashboard anheften und dann Einblicke für eine Dashboardkachel abrufen.

<iframe width="560" height="315" src="https://www.youtube.com/embed/et_MLSL2sA8" frameborder="0" allowfullscreen></iframe>


Jetzt sind sie dran. Erkunden Sie Einblicke anhand des [Analysebeispiels für die Lieferantenqualität](../sample-supplier-quality.md).

1. Wählen Sie auf der Registerkarte **Datasets** die Auslassungspunkte (...) und dann **Einblicke erhalten** aus.
   
    ![Registerkarte „Datasets“](./media/end-user-insights/power-bi-ellipses.png)
   
    ![Das Menü mit Auslassungspunkten (...)](./media/end-user-insights/power-bi-tab.png)
2. Power BI verwendet [verschiedene Algorithmen](end-user-insight-types.md) zum Suchen nach Trends in Ihrem Dataset.
   
    ![Dialogfeld „Nach Erkenntnissen suchen“](./media/end-user-insights/pbi_autoinsightssearching.png)
3. Innerhalb von Sekunden sind Ihre Einblicke bereit.  Wählen Sie **Einblicke anzeigen** aus, um Visualisierungen anzuzeigen.
   
    ![Erfolgsmeldung](./media/end-user-insights/pbi_autoinsightsuccess.png)
   
   > **HINWEIS**: Einige Datasets können keine Einblicke generieren, da die Daten statistisch nicht signifikant sind.  Weitere Informationen finden Sie unter [Optimieren von Daten für Einblicke](../service-insights-optimize.md).
   > 
   > 
1. Die Visualisierungen werden in einem speziellen Bereich für **schnelle Einblicke** mit bis zu 32 getrennten Einblickkarten angezeigt. Jede Karte enthält ein Diagramm oder eine Grafik und eine kurze Beschreibung.
   
    ![Zeichenbereich „Schnelle Einblicke“](./media/end-user-insights/power-bi-insights.png)

## <a name="interact-with-the-insight-cards"></a>Interaktion mit Karten für Einblicke
  ![Anheften-Symbol](./media/end-user-insights/pbi_hover.png)

1. Zeigen Sie auf eine Karte, und wählen Sie das Anheftsymbol aus, um die Visualisierung einem Dashboard hinzuzufügen.
2. Halten Sie den Mauszeiger über eine Karte, wählen Sie die Auslassungspunkte (...) aus, und wählen Sie dann **Einblicke anzeigen** aus. Hiermit wird ein Einblick im Vollbildmodus geöffnet.
   
    ![Einblickvollbildmodus](./media/end-user-insights/power-bi-insight-focus.png)
3. In diesem Modus haben Sie folgende Möglichkeiten:
   
   * Filtern Sie die Visualisierungen.  Um die Filter anzuzeigen, wählen Sie in der oberen rechten Ecke das Pfeilsymbol aus, um den Filterbereich zu erweitern.
        ![Einblick im Menü „Filter“ erweitert](./media/end-user-insights/power-bi-insights-filter-new.png)
   * Heften Sie die Einblickkarte an ein Dashboard an, indem Sie auf das Stecknadelsymbol ![Stecknadelsymbol](./media/end-user-insights/power-bi-pin-icon.png) oder auf **Visual anheften** klicken.
   * Führen Sie Einblicke für die Karte selbst aus. Dies wird häufig auch als **bereichsbezogene Einblicke** bezeichnet. Klicken Sie in der oberen rechten Ecke auf das Glühbirnensymbol ![Glühbirnensymbol](./media/end-user-insights/power-bi-bulb-icon.png) oder auf **Einblicke erhalten**.
     
       ![Menüleiste mit dem Symbol „Einblicke erhalten“](./media/end-user-insights/pbi-autoinsights-tile.png)
     
     Der Einblick wird auf der linken Seite angezeigt, und neue Karten (ausschließlich abhängig von den Daten in diesem Einblick) werden rechts angezeigt.
     
       ![Einblicke in Einblicke](./media/end-user-insights/power-bi-insights-on-insights-new.png)
4. Wenn Sie zum Bereich für Einblicke zurückkehren möchten, wählen Sie links oben **Fokusmodus beenden** aus.

## <a name="run-insights-on-a-dashboard-tile"></a>Ausführen von Einblicken auf einer Dashboardkachel
Anstatt ein gesamtes Dataset nach Einblicken zu durchsuchen, können Sie die Suche auf die zum Erstellen einer einzelnen Dashboardkachel verwendeten Daten einschränken. Dies wird häufig als **bereichsbezogene Einblicke** bezeichnet.

1. Öffnen Sie ein Dashboard.
2. Zeigen Sie auf eine Kachel. Wählen Sie die Auslassungspunkte (...) und dann **Einblicke anzeigen** aus. Die Kachel wird im [Fokusmodus](end-user-focus.md) geöffnet. Die Einblickkarten werden rechts angezeigt.    
   
    ![Fokusmodus](./media/end-user-insights/pbi-insights-tile.png)    
4. Ist einer der Einblicke für Sie interessant? Wählen Sie die entsprechende Einblickkarte aus, um weitere Informationen zu erhalten. Der ausgewählte Einblick wird auf der linken Seite angezeigt, und neue Einblickkarten (ausschließlich abhängig von den Daten in diesem Einblick) werden rechts angezeigt.    
6. Schlüsseln Sie Ihre Daten weiter auf. Wenn Sie für Sie interessante Einblicke finden, können Sie sie an Ihr Dashboard anheften, indem Sie rechts oben auf **Visualisierung anheften** klicken.

## <a name="next-steps"></a>Nächste Schritte
Wenn Sie ein Dataset besitzen, können Sie es [für Schnelleinblicke optimieren](../service-insights-optimize.md).

Erfahren Sie mehr über die [Typen verfügbarer schneller Einblicke](end-user-insight-types.md).

Weitere Fragen? [Wenden Sie sich an die Power BI-Community](http://community.powerbi.com/)
