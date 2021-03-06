---
title: Verwenden einer alternativen E-Mail-Adresse
description: Verwenden einer alternativen E-Mail-Adresse
author: mgblythe
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 11/01/2018
ms.author: mblythe
LocalizationGroup: Troubleshooting
ms.openlocfilehash: 41b3a0b1032616045b854e4a4776ba82bffffe47
ms.sourcegitcommit: 0611860a896e636ceeb6e30ce85243bfd8e7b61d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/01/2018
ms.locfileid: "50909413"
---
# <a name="using-an-alternate-email-address"></a>Verwenden einer alternativen E-Mail-Adresse

Wenn Sie sich für Power BI registrieren, müssen Sie eine E-Mail-Adresse angeben. Power BI verwendet diese Adresse standardmäßig, um Ihnen Updates zu den Aktivitäten in diesem Dienst zu senden. Wenn Ihnen beispielsweise ein Benutzer eine Freigabeeinladung sendet, wird diese Adresse verwendet.

Es gibt jedoch Fälle, in denen diese E-Mails an eine andere als die bei der Registrierung verwendete Adresse gesendet werden sollen. Dieser Artikel erläutert, wie Sie in Office 365 und PowerShell eine alternative E-Mail-Adresse angeben. In diesem Artikel wird ebenfalls beschrieben, wie eine E-Mail-Adresse in Azure Active Directory (Azure AD) aufgelöst wird.

> [!NOTE]
> Die Angabe einer alternativen Adresse wirkt sich nicht auf die E-Mail-Adresse aus, die Power BI für Dienstupdates, Newsletter und andere Werbekommunikation verwendet.  Diese Informationen werden immer an die E-Mail-Adresse gesendet, die Sie beim Registrieren für Power BI angegeben haben.

## <a name="use-office-365"></a>Verwenden von Office 365

Um in Office 365 eine alternative Adresse anzugeben, führen Sie die folgenden Schritte aus.

1. Öffnen Sie Ihre [persönliche Office 365-Informationsseite](https://portal.office.com/account/#personalinfo). Wenn Sie dazu aufgefordert werden, melden Sie sich mit der E-Mail-Adresse und dem Kennwort an, die Sie für Power BI verwenden.

1. Wählen Sie im linken Menü **Persönliche Informationen** aus.

1. Klicken Sie im Abschnitt mit den **Kontaktdetails** auf **Bearbeiten**.

    Wenn Sie die Informationen nicht bearbeiten können, bedeutet dies, dass Ihre E-Mail-Adresse von Ihrem Office 365-Administrator verwaltet wird. Wenden Sie sich an Ihren Administrator, um Ihre E-Mail-Adresse zu aktualisieren.

    ![Kontaktdetails](media/service-admin-alternate-email-address-for-power-bi/contact-details.png)

1. Geben Sie im Feld **Alternative E-Mail-Adresse** die E-Mail-Adresse ein, an die Power BI-Updates gesendet werden sollen.

## <a name="use-powershell"></a>Verwenden von PowerShell

Um in PowerShell eine alternative Adresse anzugeben, verwenden Sie den Befehl [Set-AzureADUser](/powershell/module/azuread/set-azureaduser/).

```powershell
Set-AzureADUser -ObjectId john@contoso.com -OtherMails "otheremail@somedomain.com"
```

## <a name="email-address-resolution-in-azure-ad"></a>Auflösung der E-Mail-Adresse in Azure AD

Bei der Erfassung eines integrierten Azure AD-Tokens für Power BI können Sie drei verschiedene E-Mail-Typen verwenden:

* Die Haupt-E-Mail-Adresse, die dem Azure AD-Konto eines Benutzers zugeordnet ist

* Die UPN-E-Mail-Adresse (UserPrincipalName)

* Das Attribut für das Array *Andere E-Mail-Adresse*

Power BI wählt anhand der folgenden Kriterien (in der angegebenen Reihenfolge) aus, welche E-Mail-Adresse verwendet werden soll:

1. Wenn das E-Mail-Attribut im Azure AD-Benutzerobjekt vorhanden ist, verwendet Power BI dieses E-Mail-Attribut für die E-Mail-Adresse.

1. Wenn es sich bei der UPN-E-Mail-Adresse *nicht* um eine E-Mail-Adresse der Domäne **\*.onmicrosoft.com** handelt (die Informationen hinter dem Symbol „@“), verwendet Power BI dieses E-Mail-Attribut für die E-Mail-Adresse.

1. Wenn das Attribut für das Array *Andere E-Mail-Adresse* im Azure AD-Benutzerobjekt vorhanden ist, wird die erste E-Mail-Adresse in dieser Liste verwendet (dieses Attribut kann eine Liste mit E-Mail-Adressen enthalten).

1. Wenn keine der oben genannten Bedingungen erfüllt ist, wird die UPN-Adresse verwendet.

Weitere Fragen? [Wenden Sie sich an die Power BI-Community](http://community.powerbi.com/)

