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
# <a name="how-to-create-scroll-bars"></a><span data-ttu-id="77837-103">Comment créer des barres de défilement</span><span class="sxs-lookup"><span data-stu-id="77837-103">How to Create Scroll Bars</span></span>

<span data-ttu-id="77837-104">Lors de la création d’une fenêtre superposée, indépendante ou enfant, vous pouvez ajouter des barres de défilement standard à l’aide de la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) et en spécifiant WS \_ HSCROLL, WS \_ VSCROLL ou les deux styles.</span><span class="sxs-lookup"><span data-stu-id="77837-104">When creating an overlapped, pop-up, or child window, you can add standard scroll bars by using the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function and specifying WS\_HSCROLL, WS\_VSCROLL, or both styles.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="77837-105">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="77837-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="77837-106">Technologies</span><span class="sxs-lookup"><span data-stu-id="77837-106">Technologies</span></span>

-   [<span data-ttu-id="77837-107">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="77837-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="77837-108">Prérequis</span><span class="sxs-lookup"><span data-stu-id="77837-108">Prerequisites</span></span>

-   <span data-ttu-id="77837-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="77837-109">C/C++</span></span>
-   <span data-ttu-id="77837-110">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="77837-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="77837-111">Instructions</span><span class="sxs-lookup"><span data-stu-id="77837-111">Instructions</span></span>

### <a name="create-a-scroll-bar"></a><span data-ttu-id="77837-112">Créer une barre de défilement</span><span class="sxs-lookup"><span data-stu-id="77837-112">Create a Scroll Bar</span></span>

<span data-ttu-id="77837-113">L’exemple suivant crée une fenêtre avec des barres de défilement horizontales et verticales standard.</span><span class="sxs-lookup"><span data-stu-id="77837-113">The following example creates a window with standard horizontal and vertical scroll bars.</span></span>


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



<span data-ttu-id="77837-114">Pour traiter les messages de la barre de défilement pour ces barres de défilement, vous devez inclure le code approprié dans la procédure de fenêtre principale.</span><span class="sxs-lookup"><span data-stu-id="77837-114">To process scroll bar messages for these scroll bars, you must include appropriate code in the main window procedure.</span></span>

<span data-ttu-id="77837-115">Vous pouvez utiliser la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) pour créer une barre de défilement en spécifiant la classe de fenêtre ScrollBar.</span><span class="sxs-lookup"><span data-stu-id="77837-115">You can use the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function to create a scroll bar by specifying the SCROLLBAR window class.</span></span> <span data-ttu-id="77837-116">Cela permet de créer une barre de défilement horizontale ou verticale, selon [**que \_ le**](scroll-bar-control-styles.md) style de fenêtre est défini sur le mode de déplacement horizontal ou le mode [**SBS \_**](scroll-bar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="77837-116">This creates a horizontal or vertical scroll bar, depending on whether [**SBS\_HORZ**](scroll-bar-control-styles.md) or [**SBS\_VERT**](scroll-bar-control-styles.md) is specified as the window style.</span></span> <span data-ttu-id="77837-117">La taille de la barre de défilement et sa position par rapport à sa fenêtre parente peuvent également être spécifiées.</span><span class="sxs-lookup"><span data-stu-id="77837-117">The scroll bar size and its position relative to its parent window can also be specified.</span></span>

<span data-ttu-id="77837-118">L’exemple suivant crée une barre de défilement horizontale qui est positionnée le long de la partie inférieure de la zone cliente de la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="77837-118">The following example creates a horizontal scroll bar that is positioned along the bottom of the parent window's client area.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="77837-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="77837-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77837-120">Utilisation des barres de défilement</span><span class="sxs-lookup"><span data-stu-id="77837-120">Using Scroll Bars</span></span>](using-scroll-bars.md)
</dt> <dt>

<span data-ttu-id="77837-121">[Démonstration des contrôles communs Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="77837-121">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 