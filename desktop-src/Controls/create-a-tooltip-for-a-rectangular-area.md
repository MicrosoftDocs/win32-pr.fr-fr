---
title: Comment créer une info-bulle pour une zone rectangulaire
description: L’exemple suivant montre comment créer un contrôle ToolTip standard pour l’ensemble de la zone client d’une fenêtre.
ms.assetid: 6AF1CE6E-AD63-4F84-9759-14FE4F16092B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f8daf62bf2ba85c8750fd07a1b9122b0360fc11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671969"
---
# <a name="how-to-create-a-tooltip-for-a-rectangular-area"></a><span data-ttu-id="67ddb-103">Comment créer une info-bulle pour une zone rectangulaire</span><span class="sxs-lookup"><span data-stu-id="67ddb-103">How to Create a Tooltip for a Rectangular Area</span></span>

<span data-ttu-id="67ddb-104">L’exemple suivant montre comment créer un contrôle ToolTip standard pour l’ensemble de la zone client d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="67ddb-104">The following example demonstrates how to create a standard tooltip control for a window's entire client area.</span></span>

<span data-ttu-id="67ddb-105">L’illustration suivante montre l’info-bulle qui s’affiche lorsque le pointeur de la souris se trouve dans la fenêtre cliente d’une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="67ddb-105">The following illustration shows the tooltip that is displayed when the mouse pointer is within the client window of a dialog box.</span></span> <span data-ttu-id="67ddb-106">Le handle de la boîte de dialogue a été passé à la fonction illustrée dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="67ddb-106">The handle of the dialog box was passed to the function shown in the preceding example.</span></span>

![capture d’écran d’une boîte de dialogue ; le pointeur de la souris se trouve dans la fenêtre du client et une info-bulle est visible](images/tt-rectangle.png)

## <a name="what-you-need-to-know"></a><span data-ttu-id="67ddb-108">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="67ddb-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="67ddb-109">Technologies</span><span class="sxs-lookup"><span data-stu-id="67ddb-109">Technologies</span></span>

-   [<span data-ttu-id="67ddb-110">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="67ddb-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="67ddb-111">Prérequis</span><span class="sxs-lookup"><span data-stu-id="67ddb-111">Prerequisites</span></span>

-   <span data-ttu-id="67ddb-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="67ddb-112">C/C++</span></span>
-   <span data-ttu-id="67ddb-113">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="67ddb-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="67ddb-114">Instructions</span><span class="sxs-lookup"><span data-stu-id="67ddb-114">Instructions</span></span>

### <a name="create-a-tooltip-for-a-rectangular-area"></a><span data-ttu-id="67ddb-115">Créer une info-bulle pour une zone rectangulaire</span><span class="sxs-lookup"><span data-stu-id="67ddb-115">Create a Tooltip for a Rectangular Area</span></span>

<span data-ttu-id="67ddb-116">L’exemple suivant montre comment créer un contrôle ToolTip standard pour l’ensemble de la zone client d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="67ddb-116">The following example demonstrates how to create a standard tooltip control for a window's entire client area.</span></span>


```C++
void CreateToolTipForRect(HWND hwndParent)
{
    // Create a tooltip.
    HWND hwndTT = CreateWindowEx(WS_EX_TOPMOST, TOOLTIPS_CLASS, NULL, 
                                 WS_POPUP | TTS_NOPREFIX | TTS_ALWAYSTIP, 
                                 CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, 
                                 hwndParent, NULL, g_hInst,NULL);

    SetWindowPos(hwndTT, HWND_TOPMOST, 0, 0, 0, 0, 
                 SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE);

    // Set up "tool" information. In this case, the "tool" is the entire parent window.
    
    TOOLINFO ti = { 0 };
    ti.cbSize   = sizeof(TOOLINFO);
    ti.uFlags   = TTF_SUBCLASS;
    ti.hwnd     = hwndParent;
    ti.hinst    = g_hInst;
    ti.lpszText = TEXT("This is your tooltip string.");;
    
    GetClientRect (hwndParent, &ti.rect);

    // Associate the tooltip with the "tool" window.
    SendMessage(hwndTT, TTM_ADDTOOL, 0, (LPARAM) (LPTOOLINFO) &ti); 
} 
```



## <a name="related-topics"></a><span data-ttu-id="67ddb-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="67ddb-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67ddb-118">Utilisation des contrôles ToolTip</span><span class="sxs-lookup"><span data-stu-id="67ddb-118">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 




