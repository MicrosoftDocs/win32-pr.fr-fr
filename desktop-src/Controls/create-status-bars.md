---
title: Comment créer des barres d’État
description: Vous pouvez créer une barre d’État à l’aide de la fonction CreateStatusWindow ou à l’aide de la fonction CreateWindowEx et en spécifiant la classe de fenêtre STATUSCLASSNAME.
ms.assetid: 4ED4BFD3-904D-4198-8152-5DD13CA7C189
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c133d7c7e15e5f43d198f21cadff54bcb4be14c2
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104031907"
---
# <a name="how-to-create-status-bars"></a><span data-ttu-id="0f645-103">Comment créer des barres d’État</span><span class="sxs-lookup"><span data-stu-id="0f645-103">How to Create Status Bars</span></span>

<span data-ttu-id="0f645-104">Vous pouvez créer une barre d’État à l’aide de la fonction [**CreateStatusWindow**](/windows/desktop/api/Commctrl/nf-commctrl-createstatuswindowa) ou à l’aide de la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) et en spécifiant la classe de fenêtre [**STATUSCLASSNAME**](common-control-window-classes.md) .</span><span class="sxs-lookup"><span data-stu-id="0f645-104">You can create a status bar by using the [**CreateStatusWindow**](/windows/desktop/api/Commctrl/nf-commctrl-createstatuswindowa) function or by using the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function and specifying the [**STATUSCLASSNAME**](common-control-window-classes.md) window class.</span></span>

<span data-ttu-id="0f645-105">Après avoir créé la barre d’État, vous pouvez la diviser en parties, définir le texte pour chaque partie et contrôler l’apparence de la fenêtre à l’aide de messages de barre d’État.</span><span class="sxs-lookup"><span data-stu-id="0f645-105">After you create the status bar, you can divide it into parts, set the text for each part, and control the appearance of the window by using status bar messages.</span></span>

> [!Note]  
> <span data-ttu-id="0f645-106">Pour vous assurer que la DLL de contrôles communs est chargée, utilisez d’abord la fonction [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) .</span><span class="sxs-lookup"><span data-stu-id="0f645-106">To ensure that the common control DLL is loaded, use the [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) function first.</span></span>

 

## <a name="what-you-need-to-know"></a><span data-ttu-id="0f645-107">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="0f645-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="0f645-108">Technologies</span><span class="sxs-lookup"><span data-stu-id="0f645-108">Technologies</span></span>

-   [<span data-ttu-id="0f645-109">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="0f645-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="0f645-110">Prérequis</span><span class="sxs-lookup"><span data-stu-id="0f645-110">Prerequisites</span></span>

-   <span data-ttu-id="0f645-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="0f645-111">C/C++</span></span>
-   <span data-ttu-id="0f645-112">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="0f645-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="0f645-113">Instructions</span><span class="sxs-lookup"><span data-stu-id="0f645-113">Instructions</span></span>

### <a name="create-a-status-bar"></a><span data-ttu-id="0f645-114">Créer une barre d’État</span><span class="sxs-lookup"><span data-stu-id="0f645-114">Create a Status Bar</span></span>

<span data-ttu-id="0f645-115">L’exemple suivant montre comment créer une barre d’État qui a une poignée de dimensionnement et diviser la fenêtre en quatre parties égales en fonction de la largeur de la zone cliente de la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="0f645-115">The following example demonstrates how to create a status bar that has a sizing grip and divide the window into four equal parts based on the width of the parent window's client area.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="0f645-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0f645-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f645-117">Utilisation des barres d’État</span><span class="sxs-lookup"><span data-stu-id="0f645-117">Using Status Bars</span></span>](using-status-bars.md)
</dt> <dt>

<span data-ttu-id="0f645-118">[Démonstration des contrôles communs Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="0f645-118">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 