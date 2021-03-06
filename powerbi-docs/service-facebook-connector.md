---
title: 'Drittanbieterdienst: Facebook-Connector für Power BI Desktop'
description: 'Drittanbieterdienst: Facebook-Connector für Power BI Desktop'
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 11/28/2018
ms.author: davidi
LocalizationGroup: Connect to data
ms.openlocfilehash: 66f6fa32ecabecfbaa178b5744e71c80a6020ebd
ms.sourcegitcommit: 2ae660a7b70fce23eb58b159d049eca44a664f2c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/30/2018
ms.locfileid: "52669656"
---
# <a name="facebook-connector-for-power-bi-desktop"></a>Facebook-Connector für Power BI Desktop
Der Facebook-Connector in **Power BI Desktop** ist abhängig von der Graph-API von Facebook. Daher können Funktionen und Verfügbarkeit im Laufe der Zeit variieren.

Sie können sich ein [Lernprogramm über den Facebook-Connector für Power BI Desktop](desktop-tutorial-facebook-analytics.md) anschauen.

Facebook hat Version 1.0 seiner Graph-API am 30. April<sup></sup> 2015 eingestellt. Die Graph-API wird von Power BI im Hintergrund für den Facebook-Connector verwendet, damit Sie sich mit Ihren Daten verbinden und diese analysieren können.

Abfragen, die vor dem 30. April<sup></sup> 2015 erstellt wurden, funktionieren möglicherweise nicht mehr oder geben weniger Daten zurück. Nach dem <sup>30. April</sup> 2015 nutzt Power BI Version 2.8 in allen Aufrufen an die Facebook-API. Wenn Ihre Abfrage vor dem 30. April 2015 erstellt wurde und Sie sie seitdem nicht verwendet haben, müssen Sie die Authentifizierung wahrscheinlich erneut durchführen, um den neuen Satz an Berechtigungen zu genehmigen, den wir abfragen.

Obwohl wir versuchen, gemäß allen Änderungen Updates zu veröffentlichen, könnte die API so abgeändert werden, dass sich dies auf die Ergebnisse der generierten Abfragen auswirkt. In einigen Fällen könnten bestimmte Abfragen nicht mehr unterstützt werden. Aufgrund dieser Abhängigkeit können wir die Ergebnisse Ihrer Abfragen nicht garantieren, wenn Sie diesen Connector verwenden.

Weitere Informationen über die Änderung in der Facebook-API stehen Ihnen [hier](https://developers.facebook.com/docs/apps/changelog#v2_0) zur Verfügung.

