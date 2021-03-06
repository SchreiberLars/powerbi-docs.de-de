---
title: Verwenden von Sicherheit auf Zeilenebene für eingebettete Inhalte aus Power BI
description: Erfahren Sie mehr zu den Schritten, die Sie durchführen müssen, um Inhalte von Power BI in Ihre Anwendung einzubetten.
author: markingmyname
ms.author: maghan
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-developer
ms.topic: conceptual
ms.date: 09/18/2018
ms.openlocfilehash: 60061d781542f8b5a3ef67a75e61d902459d4963
ms.sourcegitcommit: ded8b85276e7eda166d6e67f72d1fe3d5e234745
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/21/2018
ms.locfileid: "46506774"
---
# <a name="use-row-level-security-with-power-bi-embedded-content"></a>Verwenden von Sicherheit auf Zeilenebene für eingebettete Inhalte aus Power BI

Mit der Sicherheit auf Zeilenebene (Row Level Security,RLS) kann der Benutzerzugriff auf Daten in Dashboards, Kacheln, Berichten und Datasets beschränkt werden. Verschiedene Benutzer können mit den gleichen Artefakten arbeiten und dabei unterschiedliche Daten sehen. Beim Einbetten wird RLS unterstützt.

Wenn Sie Berichte für Benutzer einbetten, die nicht Power BI verwenden (d.h. die App ist Besitzer der Daten), was normalerweise bei ISVs der Fall ist, ist dieser Artikel für Sie relevant. Sie müssen das Einbettungstoken konfigurieren, um den Benutzer und die Rolle anzugeben. Die Vorgehensweise wird im Folgenden beschrieben.

Wenn Sie Berichte für Power BI-Benutzer in der Organisation einbetten (der Benutzer ist der Besitzer der Daten), wird RLS auf die gleiche Weise wie direkt im Power BI-Dienst angewendet. Sie müssen in der Anwendung nichts unternehmen. Weitere Informationen finden Sie unter [Sicherheit auf Zeilenebene (row-level Security; RLS) mit Power BI](../service-admin-rls.md).

![Die für die Sicherheit auf Zeilenebene relevanten Elemente.](media/embedded-row-level-security/powerbi-embedded-rls-components.png)

Um RLS nutzen zu können, müssen Sie drei wichtige Konzepte verstehen: Benutzer, Rollen und Regeln. Sehen wir uns diese im Einzelnen genauer an:

**Benutzer**: Endbenutzer, die das Artefakt (Dashboard, Kachel, Bericht oder Dataset) anzeigen. In Power BI Embedded werden Benutzer durch die username-Eigenschaft in einem Einbettungstoken identifiziert.

**Rollen**: Benutzer gehören Rollen an. Eine Rolle ist ein Container für Regeln. Sie kann z.B. mit *Vertriebsleiter* oder *Vertriebsmitarbeiter* benannt werden. Rollen werden in Power BI Desktop erstellt. Weitere Informationen finden Sie unter [Sicherheit auf Zeilenebene (row-level Security; RLS) mit Power BI Desktop](../desktop-rls.md).

