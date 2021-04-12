---
title: Comment créer des barres de défilement
description: Lors de la création d’une fenêtre superposée, indépendante ou enfant, vous pouvez ajouter des barres de défilement standard à l’aide de la fonction CreateWindowEx et en spécifiant WS \_ HSCROLL, WS \_ VSCROLL ou les deux styles.
ms.assetid: 58353030-DCF5-4368-9658-BB282B8B5EF0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06b27e3e6d9495492f46567633cc53b0f3f7c5bd
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463802"
---
# <a name="how-to-create-scroll-bars"></a>Comment créer des barres de défilement

Lors de la création d’une fenêtre superposée, indépendante ou enfant, vous pouvez ajouter des barres de défilement standard à l’aide de la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) et en spécifiant WS \_ HSCROLL, WS \_ VSCROLL ou les deux styles.

## <a name="what-you-need-to-know"></a>Ce que vous devez savoir

### <a name="technologies"></a>Technologies

-   [Contrôles Windows](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Programmation de l’interface utilisateur Windows

## <a name="instructions"></a>Instructions

### <a name="create-a-scroll-bar"></a>Créer une barre de défilement

L’exemple suivant crée une fenêtre avec des barres de défilement horizontales et verticales standard.


```C++
    hwnd = CreateWindowEx( 
        0,                     // no extended styles 
        g_szWindowClass,       // global string containing name of window class
        g_szTitle,             // global string containing title bar text 
        WS_OVERLAPPEDWINDOW |  
            WS_HSCROLL | WS_VSCROLL, // window styles 
        CW_USEDEFAULT,         // default horizontal position 
        CW_USEDEFAULT,         // default vertical position 
        CW_USEDEFAULT,         // default width 
        CW_USEDEFAULT,         // default height 
        (HWND) NULL,           // no parent for overlapped windows 
        (HMENU) NULL,          // use the window class menu 
        g_hInst,               // global instance handle  
        (PVOID) NULL           // pointer not needed 
    ); 
```



Pour traiter les messages de la barre de défilement pour ces barres de défilement, vous devez inclure le code approprié dans la procédure de fenêtre principale.

Vous pouvez utiliser la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) pour créer une barre de défilement en spécifiant la classe de fenêtre ScrollBar. Cela permet de créer une barre de défilement horizontale ou verticale, selon [**que \_ le**](scroll-bar-control-styles.md) style de fenêtre est défini sur le mode de déplacement horizontal ou le mode [**SBS \_**](scroll-bar-control-styles.md) . La taille de la barre de défilement et sa position par rapport à sa fenêtre parente peuvent également être spécifiées.

L’exemple suivant crée une barre de défilement horizontale qui est positionnée le long de la partie inférieure de la zone cliente de la fenêtre parente.


```C++
// Description:
//   Creates a horizontal scroll bar along the bottom of the parent 
//   window's area.
// Parameters:
//   hwndParent - handle to the parent window.
//   sbHeight - height, in pixels, of the scroll bar.
// Returns:
//   The handle to the scroll bar.
HWND CreateAHorizontalScrollBar(HWND hwndParent, int sbHeight)
{
    RECT rect;

    // Get the dimensions of the parent window's client area;
    if (!GetClientRect(hwndParent, &rect))
        return NULL;

    // Create the scroll bar.
    return (CreateWindowEx( 
            0,                      // no extended styles 
            L"SCROLLBAR",           // scroll bar control class 
            (PTSTR) NULL,           // no window text 
            WS_CHILD | WS_VISIBLE   // window styles  
                | SBS_HORZ,         // horizontal scroll bar style 
            rect.left,              // horizontal position 
            rect.bottom - sbHeight, // vertical position 
            rect.right,             // width of the scroll bar 
            sbHeight,               // height of the scroll bar
            hwndParent,             // handle to main window 
            (HMENU) NULL,           // no menu 
            g_hInst,                // instance owning this window 
            (PVOID) NULL            // pointer not needed 
        )); 
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des barres de défilement](using-scroll-bars.md)
</dt> <dt>

[Démonstration des contrôles communs Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 