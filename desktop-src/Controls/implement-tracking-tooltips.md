---
title: Comment implémenter des info-bulles de suivi
description: Les info-bulles de suivi restent visibles jusqu’à ce qu’elles soient explicitement fermées par l’application et peuvent changer la position sur l’écran dynamiquement. Ils sont pris en charge par la version 4,70 et les versions ultérieures des contrôles communs.
ms.assetid: 4BE1F9E6-92B6-4CA7-B89A-F2162BC86366
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a614fef7ed69cd8c2763f9370ce0011d51eb0c82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028780"
---
# <a name="how-to-implement-tracking-tooltips"></a><span data-ttu-id="32ea2-104">Comment implémenter des info-bulles de suivi</span><span class="sxs-lookup"><span data-stu-id="32ea2-104">How to Implement Tracking Tooltips</span></span>

<span data-ttu-id="32ea2-105">Les info-bulles de suivi restent visibles jusqu’à ce qu’elles soient explicitement fermées par l’application et peuvent changer la position sur l’écran dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="32ea2-105">Tracking tooltips remain visible until they are explicitly closed by the application, and can change position on the screen dynamically.</span></span> <span data-ttu-id="32ea2-106">Ils sont pris en charge par la [version 4,70](common-control-versions.md) et les versions ultérieures des contrôles communs.</span><span class="sxs-lookup"><span data-stu-id="32ea2-106">They are supported by [version 4.70](common-control-versions.md) and later of the common controls.</span></span>

<span data-ttu-id="32ea2-107">Pour créer une info-bulle de suivi, incluez l' \_ indicateur de suivi ttf dans le membre **uFlags** de la structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) lors de l’envoi du message [**atténuation \_ ADDTOOL**](ttm-addtool.md) .</span><span class="sxs-lookup"><span data-stu-id="32ea2-107">To create a tracking tooltip, include the TTF\_TRACK flag in the **uFlags** member of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure when sending the [**TTM\_ADDTOOL**](ttm-addtool.md) message.</span></span>

<span data-ttu-id="32ea2-108">Votre application doit activer (afficher) et désactiver (Masquer) manuellement une info-bulle de suivi en envoyant un message [**atténuation \_ TRACKACTIVATE**](ttm-trackactivate.md) .</span><span class="sxs-lookup"><span data-stu-id="32ea2-108">Your application must manually activate (show) and deactivate (hide) a tracking tooltip by sending a [**TTM\_TRACKACTIVATE**](ttm-trackactivate.md) message.</span></span> <span data-ttu-id="32ea2-109">Alors qu’une info-bulle de suivi est active, votre application doit spécifier l’emplacement de l’info-bulle en envoyant des messages [**atténuation \_ TRACKPOSITION**](ttm-trackposition.md) au contrôle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="32ea2-109">While a tracking tooltip is active, your application must specify the location of the tooltip by sending [**TTM\_TRACKPOSITION**](ttm-trackposition.md) messages to the tooltip control.</span></span> <span data-ttu-id="32ea2-110">Étant donné que l’application gère des tâches telles que le positionnement de l’info-bulle, les info-bulles de suivi n’utilisent pas l’indicateur de **\_ sous-classe ttf** ou le message [**atténuation \_ RELAYEVENT**](ttm-relayevent.md) .</span><span class="sxs-lookup"><span data-stu-id="32ea2-110">Because the application handles tasks such as positioning the tooltip, tracking tooltips do not use the **TTF\_SUBCLASS** flag or the [**TTM\_RELAYEVENT**](ttm-relayevent.md) message.</span></span>

<span data-ttu-id="32ea2-111">Le message [**atténuation \_ TRACKPOSITION**](ttm-trackposition.md) fait en sorte que le contrôle ToolTip affiche la fenêtre à l’aide de l’un des deux styles de placement :</span><span class="sxs-lookup"><span data-stu-id="32ea2-111">The [**TTM\_TRACKPOSITION**](ttm-trackposition.md) message causes the tooltip control to display the window using one of two placement styles:</span></span>

