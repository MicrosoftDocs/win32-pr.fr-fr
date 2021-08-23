---
title: Comment gérer les boutons déroulants
description: Un bouton déroulant peut présenter aux utilisateurs une liste d’options.
ms.assetid: 2D908D4B-AA8B-4DEF-B656-C37B673ABB4D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b74443b0d29b3ab39255d7417fd13677769f6a762ebe176e8301a76029db0c37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544946"
---
# <a name="how-to-handle-drop-down-buttons"></a>Comment gérer les boutons déroulants

Un bouton déroulant peut présenter aux utilisateurs une liste d’options. Pour créer ce style de bouton, spécifiez le style de [**\_ liste déroulante BTNS**](toolbar-control-and-button-styles.md) (également appelé [**\_ liste**](toolbar-control-and-button-styles.md) déroulante TBSTYLE pour la compatibilité avec les versions précédentes des contrôles communs). Pour afficher un bouton déroulant avec une flèche, vous devez également définir le style de barre d’outils [**TBSTYLE \_ ex \_ DRAWDDARROWS**](toolbar-extended-styles.md) en envoyant un message [**to \_ SETEXTENDEDSTYLE**](tb-setextendedstyle.md) .

L’illustration suivante montre un bouton déroulant « ouvrir » avec le menu contextuel ouvert et affichant une liste de fichiers. Dans cet exemple, la barre d’outils a le style [**TBSTYLE \_ ex \_ DRAWDDARROWS**](toolbar-extended-styles.md) .

![capture d’écran d’une boîte de dialogue avec trois éléments de barre d’outils représentés par des icônes ; l’un contient une flèche de déroulement développée et un menu contextuel à trois éléments.](images/tb-dropdown.png)

L’illustration suivante montre la même barre d’outils, cette fois sans le style [**TBSTYLE \_ ex \_ DRAWDDARROWS**](toolbar-extended-styles.md) .

![capture d’écran d’une boîte de dialogue précédente, mais l’icône avec le menu contextuel n’a pas de flèche déroulante](images/tb-dropdown2.png)

Quand les utilisateurs cliquent sur un bouton de barre d’outils qui utilise le style de [**\_ liste déroulante BTNS**](toolbar-control-and-button-styles.md) , le contrôle ToolBar envoie à la fenêtre parente un code de notification de [ \_ liste déroulante TBN](tbn-dropdown.md) .

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions

### <a name="handle-a-drop-down-button"></a>Gérer un bouton déroulant

L’exemple de code suivant montre comment une application peut prendre en charge un bouton déroulant dans un contrôle ToolBar.


```C++
BOOL DoNotify(HWND hwnd, UINT msg, WPARAM wParam, LPARAM lParam)
{

    #define lpnm   ((LPNMHDR)lParam)
    #define lpnmTB ((LPNMTOOLBAR)lParam)

    switch(lpnm->code)
    {
        case TBN_DROPDOWN:
        {
            // Get the coordinates of the button.
            RECT rc;
            SendMessage(lpnmTB->hdr.hwndFrom, TB_GETRECT, (WPARAM)lpnmTB->iItem, (LPARAM)&rc);

            // Convert to screen coordinates.            
            MapWindowPoints(lpnmTB->hdr.hwndFrom, HWND_DESKTOP, (LPPOINT)&rc, 2);                         
        
            // Get the menu.
            HMENU hMenuLoaded = LoadMenu(g_hinst, MAKEINTRESOURCE(IDR_POPUP)); 
         
            // Get the submenu for the first menu item.
            HMENU hPopupMenu = GetSubMenu(hMenuLoaded, 0);

            // Set up the pop-up menu.
            // In case the toolbar is too close to the bottom of the screen, 
            // set rcExclude equal to the button rectangle and the menu will appear above 
            // the button, and not below it.
         
            TPMPARAMS tpm;
         
            tpm.cbSize    = sizeof(TPMPARAMS);
            tpm.rcExclude = rc;
         
            // Show the menu and wait for input. 
            // If the user selects an item, its WM_COMMAND is sent.
         
            TrackPopupMenuEx(hPopupMenu, 
                             TPM_LEFTALIGN | TPM_LEFTBUTTON | TPM_VERTICAL, 
                             rc.left, rc.bottom, g_hwndMain, &tpm);

            DestroyMenu(hMenuLoaded);
         
        return (FALSE);
      
        }
    }
   
    return FALSE;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des contrôles ToolBar](using-toolbar-controls.md)
</dt> <dt>

[Windows démonstration des contrôles communs (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




