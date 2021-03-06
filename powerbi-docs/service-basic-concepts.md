---
title: Grundlegende Konzepte für Designer im Power BI-Dienst
description: Arbeitsbereiche, Dashboards, Berichte, Datasets und Arbeitsmappen im Power BI-Dienst.
author: maggiesMSFT
manager: kfile
ms.reviewer: ''
featuredvideoid: B2vd4MQrz4M
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 11/21/2018
ms.author: maggies
LocalizationGroup: Get started
ms.openlocfilehash: d18c44724899b243a34821db4d4866863e577b48
ms.sourcegitcommit: 35d763dfc75c229204d36fd8b35c1e860786b707
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/27/2018
ms.locfileid: "52332032"
---
# <a name="basic-concepts-for-designers-in-the-power-bi-service"></a>Grundlegende Konzepte für Designer im Power BI-Dienst

In diesem Artikel wird davon ausgegangen, dass Sie sich bereits [für den Power BI-Dienst registriert](service-self-service-signup-for-power-bi.md) und [Daten hinzugefügt](service-get-data.md) haben. Wenn Sie noch keine Daten hinzugefügt haben, können Sie ein [Beispielinhaltspaket für Power BI](sample-datasets.md#the-power-bi-samples-as-content-packs) installieren.

Wenn Sie den Power BI-Dienst öffnen, wird ein **_Dashboard_** angezeigt. Dashboards unterscheiden den Power BI-Dienst von Power BI Desktop.

![Der Power BI-Dienst in einem Browser](media/service-basic-concepts/completenewest.png)

Im Folgenden werden die wichtigsten Features der Benutzeroberfläche des Power BI-Diensts aufgeführt:

1. Navigationsbereich (linker Navigationsbereich)
2. Zeichenbereich (in diesem Fall Dashboard mit Kacheln)
3. Fragenfeld für Fragen und Antworten (F&A)
4. Symbolschaltflächen, einschließlich Hilfe und Feedback
5. Dashboardtitel (Navigationspfad oder Breadcrumbs)
6. Office 365-App-Startfeld
7. Power BI-Schaltfläche „Start“
8. Beschriftete Symbolschaltflächen

Diese Features werden später näher erläutert. Zunächst werden einige Grundkonzepte von Power BI besprochen.

Sie können sich auch erst dieses Video ansehen und dann den Rest des Artikels lesen.  In diesem Video gibt Will einen Überblick über den Power BI-Dienst und erklärt die grundlegenden Konzepte.

<iframe width="560" height="315" src="https://www.youtube.com/embed/B2vd4MQrz4M" frameborder="0" allowfullscreen></iframe>


## <a name="power-bi-concepts"></a>Power BI-Konzepte
Die vier wichtigsten Grundkomponenten von Power BI sind: **_Dashboards_**, **_Berichte_**, **_Arbeitsmappen_** und **_Datasets_**. Diese sind in **_Arbeitsbereichen_** angeordnet. Zunächst sollen Arbeitsbereiche erläutert werden, bevor näher auf die vier Grundkomponenten eingegangen wird.

## <a name="workspaces"></a>Arbeitsbereiche
Arbeitsbereiche sind Container für Dashboards, Berichte, Arbeitsmappen und Datasets in Power BI. Es gibt zwei Arten von Arbeitsbereichen: *Mein Arbeitsbereich* und *App-Arbeitsbereiche*. Was genau ist eine *App*? Eine Power BI-*App* ist eine Sammlung von Dashboards und Berichten, die erstellt wurden, um Schlüsselmetriken für Ihre Organisation bereitzustellen. Apps sind interaktiv, können jedoch nicht bearbeitet werden.

- *Mein Arbeitsbereich* ist der persönliche Arbeitsbereich jedes Power BI-Kunden, in dem Sie Ihre eigenen Inhalte bearbeiten. Nur Sie haben Zugriff auf Ihren „Mein Arbeitsbereich“. Sie können Dashboards und Berichte von Ihrem Arbeitsbereich aus freigeben. Wenn Sie in Dashboards und Berichte mit anderen Personen zusammenarbeiten oder eine App erstellen möchten, sollten Sie einen App-Arbeitsbereich verwenden.      
-  *App-Arbeitsbereiche* werden für die Zusammenarbeit und die Freigabe von Inhalten für Kollegen verwendet. Darüber sind hinaus werden hier Apps für Ihre Organisation erstellt, veröffentlicht und verwaltet. Betrachten Sie sie als eine Art Bereitstellungsraum und Container für Ihre Inhalte, die eine Power BI-App bilden. Sie können Ihren App-Arbeitsbereichen Kollegen hinzufügen und gemeinsam an Dashboards, Berichten, Arbeitsmappen und Datasets arbeiten. Alle Mitglieder des App-Arbeitsbereichs benötigen Power BI Pro-Lizenzen, für App-Anwender (Kollegen, die Zugriff auf die Apps haben) sind Pro-Lizenzen jedoch nicht zwingend erforderlich.  

Weitere Informationen finden Sie im Abschnitt **Freigeben Ihrer Arbeit** des Inhaltsverzeichnisses ab dem Thema [Wie kann ich Dashboards und Berichte freigeben?](service-how-to-collaborate-distribute-dashboards-reports.md)


Nun zu den Grundkomponenten von Power BI. Sie können keine Dashboards oder Berichte ohne Daten erstellen (es können zwar leere Dashboards und Berichte verwendet werden, diese wären jedoch nicht nützlich). Beginnen wir also mit **Datasets**.

## <a name="datasets"></a>Datasets
Ein *Dataset* ist eine Sammlung von Daten, die Sie *importieren* oder mit denen Sie eine *Verbindung herstellen*. In Power BI können Sie Verbindungen mit allen Arten von Datasets herstellen, sie importieren und zentral anordnen.  

Datasets sind *Arbeitsbereichen* zugeordnet, und ein einzelnes Dataset kann Teil mehrerer Arbeitsbereiche sein. Wenn Sie einen Arbeitsbereich öffnen, werden die zugeordneten Datasets auf der Registerkarte **Datasets** aufgeführt. Jedes aufgelistete Dataset stellt eine einzelne Datenquelle dar, z. B. eine Excel-Arbeitsmappe auf OneDrive oder ein lokales tabellarisches SSAS-Dataset oder ein Salesforce-Dataset. Es werden viele verschiedene Datenquellen unterstützt, zu denen beständig neue Datenquellen hinzugefügt werden. [Hier finden Sie eine Liste der Datasettypen, die mit Power BI verwendet werden können](service-get-data.md).

Im folgenden Beispiel ist die App „Vertrieb und Marketing“ ausgewählt, und es wurde auf die Registerkarte **Datasets** geklickt.

![Ausgewählte Datasets](media/service-basic-concepts/power-bi-datasets.png)

**EIN** Dataset...

* kann beliebig oft in einem oder mehreren verschiedenen Arbeitsbereichen verwendet werden.
* kann in vielen verschiedenen Berichten verwendet werden.
* Visualisierungen dieses einen Datasets können auf vielen verschiedenen Dashboards angezeigt werden.

  ![Diagramm der Datasets](media/service-basic-concepts/drawing2.png)

Wählen Sie **Daten abrufen** (am unteren Rand der linken Navigationsleiste) oder wählen Sie **+ Erstellen > Datasets** (in der rechten oberen Ecke) aus, um die [Verbindung mit einem Dataset herzustellen oder es zu importieren](service-get-data.md). Befolgen Sie die Anweisungen zum Herstellen einer Verbindung mit der jeweiligen Quelle bzw. zum Importieren, und fügen Sie das Dataset dem aktiven Arbeitsbereich hinzu. Neue Datasets werden mit einem gelben Sternchen markiert. Das zugrunde liegende Dataset wird durch Ihre Arbeit in Power BI nicht verändert.

Wenn Sie [zu einem **_App Arbeitsbereich_**](service-collaborate-power-bi-workspace.md) gehören, sind Datasets, die von einem Arbeitsbereichsmitglied hinzugefügt wurden, für die anderen Arbeitsbereichsmitglieder verfügbar.

Datasets können aktualisiert, umbenannt, untersucht und entfernt werden. Verwenden Sie ein Dataset, um einen völlig neuen Bericht zu erstellen, oder führen Sie [Schnelleinblicke](service-insights.md) aus.  Wählen Sie **Verwandte Inhalte anzeigen**, um zu erfahren, welche Berichte und Dashboards ein Dataset bereits verwenden. Wählen Sie ein Dataset aus, um es zu untersuchen. Tatsächlich öffnen Sie das Dataset im Berichts-Editor, wo Sie beginnen können, die Daten zu untersuchen und Visualisierungen zu erstellen. Fahren wir also mit dem nächsten Thema fort – Berichte.

### <a name="dig-deeper"></a>Weiterführende Themen
* [Was ist Power BI Premium?](service-premium.md)
* [Abrufen von Daten in Power BI](service-get-data.md)
* [Beispieldatasets für Power BI](sample-datasets.md)

## <a name="reports"></a>Berichte
Bei einem Power BI-Bericht handelt es sich um eine oder mehrere Seiten mit Visualisierungen (Diagramme und Grafiken wie Liniendiagramme, Kreisdiagramme, Treemaps usw.). Visualisierungen werden auch als **_visuelle Elemente oder Visuals_** bezeichnet. Alle Visualisierungen in einem Bericht stammen aus einem einzelnen Dataset. Berichte können in Power BI von Grund auf neu erstellt werden. Ebenso können sie mit Dashboards importiert werden, die Kollegen für Sie freigeben. Zudem können Berichte erstellt werden, wenn Sie eine Verbindung mit Datasets aus Excel, Power BI Desktop, Datenbanken, SaaS-Anwendungen und [Apps](service-get-data.md) herstellen.  Wenn Sie z. B. eine Verbindung mit einer Excel-Arbeitsmappe herstellen, die Power View-Tabellen enthält, dann erstellt Power BI einen Bericht auf Basis dieser Tabellen. Und wenn Sie eine Verbindung mit einer SaaS-Anwendung herstellen, wird ein vorgefertigter Bericht von Power BI importiert.

Es gibt zwei Modi, um Berichte anzuzeigen und mit ihnen zu interagieren: [die Leseansicht und die Bearbeitungsansicht](service-reading-view-and-editing-view.md).  Nur der Ersteller des Berichts, die Mitbesitzer und die Personen, denen die entsprechenden Berechtigungen erteilt wurde, haben in der **_Bearbeitungsansicht_** des Berichts Zugriff auf alle Untersuchungs-, Entwurfs-, Erstellungs- und Freigabefunktionen. Die Personen, für die der Bericht freigegeben wird, können den Bericht in der **_Leseansicht_** untersuchen und mit ihm interagieren.   

Wenn Sie einen Arbeitsbereich öffnen, werden die zugeordneten Berichte auf der Registerkarte **Berichte** aufgeführt. Jeder aufgeführte Bericht stellt mindestens eine Seite mit Visualisierungen dar, die auf nur einem der zugrunde liegenden Datasets basieren. Wählen Sie einen Bericht aus, um ihn zu öffnen.

Wenn Sie eine App öffnen, sehen Sie ein Dashboard.  Wählen Sie eine Dashboardkachel (siehe weiter unten) aus, die aus einem Bericht angeheftet wurde, um auf den zugrunde liegenden Bericht zuzugreifen. Beachten Sie, dass nicht alle Kacheln aus Berichten angeheftet werden, möglicherweise müssen Sie also einige Kacheln durchprobieren, bis Sie den gesuchten Bericht finden.

Der Bericht wird standardmäßig in der Leseansicht geöffnet.  Wählen Sie einfach **Bericht bearbeiten** aus, um den Bericht in der Bearbeitungsansicht zu öffnen (falls Sie über die erforderlichen Berechtigungen verfügen).

Im folgenden Beispiel ist die App „Vertrieb und Marketing“ ausgewählt, und es wurde auf die Registerkarte **Berichte** geklickt.

![Ausgewählte Berichte](media/service-basic-concepts/power-bi-reports.png)

**EIN** Bericht...

* ist in einem einzelnen Arbeitsbereich enthalten
* kann mehreren Dashboards in diesem Arbeitsbereich zugeordnet werden (die von diesem Bericht angehefteten Kacheln können auf mehreren Dashboards angezeigt werden).
* kann mithilfe der Daten aus einem Dataset erstellt werden. (Eine geringfügige Ausnahme besteht darin, dass Power BI Desktop mehrere Datasets zu einem einzelnen Bericht zusammenfassen kann, der in Power BI importiert werden kann.)

  ![Diagramm der Berichte](media/service-basic-concepts/drawing3new.png)

### <a name="dig-deeper"></a>Weiterführende Themen
* [Berichte im Power BI-Dienst und in Power BI Desktop](service-reports.md)
* [Berichte in den mobilen Power BI-Apps](mobile-reports-in-the-mobile-apps.md)

## <a name="dashboards"></a>Dashboards
Ein *Dashboard* ist ein von Ihnen **im Power BI-Dienst** oder von einem Kollegen **im Power BI-Dienst** erstelltes Objekt, das für Sie freigegeben wurde. Es handelt sich um einen einzelnen Zeichenbereich, der keine, eine oder mehrere Kacheln und Widgets enthält. Jede aus einem Bericht oder aus [Q&A](power-bi-q-and-a.md) angeheftete Kachel zeigt eine einzelne [Visualisierung](power-bi-report-visualizations.md) an, die aus einem Dataset erstellt wurde und an das Dashboard angeheftet ist. Gesamte Berichtsseiten können ebenfalls als einzelne Kachel an ein Dashboard angeheftet werden. Es gibt viele Möglichkeiten, dem Dashboard Kacheln hinzuzufügen – zu viele, um sie in diesem Übersichtsthema zu behandeln. Weitere Informationen finden Sie unter [Dashboardkacheln in Power BI](service-dashboard-tiles.md).

Warum werden Dashboards erstellt?  Hier sind nur einige der Gründe:

* Sie können auf einen Blick alle Informationen erkennen, die zum Treffen von Entscheidungen erforderlich sind.
* Sie können die wichtigsten unternehmensbezogenen Informationen überwachen.
* Sie können sicherstellen, dass sich alle Kollegen auf derselben Seite befinden und dabei dieselben Informationen anzeigen und verwenden.
* Sie können die Integrität eines Geschäfts, Produkts, Unternehmensbereichs oder einer Marketingkampagne usw. überwachen.
* Sie können eine personalisierte Ansicht eines umfangreicheren Dashboards erstellen, das alle für Sie erforderlichen Metriken enthält.

Wenn Sie einen Arbeitsbereich öffnen, werden die zugeordneten Dashboards auf der Registerkarte **Dashboards** aufgeführt. Wählen Sie ein Dashboard aus, um es zu öffnen. Wenn Sie eine App öffnen, sehen Sie ein Dashboard.  Jedes Dashboard stellt eine angepasste Ansicht einer Teilmenge der zugrunde liegenden Datasets dar.  Wenn Sie der Besitzer des Dashboards sind, haben Sie auch Bearbeitungszugriff auf das oder die zugrunde liegenden Datasets und Berichte.  Wenn das Dashboard für Sie freigegeben wurde, können Sie mit dem Dashboard und allen zugrunde liegenden Berichten interagieren, Sie können jedoch keine Änderungen speichern.

Es gibt viele verschiedene Möglichkeiten, wie Sie oder ein Kollege [ein Dashboard freigeben](service-share-dashboards.md) können. Power BI Pro ist für das Freigeben eines Dashboards und möglicherweise auch zum Anzeigen eines freigegebenen Dashboards erforderlich.


> [!NOTE]
> Kacheln und das Anheften werden unter der Überschrift „Dashboard mit Kacheln“ weiter unten ausführlicher beschrieben.
>

**EIN** Dashboard...

* ist einem einzelnen Arbeitsbereich zugeordnet.
* kann Visualisierungen von verschiedenen Datasets anzeigen.
* kann Visualisierungen von verschiedenen Berichten anzeigen.
* kann Visualisierungen anzeigen, die aus anderen Tools (z.B. Excel) angeheftet wurden.

  ![Ausgewähltes Dashboard](media/service-basic-concepts/drawing1.png)

### <a name="dig-deeper"></a>Weiterführende Themen
* [Erstellen eines neuen leeren Dashboards und Abrufen von Daten](service-dashboard-create.md)
* [Duplizieren eines Dashboards](service-dashboard-copy.md)
* [Erstellen einer Telefonansicht eines Dashboards](service-create-dashboard-mobile-phone-view.md)


## <a name="workbooks"></a>Arbeitsmappen
Arbeitsmappen sind eine besondere Art von Dataset. Wenn Sie den Abschnitt **Datasets** weiter oben gelesen haben, wissen Sie bereits das Wichtigste über Arbeitsmappen. Vielleicht fragen Sie sich jedoch, warum Excel-Arbeitsmappen in Power BI manchmal ein **Dataset** und manchmal eine **Arbeitsmappe** sind.

Wenn Sie **Daten abrufen** für Excel-Dateien verwenden, können Sie zwischen den Optionen *Importieren* und *Verknüpfen* für die Datei wählen. Wenn Sie „Verknüpfen“ wählen, wird die Arbeitsmappe in Power BI genauso angezeigt wie in Excel Online. Allerdings haben Sie im Gegensatz zu Excel Online einige hervorragende Funktionen zur Hand, mit denen Sie Elemente aus Arbeitsblättern direkt an Ihre Dashboards anheften können.

Sie können Ihre Arbeitsmappe in Power BI nicht bearbeiten. Wenn Sie aber Änderungen vornehmen müssen, können Sie auf „Bearbeiten“ klicken und die Arbeitsmappe in Excel online oder lokal bearbeiten. Alle vorgenommenen Änderungen werden in der Arbeitsmappe in OneDrive gespeichert.

### <a name="dig-deeper"></a>Weiterführende Themen
* [Abrufen von Daten aus Excel-Arbeitsmappendateien](service-excel-workbook-files.md)
* [Veröffentlichen in Power BI aus Excel](service-publish-from-excel.md)


## <a name="my-workspace"></a>Mein Arbeitsbereich
Bis hierher wurden Arbeitsbereiche und die Grundkomponenten erläutert. Sehen wir uns jetzt die Power BI-Benutzeroberfläche an sowie die einzelnen Komponenten, aus denen die Startseite für den Power BI-Dienst besteht.

![Der Power BI-Dienst in einem Browser](media/service-basic-concepts/completenewest.png)

### <a name="1-navigation-pane-left-navpane"></a>1. **Navigationsbereich** (linker Navigationsbereich)
Verwenden Sie den Navigationsbereich, um zwischen den Arbeitsbereichen und den Grundkomponenten von Power BI zu wechseln: Dashboards, Berichte, Arbeitsmappen und Datasets.  

  ![Navigationsbereich](media/service-basic-concepts/power-bi-navigation.png)

* Wählen Sie **Daten abrufen** aus, um [Datasets, Berichte und Dashboards zu Power BI hinzuzufügen](service-get-data.md).
* Erweitern und reduzieren Sie die Navigationsleiste mit diesem Symbol: ![Symbol für den Navigationsbereich](media/service-basic-concepts/expand-icon.png).
* Öffnen oder verwalten Sie Ihre wichtigsten Inhalte, indem Sie **Favoriten** auswählen.
* Zum Anzeigen und Öffnen der zuletzt abgerufenen Inhalte wählen Sie **Zuletzt verwendet** aus.
* Zum Anzeigen, Öffnen oder Löschen von Apps wählen Sie **Apps** aus.
* Hat ein Kollege Inhalte für Sie freigegeben? Wählen Sie **Für mich freigegeben** aus, um nach den gewünschten Inhalten zu suchen und diese zu sortieren.
* Klicken Sie auf **Arbeitsbereiche**, um Ihre Arbeitsbereiche anzuzeigen und zu öffnen.

Einfaches Klicken

* auf ein Symbol oder eine Überschrift öffnet die Inhaltsansicht.
* auf einen Rechtspfeil (>) öffnet ein Flyoutmenü für Arbeitsbereiche, Favoriten und zuletzt verwendete Elemente.
* ein Doppelpfeilsymbol () zeigt die scrollfähige Liste der Dashboards, Berichte, Arbeitsmappen und Datasets für **My Workspace** an.
* auf ein Dataset, um es zu untersuchen

### <a name="2-canvas"></a>2. **Zeichenbereich**
Da wir ein Dashboard geöffnet haben, werden im Zeichenbereich Visualisierungskacheln angezeigt. Wenn z.B. der Berichts-Editor geöffnet wäre, würde im Zeichnungsbereich eine Berichtsseite angezeigt werden.

Dashboards bestehen aus [Kacheln](service-dashboard-tiles.md).  Kacheln werden in der Bearbeitungsansicht, Q&A und anderen Dashboards für Berichte erstellt und können aus Excel, SSRS usw. angeheftet werden. Ein besonderer Kacheltyp namens [Widget](service-dashboard-add-widget.md) wird dem Dashboard direkt hinzugefügt. Die auf einem Dashboard angezeigten Kacheln wurden vom Ersteller/Besitzer eines Berichts eigens dort abgelegt.  Das Hinzufügen einer Kachel zu einem Dashboard wird als *anheften* bezeichnet.

![Power BI-Dashboardzeichenbereich](media/service-basic-concepts/canvas.png)

Weitere Informationen finden Sie unter **Dashboards** (oben).

### <a name="3-qa-question-box"></a>3. **Fragenfeld für Fragen und Antworten (F&A)**
Eine Möglichkeit zum Untersuchen der Daten besteht darin, eine Frage zu stellen, um über den Bereich für Fragen und Antworten von Power BI eine Antwort in Form einer Visualisierung zu erhalten. Mit Q&A können Inhalte einem Dashboard oder einem Bericht hinzugefügt werden.

Der Bereich für Fragen und Antworten sucht im Dataset bzw. in Datasets, die mit dem Dashboard verbunden sind, nach Antworten.  Bei einem verbundenen Dataset handelt es sich um ein Dataset, für das mindestens eine Kachel an dieses Dashboard angeheftet ist.

![Fragenfeld für Fragen und Antworten (F&A)](media/service-basic-concepts/power-bi-qna.png)

Sobald Sie mit der Eingabe einer Frage beginnen, gelangen Sie zur Seite für Fragen und Antworten (F&A). Während der Eingabe unterstützt Sie der Bereich für Fragen und Antworten mithilfe von Umformulierungen, AutoAusfüllen, Vorschlägen usw. dabei, die richtige Frage zu stellen und die beste Antwort zu finden. Wenn Sie eine Visualisierung (Antwort) gefunden haben, die Ihnen gefällt, fügen Sie diese einfach zum Dashboard hinzu. Weitere Informationen finden Sie unter [Fragen und Antworten in Power BI](power-bi-q-and-a.md).

### <a name="4-icon-buttons"></a>4. **Symbolschaltflächen**
Die Symbole in der rechten oberen Ecke sind Ihre Ressourcen für Einstellungen, Benachrichtigungen, Downloads, zum Öffnen der Hilfe und zum Senden von Feedback an das Power BI-Team. Wählen Sie den doppelten Pfeil aus, um das Dashboard im **Vollbildmodus** zu öffnen.  

![Symbolschaltflächen](media/service-basic-concepts/power-bi-icons.png)

### <a name="5-dashboard-title-navigation-path-aka-breadcrumbs"></a>5. **Dashboardtitel** (Navigationspfad oder Breadcrumbs)
Damit Sie leichter erkennen können, welcher Arbeitsbereich und welches Dashboard gerade aktiv ist, wird in Power BI automatisch ein Navigationspfad erstellt.  In diesem Beispiel sehen Sie den Arbeitsbereich („Mein Arbeitsbereich“) und den Dashboardtitel („Retail Analysis Sample“).  Wenn ein Bericht geöffnet wäre, wurde der Name des Berichts am Ende des Navigationspfads angehängt werden.  Jeder Abschnitt des Pfads ist ein aktiver Link.  

Beachten Sie das Symbol „C“ nach dem Dashboardtitel. Dieses Dashboard besitzt das [Datenklassifizierungstag](service-data-classification.md) für „Vertraulich“. Das Tag gibt die Vertraulichkeits- und Sicherheitsstufe der Daten an. Wenn Ihr Administrator die Datenklassifizierung aktiviert hat, wird für jedes Dashboard ein Standardtag festgelegt. Dashboardbesitzer sollten das Tag entsprechend der richtigen Sicherheitsstufe des Dashboards ändern.

![Symbol für die Datenklassifizierung](media/service-basic-concepts/power-bi-title.png)

### <a name="6-office-365-app-launcher"></a>6. **Office 365-App-Startfeld**
Über das App-Startfeld können Sie mit einem Mausklick einfach auf alle Ihre Office 365-Apps zugreifen. Hier können Sie schnell Ihre E-Mails, Dokumente, Kalender und vieles mehr starten.

![Office App-Startfeld](media/service-basic-concepts/power-bi-waffle.png)

### <a name="7-power-bi-home"></a>7. **Power BI-Startseite**
Wenn Sie auf **Power BI** klicken, gelangen Sie zur Power BI-Startseite zurück.

   ![„Power BI“ im Dienst](media/service-basic-concepts/version-new.png)

### <a name="8-labeled-icon-buttons"></a>8. **Beschriftete Symbolschaltflächen**
In diesem Bereich des Bildschirms finden Sie zusätzliche Optionen für die Interaktion mit Inhalten (in diesem Fall dem Dashboard).  Neben den beschrifteten Symbolen können Sie die Auslassungspunkte auswählen, um Optionen zum Duplizieren, Drucken und Aktualisieren des Dashboards und weitere Optionen anzuzeigen.

   ![Beschriftete Symbolschaltflächen](media/service-basic-concepts/power-bi-labeled-icons.png)

## <a name="next-steps"></a>Nächste Schritte
[Was ist Power BI?](power-bi-overview.md)  
[Die neue Navigation im Power BI-Dienst](service-the-new-power-bi-experience.md)
[Power BI-Videos](videos.md)  
[Berichts-Editor – Verschaffen Sie sich einen Überblick](service-the-report-editor-take-a-tour.md)

Weitere Fragen? [Stellen Sie Ihre Frage in der Power BI-Community.](http://community.powerbi.com/)