-   <span data-ttu-id="32ea2-112">Par défaut, l’info-bulle est affichée à côté de l’outil correspondant dans une position choisie par le contrôle.</span><span class="sxs-lookup"><span data-stu-id="32ea2-112">By default, the tooltip is displayed next to the corresponding tool in a position that the control chooses.</span></span> <span data-ttu-id="32ea2-113">L’emplacement choisi est relatif aux coordonnées que vous fournissez à l’aide de ce message.</span><span class="sxs-lookup"><span data-stu-id="32ea2-113">The location chosen is relative to the coordinates that you provide by using this message.</span></span>
-   <span data-ttu-id="32ea2-114">Si vous incluez la valeur de **ttf \_ Absolute** dans le membre de la structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) , l’info-bulle est affichée à l’emplacement de pixel spécifié dans le message.</span><span class="sxs-lookup"><span data-stu-id="32ea2-114">If you include the **TTF\_ABSOLUTE** value in the member of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure, the tooltip is displayed at the pixel location specified in the message.</span></span> <span data-ttu-id="32ea2-115">Dans ce cas, le contrôle ne tente pas de modifier l’emplacement de la fenêtre d’info-bulle à partir des coordonnées que vous fournissez.</span><span class="sxs-lookup"><span data-stu-id="32ea2-115">In this case, the control does not attempt to change the tooltip window's location from the coordinates you provide.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="32ea2-116">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="32ea2-116">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="32ea2-117">Technologies</span><span class="sxs-lookup"><span data-stu-id="32ea2-117">Technologies</span></span>

-   [<span data-ttu-id="32ea2-118">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="32ea2-118">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="32ea2-119">Prérequis</span><span class="sxs-lookup"><span data-stu-id="32ea2-119">Prerequisites</span></span>

-   <span data-ttu-id="32ea2-120">C/C++</span><span class="sxs-lookup"><span data-stu-id="32ea2-120">C/C++</span></span>
-   <span data-ttu-id="32ea2-121">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="32ea2-121">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="32ea2-122">Instructions</span><span class="sxs-lookup"><span data-stu-id="32ea2-122">Instructions</span></span>

### <a name="implement-in-place-tooltips"></a><span data-ttu-id="32ea2-123">Implémenter des info-bulles In-Place</span><span class="sxs-lookup"><span data-stu-id="32ea2-123">Implement In-Place Tooltips</span></span>

<span data-ttu-id="32ea2-124">Le membre **uFlags** de la structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) utilisé dans l’exemple comprend l’indicateur **\_ absolu ttf** .</span><span class="sxs-lookup"><span data-stu-id="32ea2-124">The **uFlags** member of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure that is used in the example includes the **TTF\_ABSOLUTE** flag.</span></span> <span data-ttu-id="32ea2-125">Sans cet indicateur, le contrôle ToolTip choisit où afficher l’info-bulle, et sa position relative à la boîte de dialogue peut changer soudainement lorsque le pointeur de la souris se déplace.</span><span class="sxs-lookup"><span data-stu-id="32ea2-125">Without this flag, the tooltip control chooses where to display the tooltip, and its position relative to the dialog box may change suddenly as the mouse pointer moves.</span></span>