**Regeln**: Für Rollen gelten Regeln, und diese Regeln sind die Filter, die auf die Daten anzuwenden sind. Dabei kann es sich um eine einfache Regel, z.B. „Land = USA“, oder eine dynamischere Regel handeln.
Im Rest dieses Artikels wird ein Beispiel für das Erstellen von RLS beschrieben, das dann in einer eingebetteten Anwendung verwendet wird. In unserem Beispiel wird die PBIX-Datei [Retail Analysis Sample](http://go.microsoft.com/fwlink/?LinkID=780547) (Analysebeispiel für den Einzelhandel) verwendet.

![Beispiel für einen Bericht](media/embedded-row-level-security/powerbi-embedded-report-example.png)

## <a name="adding-roles-with-power-bi-desktop"></a>Hinzufügen von Rollen mit Power BI Desktop

Im Analysebeispiel für den Einzelhandel werden die Umsätze für alle Geschäfte in einer Einzelhandelskette angezeigt. Ohne RLS werden für jeden Gebietsleiter, der sich anmeldet und den Bericht öffnet, dieselben Daten angezeigt. Die Geschäftsleitung hat bestimmt, dass für jeden Gebietsleiter nur die Umsätze für die von ihnen geleiteten Geschäfte angezeigt werden sollen. Dies können wir mit RLS erreichen.

RLS wird in Power BI Desktop konfiguriert. Wenn das Dataset und der Bericht geöffnet sind, können wir zur Diagrammansicht wechseln, um das Schema anzuzeigen:

![Diagrammansicht in Power BI Desktop](media/embedded-row-level-security/powerbi-embedded-schema.png)

Dieses Schema weist die folgenden Merkmale auf:

* Sämtliche Measures, z.B. **Total Sales** (Gesamtumsatz), werden in der Faktentabelle **Sales** (Umsätze) gespeichert.
* Es gibt vier zusätzliche verknüpfte Dimensionstabellen: **Item** (Artikel), **Time** (Zeit), **Store** (Geschäft) und **District** (Bezirk).
* Die Pfeile auf den Beziehungslinien geben die Richtung der Filter zwischen den Tabellen an. Wenn z.B. im aktuellen Schema der Filter **Time[Date]** (Zeit[Datum]) eingesetzt wird, filtert dieser nur Werte in der Tabelle **Sales** (Umsätze). Von diesem Filter sind keine weiteren Tabellen betroffen, da alle Pfeile auf den Beziehungslinien ausschließlich auf die Tabelle „Sales“ (Umsätze) zeigen.
* Die Tabelle **District** (Bezirk) gibt an, wer der Gebietsleiter für den jeweiligen Bezirk ist:
  
    ![Zeilen in der Tabelle „Disctrict“ (Bezirk)](media/embedded-row-level-security/powerbi-embedded-district-table.png)

Wir wenden basierend auf diesem Schema einen Filter auf die Spalte **District Manager** (Gebietsleiter) in der Tabelle **District** (Bezirk) an. Wenn dieser Filter mit dem Benutzer übereinstimmt, der den Bericht anzeigt, wird der Filter auch auf die Tabellen **Store** (Geschäft) und **Sales** (Umsätze) angewendet, damit nur Daten für diesen Gebietsleiter angezeigt werden.

Dazu gehen Sie wie folgt vor:

1. Wählen Sie auf der Registerkarte **Modellierung** die Option **Rollen verwalten** aus.

    ![Registerkarte „Modellierung“ in Power BI Desktop](media/embedded-row-level-security/powerbi-embedded-manage-roles.png)
2. Erstellen Sie eine neue Rolle mit dem Namen **Manager**.

    ![Neue Rolle erstellen](media/embedded-row-level-security/powerbi-embedded-new-role.png)
3. Geben Sie in der Tabelle **District** (Bezirk) den folgenden DAX-Ausdruck ein: **[District Manager] = USERNAME()**.

    ![DAX-Anweisung für RLS-Regel](media/embedded-row-level-security/powerbi-embedded-new-role-dax.png)
4. Um sicherzustellen, dass die Regeln angewendet werden, wählen Sie auf der Registerkarte **Modellierung** die Option **Als Rollen anzeigen** aus, und wählen Sie dann die Ro+lle **Manager**, die Sie gerade erstellt haben, und **Anderer Benutzer** aus. Geben Sie als Benutzer **AndrewMa** ein.

    ![Dialogfeld „Als Rollen anzeigen“](media/embedded-row-level-security/powerbi-embedded-new-role-view.png)

    In den Berichten werden jetzt Daten für den angemeldeten Benutzer **AndrewMa** angezeigt.

Wenn der Filter so wie hier angewendet wird, werden alle Datensätze in den Tabellen **District** (Bezirk), **Store** (Geschäft) und **Sales** (Umsätze) gefiltert. Aufgrund der Filterrichtung in den Beziehungen zwischen den Tabellen **Sales** (Umsätze) und **Time** (Zeit), **Sales** (Umsätze) und **Item** (Artikel) sowie **Item** (Artikel) und **Time** (Zeit) erfolgt keine Filterung in diesen Richtungen. Um weitere Informationen über die bidirektionale Kreuzfilterung zu erhalten, laden Sie das Whitepaper [Bidirectional cross-filtering in SQL Server Analysis Services 2016 and Power BI Desktop](http://download.microsoft.com/download/2/7/8/2782DF95-3E0D-40CD-BFC8-749A2882E109/Bidirectional%20cross-filtering%20in%20Analysis%20Services%202016%20and%20Power%20BI.docx) (Bidirektionale Kreuzfilterung in SQL Server Analysis Services 2016 und Power BI Desktop, in englischer Sprache) herunter.

## <a name="applying-user-and-role-to-an-embed-token"></a>Anwenden eines Benutzers und einer Rolle auf ein Einbettungstoken

Nachdem Sie jetzt die Power BI Desktop-Rollen konfiguriert haben, müssen in Ihrer Anwendung einige Schritte ausgeführt werden, um die Rollen zu nutzen.

Benutzer werden durch die Anwendung authentifiziert und autorisiert, und mithilfe von Einbettungstoken wird einem Benutzer Zugriff auf einen bestimmten Power BI Embedded-Bericht gewährt. Power BI Embedded verfügt über keine Informationen über die Identität des Benutzers. Damit RLS erfolgreich angewendet wird, müssen Sie im Einbettungstoken zusätzlichen Kontext in Form von Identitäten übergeben. Dies erfolgt durch die [Embed Token](https://docs.microsoft.com/rest/api/power-bi/embedtoken)-API.

Die API akzeptiert eine Liste von Identitäten mit Angabe der entsprechenden Datasets. Für die erfolgreiche Anwendung von RLS müssen Sie Folgendes als Teil der Identität übergeben.

* **username** (obligatorisch): Dies ist eine Zeichenfolge, die beim Anwenden von RLS-Regeln zum Identifizieren des Benutzers verwendet werden kann. Es kann nur ein einziger Benutzer aufgelistet werden. Ihr Benutzername kann mit *ASCII*-Zeichen erstellt werden.
* **roles** (obligatorisch): Eine Zeichenfolge, in der die Rollen angegeben werden, die beim Anwenden von Regeln für die Sicherheit auf Zeilenebene ausgewählt werden sollen. Wenn mehrere Rollen übergeben werden, müssen sie als Zeichenfolgenarray übergeben werden.
* **Dataset** (obligatorisch): Das entsprechende Dataset für das Artefakt, das Sie einbetten.

Sie können das Einbettungstoken mit der **GenerateTokenInGroup**-Methode für **PowerBIClient.Reports** erstellen.

Sie können z.B. das Beispiel [PowerBIEmbedded_AppOwnsData](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/App%20Owns%20Data) ändern. Zeile 76 und 77 in *Home\HomeController.cs* können aktualisiert werden von:

```csharp
// Generate Embed Token.
var generateTokenRequestParameters = new GenerateTokenRequest(accessLevel: "view");

var tokenResponse = await client.Reports.GenerateTokenInGroupAsync(GroupId, report.Id, generateTokenRequestParameters);
```

auf

```csharp
var generateTokenRequestParameters = new GenerateTokenRequest("View", null, identities: new List<EffectiveIdentity> { new EffectiveIdentity(username: "username", roles: new List<string> { "roleA", "roleB" }, datasets: new List<string> { "datasetId" }) });

var tokenResponse = await client.Reports.GenerateTokenInGroupAsync("groupId", "reportId", generateTokenRequestParameters);
```

Wenn Sie die REST-API aufrufen, akzeptiert die aktualisierte API ein zusätzliches JSON-Array mit dem Namen **identities**, das einen Benutzernamen, eine Liste von Zeichenfolgen mit Rollen und eine Liste von Zeichenfolgen mit Datasets enthält, z.B.:

```json
{
    "accessLevel": "View",
    "identities": [
        {
            "username": "EffectiveIdentity",
            "roles": [ "Role1", "Role2" ],
            "datasets": [ "fe0a1aeb-f6a4-4b27-a2d3-b5df3bb28bdc" ]
        }
    ]
}
```

Da jetzt alle Komponenten implementiert wurden, werden für einen Benutzer, der sich zum Anzeigen dieses Artefakts bei der Anwendung anmeldet, nur die Daten angezeigt, die für ihn gemäß der von uns definierten Sicherheit auf Zeilenebene angezeigt werden dürfen.

## <a name="working-with-analysis-services-live-connections"></a>Arbeiten mit den Liveverbindungen von Analysis Services

Bei Liveverbindungen von Analysis Services kann für lokale Server Sicherheit auf Zeilenebene verwendet werden. Wenn Sie diesen Typ von Verbindung verwenden, sollten Sie einige spezielle Konzepte verstehen.

Die effektive Identität, die für die username-Eigenschaft bereitgestellt wird, muss ein Windows-Benutzer mit Berechtigungen für den Analysis Services-Server sein.

**Konfiguration des lokalen Datengateways**

Beim Arbeiten mit Liveverbindungen von Analysis Services wird ein [lokales Datengateway](../service-gateway-onprem.md) verwendet. Beim Generieren eines Einbettungstokens mit einer angegebenen Identität muss das Hauptkonto als Administrator des Gateways aufgeführt werden. Wenn das Hauptkonto nicht aufgeführt ist, wird Sicherheit auf Zeilenebene nicht auf die Eigenschaft der Daten angewendet. Ein Benutzer des Gateways ohne Administratorrechte kann Rollen bereitstellen, er muss jedoch den eigenen Benutzernamen als effektive Identität angeben.

**Verwenden von Rollen**

Rollen können in einem Einbettungstoken mit der Identität angegeben werden. Wenn keine Rolle angegeben wurde, wird zum Auflösen der zugehörigen Rollen der angegebene Benutzername verwendet.

**Verwenden des CustomData-Features**

Das CustomData-Feature ermöglicht die Übergabe von Freitext (Zeichenfolge) mithilfe der Verbindungszeichenfolgen-Eigenschaft von CustomData. Dabei handelt es sich um einen Wert, der von AS (über die CUSTOMDATA()-Funktion) verwendet werden soll.
Sie können dies als alternative Möglichkeit zum Anpassen der Datennutzung verwenden.
Sie können das Feature innerhalb der DAX-Rollenabfrage verwenden. Außerdem können Sie es ohne eine Rolle in einer DAX-Measureabfrage verwenden.
Das CustomData-Feature ist Teil der Funktionalität zur Tokengenerierung für folgende Elemente: Dashboards, Berichte und Kacheln. Dashboards können über mehrere CustomData-Identitäten (eine pro Kachel/Modell) verfügen.

> [!NOTE]
> Das CustomData-Feature funktioniert nur für Modelle, die in Azure Analysis Services gespeichert sind und nur im Livemodus. Im Gegensatz zu Benutzern und Rollen kann das CustomData-Feature nicht innerhalb einer PBIX-Datei festgelegt werden. Wenn ein Token mit dem CustomData-Feature generiert wird, müssen Sie einen Benutzernamen besitzen.

**Erweiterungen des CustomData SDK**

Die CustomData-Zeichenfolgeneigenschaft wurde bei der Tokengenerierung zur effektiven Identität hinzugefügt.

        [JsonProperty(PropertyName = "customData")]
        public string CustomData { get; set; }

Die Identität kann mithilfe von benutzerdefinierten Daten erstellt werden, indem Sie folgenden Aufruf verwenden:

        public EffectiveIdentity(string username, IList<string> datasets, IList<string> roles = null, string customData = null);

**Verwendung des CustomData SDK**

Wenn Sie die REST-API aufrufen, können Sie in jeder Identität benutzerdefinierte Daten hinzufügen, z.B.:

```json
{
    "accessLevel": "View",
    "identities": [
        {
            "username": "EffectiveIdentity",
            "roles": [ "Role1", "Role2" ],
            "customData": "MyCustomData",
            "datasets": [ "fe0a1aeb-f6a4-4b27-a2d3-b5df3bb28bdc" ]
        }
    ]
}
```

## <a name="considerations-and-limitations"></a>Überlegungen und Einschränkungen

* Die Zuweisung von Benutzern zu Rollen im Power BI-Dienst wirkt sich bei Verwendung eines Einbettungstokens nicht auf RLS aus.
* Der Power BI-Dienst wendet die RLS-Einstellung nicht auf Administratoren oder Mitglieder mit Bearbeitungsberechtigungen an, wenn Sie eine Identität mit einem Einbettungstoken bereitstellen, jedoch auf die Daten.
* Liveverbindungen von Analysis Services werden für lokale Server unterstützt.
* Azure Analysis Services-Liveverbindungen unterstützen Filtern nach Rollen. Die dynamische Filterung kann mit „CustomData“ ausgeführt werden.
* Wenn das zugrunde liegende Dataset kein RLS erfordert, darf die GenerateToken-Anforderung **keine** effektive Identität enthalten.
* Wenn das zugrunde liegende Dataset ein Cloudmodell ist (Cachemodell oder DirectQuery), muss die effektive Identität mindestens eine Rolle enthalten. Andernfalls erfolgt keine Rollenzuweisung.
* Mit einer Identitätenliste werden mehrere Identitätstoken für die Dashboardeinbettung aktiviert. Bei allen anderen Artefakten enthält die Liste eine einzelne Identität.

Weitere Fragen? [Stellen Sie Ihre Frage in der Power BI-Community.](https://community.powerbi.com/)
