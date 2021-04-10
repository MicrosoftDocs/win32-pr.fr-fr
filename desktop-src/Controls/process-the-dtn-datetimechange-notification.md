---
title: Comment traiter la notification de DTN_DATETIMECHANGE
description: Cette rubrique montre comment traiter la notification des modifications apportées par l’utilisateur au contrôle de sélecteur de date et d’heure (PAO).
ms.assetid: AE029962-E9D3-47BC-A24F-312B54137F18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5434c7ebbda673f76a757375e9a3d23504483d42
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103941511"
---
# <a name="how-to-process-the-dtn_datetimechange-notification"></a>Comment traiter la notification DTN \_ DATETIMECHANGE

Cette rubrique montre comment traiter la notification des modifications apportées par l’utilisateur au contrôle de sélecteur de date et d’heure (PAO).

## <a name="what-you-need-to-know"></a>Ce que vous devez savoir

### <a name="technologies"></a>Technologies

-   [Contrôles Windows](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Programmation de l’interface utilisateur Windows

## <a name="instructions"></a>Instructions


Un contrôle de PAO envoie le code de notification [DTN \_ DATETIMECHANGE](dtn-datetimechange.md) à chaque fois qu’une modification se produit. Par exemple, cette notification est générée lorsque l’utilisateur modifie l’un des champs du contrôle ou, dans le cas où le contrôle est défini sur le style [**DTS \_ SHOWNONE**](date-and-time-picker-control-styles.md) , lorsque l’utilisateur modifie l’état de la case à cocher du contrôle.

Votre application doit inclure du code pour traiter \_ les messages DTN DATETIMECHANGE qui sont envoyés par le contrôle PAO.

L’exemple de code C++ suivant est une fonction définie par l’application conçue pour indiquer l’état d’un contrôle PAO défini sur le style **DTS \_ SHOWNONE** .



```C++
void WINAPI DoDateTimeChange(LPNMDATETIMECHANGE lpChange)
{
    // If the user has unchecked the DTP's check box, change the
    // text in a static control to show the appropriate message.
    //
    // g_hwndDlg - a program-global address of a dialog box.

    if(lpChange->dwFlags == GDT_NONE)
        SetDlgItemText(g_hwndDlg, IDC_STATUS, L"Disabled");
    else
        SetDlgItemText(g_hwndDlg, IDC_STATUS, L"Active");
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des contrôles de sélecteur de date et heure](using-date-and-time-picker.md)
</dt> <dt>

[Référence de contrôle de sélecteur de date et heure](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Sélecteur de date et heure](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




