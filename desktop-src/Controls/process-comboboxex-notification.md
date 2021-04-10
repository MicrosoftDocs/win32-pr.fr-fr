---
title: Traitement des notifications ComboBoxEx
description: Cette rubrique montre comment traiter les messages de notification ComboBoxEx.
ms.assetid: 375634BC-CDD6-4D72-A41E-FCBFCBFE7F03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a9787e22aa01d51478ca55f0dde5d7ac944decb
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103941512"
---
# <a name="how-to-process-comboboxex-notifications"></a>Traitement des notifications ComboBoxEx

Cette rubrique montre comment traiter les messages de notification ComboBoxEx.

## <a name="what-you-need-to-know"></a>Ce que vous devez savoir

### <a name="technologies"></a>Technologies

-   [Contrôles Windows](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Programmation de l’interface utilisateur Windows

## <a name="instructions"></a>Instructions


Un contrôle ComboBoxEx informe sa fenêtre parente d’événements en envoyant des messages de [**\_ notification WM**](wm-notify.md) . Il transmet également les messages de notification de [**\_ commande WM**](/windows/desktop/menurc/wm-command) qu’il reçoit de la zone de liste déroulante qu’il contient à la fenêtre parente à traiter. Par conséquent, votre application doit être préparée à traiter les messages de **\_ notification WM** à partir des messages de **\_ commande** ComboBoxEx et WM qui sont transférés à partir du contrôle de zone de liste déroulante enfant ComboBoxEx.

L’exemple de cette section gère les messages [**WM \_ Notify**](wm-notify.md) et la [**\_ commande WM**](/windows/desktop/menurc/wm-command) à partir d’un contrôle ComboBoxEx en appelant une fonction définie par l’application correspondante pour traiter ces messages.

## <a name="complete-example"></a>Exemple complet


```C++
LRESULT CALLBACK WndProc (HWND hwnd, UINT msg, WPARAM wParam, LPARAM lParam)
{
    switch(msg){

        case WM_COMMAND: // notification from the child ComboBox within the ComboBoxEx control.
            if((HWND)lParam == g_hwndCB)
                DoOldNotify(hwnd,  wParam);  
            break;

        case WM_NOTIFY: // notification from the ComboBoxEx control
            return (DoCBEXNotify(hwnd, lParam));

        case WM_PAINT:
            hdc = BeginPaint(hwnd, &ps);
            EndPaint(hwnd, &ps);
            break;

        case WM_DESTROY:
            PostQuitMessage(0);
            break;

        default:
            return DefWindowProc(hwnd, msg, wParam, lParam);
            break;
    }

    return FALSE;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos des contrôles ComboBoxEx](comboboxex-controls.md)
</dt> <dt>

[Référence du contrôle ComboBoxEx](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[Utilisation des contrôles ComboBoxEx](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[ComboBoxEx](comboboxex-control-reference.md)
</dt> </dl>

 

 