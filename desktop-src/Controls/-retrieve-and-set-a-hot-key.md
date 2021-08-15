---
title: Comment récupérer et définir une touche d’accès rapide
description: Cette rubrique montre comment récupérer ou définir la combinaison de touches pour un contrôle de touche d’accès rapide.
ms.assetid: F3643196-F847-4EE4-97ED-75AF52D4FF8D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fac5d0bab71fea11fe3d2aba23405f6d7ee7fb1ed8c78f2578f034ae9c84cad8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119079493"
---
# <a name="how-to-retrieve-and-set-a-hot-key"></a>Comment récupérer et définir une touche d’accès rapide

Cette rubrique montre comment récupérer ou définir la combinaison de touches pour un contrôle de touche d’accès rapide. Le message [**hkm \_ SETHOTKEY**](hkm-sethotkey.md) permet à une application de définir la combinaison de touches d’accès rapide pour un contrôle de touche d’accès rapide. Les applications utilisent le message [**hkm \_ GETHOTKEY**](hkm-gethotkey.md) pour récupérer le code de touche virtuel et les indicateurs de modificateur de la touche d’accès rapide choisie par l’utilisateur.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions


Utilisez le message [**hkm \_ GETHOTKEY**](hkm-gethotkey.md) pour récupérer le code de touche virtuelle et les touches de modification qui décrivent une touche d’accès rapide choisie par l’utilisateur. Utilisez le message [**hkm \_ SETHOTKEY**](hkm-sethotkey.md) pour définir ces valeurs pour une touche d’accès rapide.

Dans l’exemple de code C++ suivant, la fonction définie par l’application utilise le message [**hkm \_ GETHOTKEY**](hkm-gethotkey.md) pour récupérer une combinaison de touches à partir d’un contrôle de touche d’accès rapide, puis utilise le message [**WM \_ SETHOTKEY**](/windows/desktop/inputdev/wm-sethotkey) pour définir une touche d’accès rapide globale. Notez que vous ne pouvez pas définir une touche d’accès rapide globale pour une fenêtre qui a le style de fenêtre [**\_ enfant WS**](/windows/desktop/winmsg/window-styles) .



```C++
// Retrieves the hot key from the hot key control and sets it as
// the hot key for the application's main window. 
//
// Parameters 
//     hwndHot  - Handle of the hot key control. 
//     hwndMain - Handle of the main window. 

BOOL WINAPI ProcessHotkey(HWND hwndHot, HWND hwndMain) 
{ 
    WORD wHotkey;  

    // Retrieve the hot key (virtual key code and modifiers). 
    wHotkey = (WORD) SendMessage(hwndHot, HKM_GETHOTKEY, 0, 0); 
    
    // Use the result as wParam for WM_SETHOTKEY. 
    SendMessage(hwndMain, WM_SETHOTKEY, wHotkey, 0); 
    return TRUE;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence de contrôle de touche d’accès rapide](bumper-hot-key-hot-key-control-reference.md)
</dt> <dt>

[À propos des contrôles de touche d’accès rapide](hot-key-controls.md)
</dt> <dt>

[Utilisation des contrôles de touche d’accès rapide](using-hot-key-controls.md)
</dt> </dl>

 

 