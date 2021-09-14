---
title: Comment traiter les notifications de sélecteur de date et d’heure
description: Cette section montre comment traiter les notifications de sélecteur de date et d’heure.
ms.assetid: DBF624F0-89E0-435B-BE96-60B7A4CEDA61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa1214ebd671b4ae222990bde4b44586e6d7b11
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117602"
---
# <a name="how-to-process-date-and-time-picker-notifications"></a>Comment traiter les notifications de sélecteur de date et d’heure

Cette section montre comment traiter les notifications de sélecteur de date et d’heure.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions


Un contrôle de sélecteur de date et heure (PAO) envoie des messages de notification à la fenêtre parente lorsque des événements, généralement déclenchés par une entrée de l’utilisateur, se produisent dans le contrôle. Votre application doit inclure du code pour déterminer le type de message de notification et répondre de manière appropriée.

Si vous envisagez d’utiliser des champs de rappel avec les contrôles de PAO dans votre application, vous devez être prêt à gérer les codes de notification [DTN \_ FORMATQUERY](dtn-formatquery.md), [DTN \_ ](dtn-format.md)et [DTN \_ WMKEYDOWN](dtn-wmkeydown.md) . Pour plus d’informations sur les champs de rappel, consultez [champs de rappel](date-and-time-picker-controls.md).

L’exemple de code C++ suivant identifie le message de notification envoyé par un contrôle de PAO et appelle la fonction appropriée définie par l’application. Reportez-vous aux rubriques suivantes pour obtenir des exemples de code qui illustrent comment traiter les notifications qui s’affichent dans cet exemple.

|   Rubriques                                                                                                     |
|--------------------------------------------------------------------------------------------------------|
| [Comment traiter la notification DTN \_ DATETIMECHANGE](process-the-dtn-datetimechange-notification.md) |
| [Comment traiter la notification DTN \_ FORMATQUERY](process-the-dtn-formatquery-notification.md)       |
| [Comment traiter la notification au \_ format DTN](process-the-dtn-format-notfication.md)                  |
| [Comment traiter la notification DTN \_ WMKEYDOWN](process-the-dtn-wmkeydown-notification.md)           |



 



```C++
BOOL WINAPI DoNotify(HWND hwnd, WPARAM wParam, LPARAM lParam)
{
    LPNMHDR hdr = (LPNMHDR)lParam;

    switch(hdr->code){

        case DTN_DATETIMECHANGE:{
            LPNMDATETIMECHANGE lpChange = (LPNMDATETIMECHANGE)lParam;
            DoDateTimeChange(lpChange);
        }
        break;

        case DTN_FORMATQUERY:{
            LPNMDATETIMEFORMATQUERY lpDTFQuery = (LPNMDATETIMEFORMATQUERY)lParam;

            // Process DTN_FORMATQUERY to ensure that the control
            // displays callback information properly.
            DoFormatQuery(hdr->hwndFrom, lpDTFQuery);
        }
        break;

        case DTN_FORMAT:{
            LPNMDATETIMEFORMAT lpNMFormat = (LPNMDATETIMEFORMAT) lParam;

            // Process DTN_FORMAT to supply information about callback
            // fields (fields) in the DTP control.
            DoFormat(hdr->hwndFrom, lpNMFormat);
        }
        break;

        case DTN_WMKEYDOWN:{
            LPNMDATETIMEWMKEYDOWN lpDTKeystroke = 
                            (LPNMDATETIMEWMKEYDOWN)lParam;

            // Process DTN_WMKEYDOWN to respond to a user's keystroke in
            // a callback field.
            DoWMKeydown(hdr->hwndFrom, lpDTKeystroke);
        }
        break;
    }

    // All of the above notifications require the owner to return zero.
    return FALSE;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Notifications du sélecteur de date et heure](bumper-date-and-time-picker-control-reference-notifications.md)
</dt> <dt>

[Référence de contrôle de sélecteur de date et heure](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Utilisation des contrôles de sélecteur de date et heure](using-date-and-time-picker.md)
</dt> <dt>

[Sélecteur de date et heure](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




