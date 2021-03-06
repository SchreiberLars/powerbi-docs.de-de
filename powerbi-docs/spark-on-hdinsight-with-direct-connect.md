---
title: Spark on HDInsight mit DirectQuery
description: Spark on HDInsight mit DirectQuery
author: markingmyname
ms.author: maghan
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 10/01/2018
LocalizationGroup: Data from databases
ms.openlocfilehash: 92b8d0e0ecfa9bae36e552e30cf8f1a7fcecff4b
ms.sourcegitcommit: 60fb46b61ac73806987847d9c606993c0e14fb30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2018
ms.locfileid: "50100747"
---
# <a name="spark-on-hdinsight-with-directquery"></a>Spark on HDInsight mit DirectQuery

Spark on Azure HDInsight mit DirectQuery ermöglicht es Ihnen, dynamische Berichte auf Basis von Daten und Metriken zu erstellen, die bereits im Spark-Cluster verfügbar sind. Mit DirectQuery werden Abfragen zurück zum Azure HDInsight Spark-Cluster gesendet, während Sie die Daten in der Berichtsansicht untersuchen. Diese Variante wird für Benutzer empfohlen, die mit den Entitäten vertraut sind, mit denen die Verbindung hergestellt wird.

> [!WARNING]
> Die automatische Aktualisierung von Kacheln wurde für auf Grundlage von Spark-Datasets erstellte Dashboardkacheln deaktiviert. Mit der Option **Dashboardkacheln aktualisieren** können Sie die Kacheln manuell aktualisieren. Berichte sind hiervon nicht betroffen und sollten auf dem neuesten Stand bleiben. 

Sie können die folgenden Schritte ausführen, um mithilfe von DirectQuery im Power BI-Dienst eine Verbindung mit der Spark on Azure HDInsight-Datenquelle herzustellen.

> [!Important]
> Die Konnektivität mit Spark wurde verbessert.  Verwenden Sie Power BI Desktop für optimale Ergebnisse beim Herstellen einer Verbindung mit Ihrer Spark-Datenquelle.  Sobald Sie Ihr Modell und Ihren Bericht erstellt haben, können Sie diese im Power BI-Dienst veröffentlichen.  Der direkte Connector für Spark im Power BI-Dienst ist mittlerweile veraltet.

1. Wählen Sie unten im linken Navigationsbereich **Daten abrufen** aus.

     ![](media/spark-on-hdinsight-with-direct-connect/spark-getdata.png)
2. Wählen Sie **Datenbanken und mehr** aus.

     ![](media/spark-on-hdinsight-with-direct-connect/spark-getdata-databases.png)
3. Wählen Sie den Connector **Spark auf HDInsight** und anschließend **Verbinden**aus.

     ![](media/spark-on-hdinsight-with-direct-connect/spark-getdata-databases-connect.png)
4. Geben Sie den Namen des **Servers** ein, zu dem eine Verbindung hergestellt werden soll, sowie Ihren **Benutzernamen** und das **Kennwort**. Der Server erscheint immer in der Form „\<Clustername\>.azurehdinsight.net“. Weitere Informationen zum Suchen dieser Werte finden Sie unten.

     ![](media/spark-on-hdinsight-with-direct-connect/spark-server-name.png)

     ![](media/spark-on-hdinsight-with-direct-connect/spark-username.png)
5. Nachdem die Verbindung hergestellt ist, sehen Sie ein neues Dataset mit dem Namen „SparkDataset“. Sie können auf das Dataset auch über die erstellte Platzhalterkachel zugreifen.

     ![](media/spark-on-hdinsight-with-direct-connect/spark-dataset.png)
6. Beim Drilldown in das Dataset können Sie alle Tabellen und Spalten in der Datenbank durchsuchen. Wenn Sie eine Spalte auswählen, wird eine Abfrage zurück an die Quelle gesendet, wodurch Ihre Visualisierung dynamisch erstellt wird. Diese Visualisierungen können in einem neuen Bericht gespeichert und wieder auf Ihrem Dashboard angeheftet werden.

## <a name="finding-your-spark-on-hdinsight-parameters"></a>Suchen von Spark auf HDInsight-Parametern

Der Server besitzt immer die Form „\<Clustername\>.azurehdinsight.net“ und steht im Azure-Portal.

![](media/spark-on-hdinsight-with-direct-connect/spark-server-name-parameter.png)

Benutzername und Kennwort finden Sie ebenfalls im Azure-Portal.

## <a name="limitations"></a>Einschränkungen

Diese Einschränkungen und Hinweise können sich ändern, da wir die Benutzeroberfläche fortlaufend optimieren. Zusätzliche Dokumentation finden Sie unter [Verwenden von BI-Tools mit Apache Spark für Azure HDInsight](/azure/hdinsight/spark/apache-spark-use-bi-tools/).

* Der Power BI-Dienst unterstützt nur eine Konfiguration, die Spark 2.0 und HDInsights 3.5 umfasst.
* Durch jede Aktion, wie z. B. das Auswählen einer Spalte oder das Hinzufügen eines Filters, wird eine Abfrage an die Datenbank gesendet – bevor Sie sehr große Felder auswählen, sollten Sie einen geeigneten Visualisierungstyp wählen.
* Q&A steht für DirectQuery-Datasets nicht zur Verfügung.
* Schemaänderungen werden nicht automatisch übernommen.
* Power BI unterstützt 16.000 Spalten **für alle Tabellen insgesamt** in einem Dataset. Power BI enthält außerdem eine interne Zeilennummernspalte pro Tabelle. Dies bedeutet, dass 15.900 Spalten verfügbar sind, wenn das Dataset 100 Tabellen enthält. Abhängig vom Umfang der Daten aus der Spark-Datenquelle, mit denen Sie arbeiten, kann diese Einschränkung zur Wirkung kommen.

## <a name="troubleshooting"></a>Problembehandlung

Wenn Probleme beim Ausführen von Abfragen gegen Ihr Cluster auftreten, stellen Sie sicher, dass die Anwendung weiterhin ausgeführt wird, und starten Sie sie bei Bedarf neu.

Sie können im Azure-Portal unter **Konfiguration** > **Cluster skalieren** auch zusätzliche Ressourcen zuordnen:

![](media/spark-on-hdinsight-with-direct-connect/spark-scale.png)

## <a name="next-steps"></a>Nächste Schritte

[Erste Schritte: Erstellen eines Apache Spark-Clusters für HDInsight (Linux) und Ausführen von interaktiven Abfragen per Spark-SQL](/azure/hdinsight/spark/apache-spark-jupyter-spark-sql/)  
[Was ist Power BI?](power-bi-overview.md)  
[Abrufen von Daten für Power BI](service-get-data.md)
[Verwenden von Kerberos auf dem lokalen Gateway für SSO](service-gateway-sso-kerberos.md)

Weitere Fragen? [Wenden Sie sich an die Power BI-Community](http://community.powerbi.com/)