> [!Note]  
> <span data-ttu-id="32ea2-126">`g_toolItem` est une structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) globale.</span><span class="sxs-lookup"><span data-stu-id="32ea2-126">`g_toolItem` is a global [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span>

 

<span data-ttu-id="32ea2-127">L’exemple suivant montre comment créer un contrôle ToolTip de suivi.</span><span class="sxs-lookup"><span data-stu-id="32ea2-127">The following example demonstrates how to create a tracking tooltip control.</span></span> <span data-ttu-id="32ea2-128">L’exemple spécifie la zone cliente entière de la fenêtre principale comme outil.</span><span class="sxs-lookup"><span data-stu-id="32ea2-128">The example specifies the main window's entire client area as the tool.</span></span>


```C++
HWND CreateTrackingToolTip(int toolID, HWND hDlg, WCHAR* pText)
{
    // Create a tooltip.
    HWND hwndTT = CreateWindowEx(WS_EX_TOPMOST, TOOLTIPS_CLASS, NULL, 
                                 WS_POPUP | TTS_NOPREFIX | TTS_ALWAYSTIP, 
                                 CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, 
                                 hDlg, NULL, g_hInst,NULL);

    if (!hwndTT)
    {
      return NULL;
    }

    // Set up the tool information. In this case, the "tool" is the entire parent window.
    
    g_toolItem.cbSize   = sizeof(TOOLINFO);
    g_toolItem.uFlags   = TTF_IDISHWND | TTF_TRACK | TTF_ABSOLUTE;
    g_toolItem.hwnd     = hDlg;
    g_toolItem.hinst    = g_hInst;
    g_toolItem.lpszText = pText;
    g_toolItem.uId      = (UINT_PTR)hDlg;
    
    GetClientRect (hDlg, &g_toolItem.rect);

    // Associate the tooltip with the tool window.
    
    SendMessage(hwndTT, TTM_ADDTOOL, 0, (LPARAM) (LPTOOLINFO) &g_toolItem); 
    
    return hwndTT;
}
            
```



### <a name="window-procedure-implementation"></a><span data-ttu-id="32ea2-129">Implémentation de la procédure de fenêtre</span><span class="sxs-lookup"><span data-stu-id="32ea2-129">Window Procedure Implementation</span></span>

<span data-ttu-id="32ea2-130">Lorsque le pointeur de la souris se trouve dans la zone cliente, l’info-bulle est active et affiche les coordonnées du curseur, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="32ea2-130">When the mouse pointer is within the client area, the tooltip is active and displays the cursor coordinates, as shown in the following illustration.</span></span>

![capture d’écran d’une boîte de dialogue ; une info-bulle affiche les coordonnées x et y du pointeur de la souris.](images/tt-tracking.png)

<span data-ttu-id="32ea2-132">L’exemple de code suivant est issu de la procédure de fenêtre pour une boîte de dialogue qui affiche l’info-bulle de suivi créée dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="32ea2-132">The following example code is from the window procedure for a dialog box that displays the tracking tooltip created in the preceding example.</span></span> <span data-ttu-id="32ea2-133">La variable booléenne globale *g \_ TrackingMouse* est utilisée pour déterminer s’il est nécessaire de réactiver l’info-bulle et de réinitialiser le suivi de la souris afin que l’application soit avertie lorsque le pointeur de la souris quitte la zone cliente de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="32ea2-133">The global Boolean variable *g\_TrackingMouse* is used to determine whether it is necessary to reactivate the tooltip and reset mouse tracking so that the application is notified when the mouse pointer leaves the client area of the dialog box.</span></span>


```
//g_hwndTrackingTT is a global HWND variable

case WM_INITDIALOG:

        InitCommonControls();
        g_hwndTrackingTT = CreateTrackingToolTip(IDC_BUTTON1, hDlg, L"");
        return TRUE;

case WM_MOUSELEAVE: // The mouse pointer has left our window. Deactivate the tooltip.
    
    SendMessage(g_hwndTrackingTT, TTM_TRACKACTIVATE, (WPARAM)FALSE, (LPARAM)&g_toolItem);
    g_TrackingMouse = FALSE;
    return FALSE;

case WM_MOUSEMOVE:

    static int oldX, oldY;
    int newX, newY;

    if (!g_TrackingMouse)   // The mouse has just entered the window.
    {                       // Request notification when the mouse leaves.
    
        TRACKMOUSEEVENT tme = { sizeof(TRACKMOUSEEVENT) };
        tme.hwndTrack       = hDlg;
        tme.dwFlags         = TME_LEAVE;
        
        TrackMouseEvent(&tme);

        // Activate the tooltip.
        SendMessage(g_hwndTrackingTT, TTM_TRACKACTIVATE, (WPARAM)TRUE, (LPARAM)&g_toolItem);
        
        g_TrackingMouse = TRUE;
    }

    newX = GET_X_LPARAM(lParam);
    newY = GET_Y_LPARAM(lParam);

    // Make sure the mouse has actually moved. The presence of the tooltip 
    // causes Windows to send the message continuously.
    
    if ((newX != oldX) || (newY != oldY))
    {
        oldX = newX;
        oldY = newY;
            
        // Update the text.
        WCHAR coords[12];
        swprintf_s(coords, ARRAYSIZE(coords), L"%d, %d", newX, newY);
        
        g_toolItem.lpszText = coords;
        SendMessage(g_hwndTrackingTT, TTM_SETTOOLINFO, 0, (LPARAM)&g_toolItem);

        // Position the tooltip. The coordinates are adjusted so that the tooltip does not overlap the mouse pointer.
        
        POINT pt = { newX, newY }; 
        ClientToScreen(hDlg, &pt);
        SendMessage(g_hwndTrackingTT, TTM_TRACKPOSITION, 0, (LPARAM)MAKELONG(pt.x + 10, pt.y - 20));
    }
    return FALSE;
```



## <a name="related-topics"></a><span data-ttu-id="32ea2-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="32ea2-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32ea2-135">Utilisation des contrôles ToolTip</span><span class="sxs-lookup"><span data-stu-id="32ea2-135">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 




