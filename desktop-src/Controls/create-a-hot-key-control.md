---
title: Comment créer un contrôle de touche d’accès rapide
description: Cette rubrique montre comment créer un contrôle de touche d’accès rapide. Vous créez un contrôle de touche d’accès rapide à l’aide de la fonction CreateWindowEx, en spécifiant la classe de fenêtre de raccourci de \_ classe.
ms.assetid: A6723D4E-B8F6-4365-8FCD-99B73D2C0470
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 081db39f07e8d80fcbb5a437bc8cbe83473b4299282c8b2437d95acda02b2db9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119577040"
---
# <a name="how-to-create-a-hot-key-control"></a>Comment créer un contrôle de touche d’accès rapide

Cette rubrique montre comment créer un contrôle de touche d’accès rapide. Vous créez un contrôle de touche d’accès rapide à l’aide de la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , en spécifiant la classe de fenêtre de raccourci de \_ classe.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions


Avant de créer le contrôle de touche d’accès rapide, assurez-vous que la DLL de contrôles communs est chargée.

Dans l’exemple de code C++ suivant, la fonction définie par l’application appelle la fonction [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) pour charger la dll de contrôle commune. Elle appelle ensuite la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , en spécifiant la classe de fenêtre de raccourcis de la **\_ classe** , pour créer un contrôle de touche d’accès rapide. Elle utilise les messages [**hkm \_ SETRULES**](hkm-setrules.md) et [**hkm \_ SETHOTKEY**](hkm-sethotkey.md) pour initialiser le contrôle et retourne un handle pour le contrôle.

Ce contrôle de touche d’accès rapide ne permet pas à l’utilisateur de choisir une touche d’accès rapide qui est une seule clé non modifiée, pas plus qu’il ne permet à l’utilisateur de choisir uniquement Maj et une clé. Ces règles empêchent l’utilisateur de choisir une touche d’accès rapide qui peut être entrée accidentellement lors de la saisie de texte.



```C++
// Creates a hot key control and sets rules and default settings for it.
// 
// Returns the handle of the hot key control. 
//
// Parameter
//     hwndDlg - Handle of the parent window (dialog box). 
// 
// Global variable 
//     g_hinst - Handle of the application instance. 

extern HINSTANCE g_hinst; 

HWND WINAPI InitializeHotkey(HWND hwndDlg) 
{ 
    HWND hwndHot = NULL;
    
    // Ensure that the common control DLL is loaded. 
    INITCOMMONCONTROLSEX icex;  //declare an INITCOMMONCONTROLSEX Structure
    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icex.dwICC = ICC_HOTKEY_CLASS;   //set dwICC member to ICC_HOTKEY_CLASS    
                                     // this loads the Hot Key control class.
    InitCommonControlsEx(&icex);  
 
    hwndHot = CreateWindowEx(0,                        // no extended styles 
                             HOTKEY_CLASS,             // class name 
                             TEXT(""),                 // no title (caption) 
                             WS_CHILD | WS_VISIBLE,    // style 
                             15, 10,                   // position 
                             200, 20,                  // size 
                             hwndDlg,                  // parent window 
                             NULL,                     // uses class menu 
                             g_hinst,                  // instance 
                             NULL);                    // no WM_CREATE parameter 
 
    SetFocus(hwndHot); 
 
    // Set rules for invalid key combinations. If the user does not supply a
    // modifier key, use ALT as a modifier. If the user supplies SHIFT as a 
    // modifier key, use SHIFT + ALT instead.
    SendMessage(hwndHot, 
                HKM_SETRULES, 
                (WPARAM) HKCOMB_NONE | HKCOMB_S,   // invalid key combinations 
                MAKELPARAM(HOTKEYF_ALT, 0));       // add ALT to invalid entries 
 
    // Set CTRL + ALT + A as the default hot key for this window. 
    // 0x41 is the virtual key code for 'A'. 
    SendMessage(hwndHot, 
                HKM_SETHOTKEY, 
                MAKEWORD(0x41, HOTKEYF_CONTROL | HOTKEYF_ALT), 
                0); 
 
    return hwndHot; 
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

 

 