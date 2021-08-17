---
title: Comment créer des barres d’État
description: Vous pouvez créer une barre d’État à l’aide de la fonction CreateStatusWindow ou à l’aide de la fonction CreateWindowEx et en spécifiant la classe de fenêtre STATUSCLASSNAME.
ms.assetid: 4ED4BFD3-904D-4198-8152-5DD13CA7C189
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7075c8d8896d59a5711d5ee80be4af90948ee4ee99a441fbbf1140cd7452c4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118413187"
---
# <a name="how-to-create-status-bars"></a>Comment créer des barres d’État

Vous pouvez créer une barre d’État à l’aide de la fonction [**CreateStatusWindow**](/windows/desktop/api/Commctrl/nf-commctrl-createstatuswindowa) ou à l’aide de la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) et en spécifiant la classe de fenêtre [**STATUSCLASSNAME**](common-control-window-classes.md) .

Après avoir créé la barre d’État, vous pouvez la diviser en parties, définir le texte pour chaque partie et contrôler l’apparence de la fenêtre à l’aide de messages de barre d’État.

> [!Note]  
> Pour vous assurer que la DLL de contrôles communs est chargée, utilisez d’abord la fonction [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) .

 

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions

### <a name="create-a-status-bar"></a>Créer une barre d’État

L’exemple suivant montre comment créer une barre d’État qui a une poignée de dimensionnement et diviser la fenêtre en quatre parties égales en fonction de la largeur de la zone cliente de la fenêtre parente.


```C++
// Description: 
//   Creates a status bar and divides it into the specified number of parts.
// Parameters:
//   hwndParent - parent window for the status bar.
//   idStatus - child window identifier of the status bar.
//   hinst - handle to the application instance.
//   cParts - number of parts into which to divide the status bar.
// Returns:
//   The handle to the status bar.
//
HWND DoCreateStatusBar(HWND hwndParent, int idStatus, HINSTANCE
                      hinst, int cParts)
{
    HWND hwndStatus;
    RECT rcClient;
    HLOCAL hloc;
    PINT paParts;
    int i, nWidth;

    // Ensure that the common control DLL is loaded.
    InitCommonControls();

    // Create the status bar.
    hwndStatus = CreateWindowEx(
        0,                       // no extended styles
        STATUSCLASSNAME,         // name of status bar class
        (PCTSTR) NULL,           // no text when first created
        SBARS_SIZEGRIP |         // includes a sizing grip
        WS_CHILD | WS_VISIBLE,   // creates a visible child window
        0, 0, 0, 0,              // ignores size and position
        hwndParent,              // handle to parent window
        (HMENU) idStatus,       // child window identifier
        hinst,                   // handle to application instance
        NULL);                   // no window creation data

    // Get the coordinates of the parent window's client area.
    GetClientRect(hwndParent, &rcClient);

    // Allocate an array for holding the right edge coordinates.
    hloc = LocalAlloc(LHND, sizeof(int) * cParts);
    paParts = (PINT) LocalLock(hloc);

    // Calculate the right edge coordinate for each part, and
    // copy the coordinates to the array.
    nWidth = rcClient.right / cParts;
    int rightEdge = nWidth;
    for (i = 0; i < cParts; i++) { 
       paParts[i] = rightEdge;
       rightEdge += nWidth;
    }

    // Tell the status bar to create the window parts.
    SendMessage(hwndStatus, SB_SETPARTS, (WPARAM) cParts, (LPARAM)
               paParts);

    // Free the array, and return.
    LocalUnlock(hloc);
    LocalFree(hloc);
    return hwndStatus;
}  
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des barres d’État](using-status-bars.md)
</dt> <dt>

[Windows démonstration des contrôles communs (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 