---
title: Gérer les notifications de BCN_DROPDOWN à partir de SplitButtons
description: Cette rubrique décrit une manière possible de répondre à la \_ notification de liste déroulante BCN dans une procédure de dialogue.
ms.assetid: 847DD645-AE29-4F62-BC32-F235BA409E1E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a368dd28c5347f438feff75fbddb129a420caae7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006291"
---
# <a name="how-to-handle-the-bcn_dropdown-notification-from-a-split-button"></a>Gestion \_ de la notification de liste déroulante BCN à partir d’un bouton partagé

Cette rubrique décrit une manière possible de répondre à la notification de [ \_ liste déroulante BCN](bcn-dropdown.md) dans une procédure de dialogue.

L’application C++ récupère les coordonnées clientes du bouton à partir de l’en-tête de notification et les convertit en coordonnées d’écran. Il crée ensuite un menu contextuel et l’affiche en bas du bouton. Pour que l’exemple reste simple, les raccourcis clavier ne sont pas implémentés pour le menu.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions

### <a name="step-1-wait-for-the-bcn_dropdown-notification"></a>Étape 1 : attendez la notification de la *\_ liste déroulante BCN* .


```C++
case BCN_DROPDOWN:
{
    NMBCDROPDOWN* pDropDown = (NMBCDROPDOWN*)lParam;
    if (pDropDown->hdr.hwndFrom = GetDlgItem(hDlg, IDC_SPLIT))
    {
```



### <a name="step-2-get-the-screen-coordinates-of-the-button"></a>Étape 2 : obtenir les coordonnées d’écran du bouton.

Utilisez la fonction [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) pour convertir les coordonnées de la fenêtre du bord inférieur gauche du bouton en coordonnées d’écran.


```C++
POINT pt;
pt.x = pDropDown->rcButton.left;
pt.y = pDropDown->rcButton.bottom;
ClientToScreen(pDropDown->hdr.hwndFrom, &pt);
```



### <a name="step-3-create-a-menu-and-add-items"></a>Étape 3 : créer un menu et ajouter des éléments.

Utilisez la fonction [**CreatePopupMenu**](/windows/desktop/api/winuser/nf-winuser-createpopupmenu) pour créer un menu. Utilisez la fonction [**AppendMenu**](/windows/desktop/menurc/u) pour ajouter des éléments au menu. IDC \_ MENUCOMMAND1 et IDC \_ MENUCOMMAND2 sont des constantes définies par l’application pour les commandes de menu.


```C++
HMENU hSplitMenu = CreatePopupMenu();
AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND1, L"Menu item 1");
AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND2, L"Menu item 2");
```



### <a name="step-4-display-the-menu"></a>Étape 4 : afficher le menu.

La fonction [**TrackPopupMenu**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) affiche un menu contextuel à l’emplacement spécifié et effectue le suivi de la sélection des éléments dans le menu.


```C++
TrackPopupMenu(hSplitMenu, TPM_LEFTALIGN | TPM_TOPALIGN, pt.x, pt.y, 0, hDlg, NULL);
```



## <a name="complete-example"></a>Exemple complet


```C++
case WM_NOTIFY:
    switch (((LPNMHDR)lParam)->code)
    {
        case BCN_DROPDOWN:
        {
            NMBCDROPDOWN* pDropDown = (NMBCDROPDOWN*)lParam;
            if (pDropDown->hdr.hwndFrom = GetDlgItem(hDlg, IDC_SPLIT))
            {

                // Get screen coordinates of the button.
                POINT pt;
                pt.x = pDropDown->rcButton.left;
                pt.y = pDropDown->rcButton.bottom;
                ClientToScreen(pDropDown->hdr.hwndFrom, &pt);
        
                // Create a menu and add items.
                HMENU hSplitMenu = CreatePopupMenu();
                AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND1, L"Menu item 1");
                AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND2, L"Menu item 2");
        
                // Display the menu.
                TrackPopupMenu(hSplitMenu, TPM_LEFTALIGN | TPM_TOPALIGN, pt.x, pt.y, 0, hDlg, NULL);
                return TRUE;
            }
            break;
        }
    }
    return FALSE;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[\_Code de notification de liste déroulante BCN](bcn-dropdown.md)
</dt> <dt>

[À propos des boutons](about-buttons.md)
</dt> <dt>

[Référence du contrôle Button](bumper-button-button-control-reference.md)
</dt> <dt>

[Utilisation des boutons](using-buttons.md)
</dt> <dt>

[Button](buttons.md)
</dt> </dl>

 

 