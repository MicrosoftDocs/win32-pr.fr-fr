---
title: Comment créer un contrôle ComboBoxEx
description: Cette rubrique montre comment créer un contrôle ComboBoxEx.
ms.assetid: E3D577AF-3290-431E-AA6C-1E9A9ED6448C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73989124982cb563fc008d7f3c543388cca685a5
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103941508"
---
# <a name="how-to-create-a-comboboxex-control"></a>Comment créer un contrôle ComboBoxEx

Cette rubrique montre comment créer un contrôle ComboBoxEx.

## <a name="what-you-need-to-know"></a>Ce que vous devez savoir

### <a name="technologies"></a>Technologies

-   [Contrôles Windows](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Programmation de l’interface utilisateur Windows

## <a name="instructions"></a>Instructions


Pour créer un contrôle ComboBoxEx, appelez la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , en utilisant [**WC \_ ComboBoxEx**](common-control-window-classes.md) comme classe de fenêtre. Vous devez d’abord inscrire la classe de fenêtre en appelant la fonction [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) , tout en spécifiant le \_ bit des classes ICC USEREX \_ dans la structure [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) qui l’accompagne.

## <a name="complete-example"></a>Exemple complet

La fonction définie par l’application suivante crée un contrôle ComboBoxEx avec le style de [**\_ liste déroulante CBS**](combo-box-styles.md) dans la fenêtre principale.


```C++
// CreateComboEx - Registers the ComboBoxEx window class and creates
// a ComboBoxEx control in the client area of the main window.
//
// g_hwndMain - A handle to the main window.
// g_hinst    - A handle to the program instance.
HWND WINAPI CreateComboEx(void)
{
    HWND hwnd;
    INITCOMMONCONTROLSEX icex;

    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icex.dwICC = ICC_USEREX_CLASSES;

    InitCommonControlsEx(&icex);

    hwnd = CreateWindowEx(0, WC_COMBOBOXEX, NULL,
                    WS_BORDER | WS_VISIBLE |
                    WS_CHILD | CBS_DROPDOWN,
                    // No size yet--resize after setting image list.
                    0,      // Vertical position of Combobox
                    0,      // Horizontal position of Combobox
                    0,      // Sets the width of Combobox
                    100,    // Sets the height of Combobox
                    g_hwndMain,
                    NULL,
                    g_hinst,
                    NULL);

    return (hwnd);
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

 

 