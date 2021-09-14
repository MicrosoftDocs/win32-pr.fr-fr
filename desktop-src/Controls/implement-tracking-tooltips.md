---
title: Comment implémenter des info-bulles de suivi
description: Les info-bulles de suivi restent visibles jusqu’à ce qu’elles soient explicitement fermées par l’application et peuvent changer la position sur l’écran dynamiquement. Ils sont pris en charge par la version 4,70 et les versions ultérieures des contrôles communs.
ms.assetid: 4BE1F9E6-92B6-4CA7-B89A-F2162BC86366
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a614fef7ed69cd8c2763f9370ce0011d51eb0c82
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999896"
---
# <a name="how-to-implement-tracking-tooltips"></a>Comment implémenter des info-bulles de suivi

Les info-bulles de suivi restent visibles jusqu’à ce qu’elles soient explicitement fermées par l’application et peuvent changer la position sur l’écran dynamiquement. Ils sont pris en charge par la [version 4,70](common-control-versions.md) et les versions ultérieures des contrôles communs.

Pour créer une info-bulle de suivi, incluez l' \_ indicateur de suivi ttf dans le membre **uFlags** de la structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) lors de l’envoi du message [**atténuation \_ ADDTOOL**](ttm-addtool.md) .

Votre application doit activer (afficher) et désactiver (Masquer) manuellement une info-bulle de suivi en envoyant un message [**atténuation \_ TRACKACTIVATE**](ttm-trackactivate.md) . Alors qu’une info-bulle de suivi est active, votre application doit spécifier l’emplacement de l’info-bulle en envoyant des messages [**atténuation \_ TRACKPOSITION**](ttm-trackposition.md) au contrôle ToolTip. Étant donné que l’application gère des tâches telles que le positionnement de l’info-bulle, les info-bulles de suivi n’utilisent pas l’indicateur de **\_ sous-classe ttf** ou le message [**atténuation \_ RELAYEVENT**](ttm-relayevent.md) .

Le message [**atténuation \_ TRACKPOSITION**](ttm-trackposition.md) fait en sorte que le contrôle ToolTip affiche la fenêtre à l’aide de l’un des deux styles de placement :

-   Par défaut, l’info-bulle est affichée à côté de l’outil correspondant dans une position choisie par le contrôle. L’emplacement choisi est relatif aux coordonnées que vous fournissez à l’aide de ce message.
-   Si vous incluez la valeur de **ttf \_ Absolute** dans le membre de la structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) , l’info-bulle est affichée à l’emplacement de pixel spécifié dans le message. Dans ce cas, le contrôle ne tente pas de modifier l’emplacement de la fenêtre d’info-bulle à partir des coordonnées que vous fournissez.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions

### <a name="implement-in-place-tooltips"></a>Implémenter des info-bulles In-Place

Le membre **uFlags** de la structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) utilisé dans l’exemple comprend l’indicateur **\_ absolu ttf** . Sans cet indicateur, le contrôle ToolTip choisit où afficher l’info-bulle, et sa position relative à la boîte de dialogue peut changer soudainement lorsque le pointeur de la souris se déplace.

> [!Note]  
> `g_toolItem` est une structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) globale.

 

L’exemple suivant montre comment créer un contrôle ToolTip de suivi. L’exemple spécifie la zone cliente entière de la fenêtre principale comme outil.


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



### <a name="window-procedure-implementation"></a>Implémentation de la procédure de fenêtre

Lorsque le pointeur de la souris se trouve dans la zone cliente, l’info-bulle est active et affiche les coordonnées du curseur, comme indiqué dans l’illustration suivante.

![capture d’écran d’une boîte de dialogue ; une info-bulle affiche les coordonnées x et y du pointeur de la souris.](images/tt-tracking.png)

L’exemple de code suivant est issu de la procédure de fenêtre pour une boîte de dialogue qui affiche l’info-bulle de suivi créée dans l’exemple précédent. La variable booléenne globale *g \_ TrackingMouse* est utilisée pour déterminer s’il est nécessaire de réactiver l’info-bulle et de réinitialiser le suivi de la souris afin que l’application soit avertie lorsque le pointeur de la souris quitte la zone cliente de la boîte de dialogue.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des contrôles ToolTip](using-tooltip-contro.md)
</dt> </dl>

 

 




