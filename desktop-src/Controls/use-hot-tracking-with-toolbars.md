---
title: Utilisation de Hot-Tracking avec des barres d’outils
description: Quand un pointeur de la souris est placé sur un élément, l’élément devient réactif. Si le suivi à chaud est activé, l’élément réactif est mis en surbrillance. Une barre d’outils créée avec le \_ style à deux dimensions TBSTYLE, ou une barre d’outils qui utilise des styles visuels, prend en charge le suivi à chaud par défaut.
ms.assetid: E77B15D7-F0C9-41F7-8BE9-30260FA4BB0C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd735828675ca360cfa91aceefb2d76d34252a96aa7b5edb776e3d48a1fcdc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829083"
---
# <a name="how-to-use-hot-tracking-with-toolbars"></a>Utilisation de Hot-Tracking avec des barres d’outils

Quand un pointeur de la souris est placé sur un élément, l’élément devient réactif. Si le suivi à chaud est activé, l’élément réactif est mis en surbrillance. Une barre d’outils créée avec le style à [**\_ deux dimensions TBSTYLE**](toolbar-control-and-button-styles.md) , ou une barre d’outils qui utilise des [styles visuels](themes-overview.md), prend en charge le suivi à chaud par défaut.

Le suivi à chaud requiert la création de listes d’images ; par conséquent, vous ne pouvez pas utiliser le message [**to \_ ADDBITMAP**](tb-addbitmap.md) ou la fonction [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) pour créer votre barre d’outils.

Lorsque la souris pointe sur un bouton de barre d’outils, le bouton est entouré pour le mettre en surbrillance. L’illustration suivante montre une barre d’outils avec le suivi actif activé ; le pointeur de la souris est positionné sur le bouton enregistrer au moment où la capture d’écran a été effectuée.

![capture d’écran d’une boîte de dialogue avec une barre d’outils à trois éléments ; l’icône sélectionnée est entourée](images/tb-withstyles.png)

Si vous souhaitez qu’une image bitmap de bouton de barre d’outils change lorsque l’état du contrôle change, stockez les différentes images dans les [listes d’images](image-lists.md). Par exemple, certaines applications ont des boutons de barre d’outils noir et blanc qui deviennent colorés lorsqu’ils sont sélectionnés. Les deux images différentes sont stockées dans des listes d’images. Les barres d’outils prennent en charge l’utilisation de trois listes d’images. En général, une application a une liste d’images par défaut, désactivée et de suivi à chaud. Pour définir et récupérer des listes d’images pour les boutons de barre d’outils à chaud, utilisez les messages [**to \_ SETHOTIMAGELIST**](tb-sethotimagelist.md) et [**to \_ GETHOTIMAGELIST**](tb-gethotimagelist.md) .

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions

### <a name="use-hot-tracking-with-a-toolbar"></a>Utiliser Hot-Tracking avec une barre d’outils

L’exemple de code suivant crée, remplit et assigne une liste d’images pour les boutons actifs.


```C++
// Create the image list, himlHot.
g_himlHot = ImageList_Create(MYICON_CX,MYICON_CY,ILC_COLOR8,0,4);

// Load a bitmap from a resource file, and add the images to the image list.
// Note that the bitmap contains four images.

hBitmapHot = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_HOT));

ImageList_Add(g_himlHot, hBitmapHot, NULL);
   
// Set the image list. 
SendMessage(hwndTB, TB_SETHOTIMAGELIST, 0, (LPARAM)g_himlHot);
   
// Loop to fill the array of TBBUTTON structures.  
for(i=0;i<MAX_BUTTONS;i++)
{
    tbArray[i].iBitmap   = i;                   // Bitmap from image list.
    tbArray[i].idCommand = IDM_BUTTONSTART + i;
    tbArray[i].fsState   = TBSTATE_ENABLED;
    tbArray[i].fsStyle   = BTNS_DROPDOWN;
    tbArray[i].dwData    = 0;
    tbArray[i].iString   = i;
}

DeleteObject(hBitmapHot);    // Delete the loaded bitmap.
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des contrôles ToolBar](using-toolbar-controls.md)
</dt> <dt>

[Windows démonstration des contrôles communs (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




