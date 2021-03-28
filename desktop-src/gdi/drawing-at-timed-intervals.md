---
description: Vous pouvez dessiner aux intervalles chronométrés en créant un minuteur avec la fonction SetTimer.
ms.assetid: 82f9aa5e-8e42-49cf-bcd0-785bc78fe159
title: Dessin à des intervalles chronométrés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1757aca4e6be8f169aea378c52038420519ee879
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528359"
---
# <a name="drawing-at-timed-intervals"></a>Dessin à des intervalles chronométrés

Vous pouvez dessiner aux intervalles chronométrés en créant un minuteur avec la fonction [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) . En utilisant un minuteur pour envoyer des messages [**\_ du minuteur WM**](../winmsg/wm-timer.md) à la procédure de fenêtre à intervalles réguliers, une application peut effectuer une animation simple dans la zone cliente pendant que d’autres applications continuent de s’exécuter.

Dans l’exemple suivant, l’application rebondit une étoile d’un côté à l’autre dans la zone cliente. Chaque fois que la procédure de fenêtre reçoit un message de [**\_ minuteur WM**](../winmsg/wm-timer.md) , la procédure efface l’étoile à la position actuelle, calcule une nouvelle position et dessine l’étoile à l’intérieur de la nouvelle position. La procédure démarre le minuteur en appelant [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) lors du traitement du message [**WM \_ Create**](../winmsg/wm-create.md) .


```C++
RECT rcCurrent = {0,0,20,20}; 
POINT aptStar[6] = {10,1, 1,19, 19,6, 1,6, 19,19, 10,1}; 
int X = 2, Y = -1, idTimer = -1; 
BOOL fVisible = FALSE; 
HDC hdc; 
 
LRESULT APIENTRY WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    PAINTSTRUCT ps; 
    RECT rc; 
 
    switch (message) 
    { 
        case WM_CREATE: 
 
            // Calculate the starting point.  
 
            GetClientRect(hwnd, &rc); 
            OffsetRect(&rcCurrent, rc.right / 2, rc.bottom / 2); 
 
            // Initialize the private DC.  
 
            hdc = GetDC(hwnd); 
            SetViewportOrgEx(hdc, rcCurrent.left, 
                rcCurrent.top, NULL); 
            SetROP2(hdc, R2_NOT); 
 
            // Start the timer.  
 
            SetTimer(hwnd, idTimer = 1, 10, NULL); 
            return 0L; 
 
        case WM_DESTROY: 
            KillTimer(hwnd, 1); 
            PostQuitMessage(0); 
            return 0L; 
 
        case WM_SIZE: 
            switch (wParam) 
            { 
                case SIZE_MINIMIZED: 
 
                    // Stop the timer if the window is minimized. 
 
                    KillTimer(hwnd, 1); 
                    idTimer = -1; 
                    break; 
 
                case SIZE_RESTORED: 
 
                    // Move the star back into the client area  
                    // if necessary.  
 
                    if (rcCurrent.right > (int) LOWORD(lParam)) 
                    {
                        rcCurrent.left = 
                            (rcCurrent.right = 
                                (int) LOWORD(lParam)) - 20; 
                    }
                    if (rcCurrent.bottom > (int) HIWORD(lParam)) 
                    {
                        rcCurrent.top = 
                            (rcCurrent.bottom = 
                                (int) HIWORD(lParam)) - 20; 
                    }
 
                    // Fall through to the next case.  
 
                case SIZE_MAXIMIZED: 
 
                    // Start the timer if it had been stopped.  
 
                    if (idTimer == -1) 
                        SetTimer(hwnd, idTimer = 1, 10, NULL); 
                    break; 
            } 
            return 0L; 
 
        case WM_TIMER: 
 
            // Hide the star if it is visible.  
 
            if (fVisible) 
                Polyline(hdc, aptStar, 6); 
 
            // Bounce the star off a side if necessary.  
 
            GetClientRect(hwnd, &rc); 
            if (rcCurrent.left + X < rc.left || 
                rcCurrent.right + X > rc.right) 
                X = -X; 
            if (rcCurrent.top + Y < rc.top || 
                rcCurrent.bottom + Y > rc.bottom) 
                Y = -Y; 
 
            // Show the star in its new position.  
 
            OffsetRect(&rcCurrent, X, Y); 
            SetViewportOrgEx(hdc, rcCurrent.left, 
                rcCurrent.top, NULL); 
            fVisible = Polyline(hdc, aptStar, 6); 
 
            return 0L; 
 
        case WM_ERASEBKGND: 
 
            // Erase the star.  
 
            fVisible = FALSE; 
            return DefWindowProc(hwnd, message, wParam, lParam); 
 
        case WM_PAINT: 
 
            // Show the star if it is not visible. Use BeginPaint  
            // to clear the update region.  
 
            BeginPaint(hwnd, &ps); 
            if (!fVisible) 
                fVisible = Polyline(hdc, aptStar, 6); 
            EndPaint(hwnd, &ps); 
            return 0L; 
    } 
    return DefWindowProc(hwnd, message, wParam, lParam); 
} 
```



Cette application utilise un contexte de périphérique privé pour réduire le temps nécessaire à la préparation du contexte de périphérique pour le dessin. La procédure de fenêtre récupère et initialise le contexte de périphérique privé lors du traitement du message [**WM \_ Create**](../winmsg/wm-create.md) , en définissant le mode d’opération Raster binaire pour permettre l’effacement de l’étoile et son dessin à l’aide du même appel à la fonction [**Polyline**](/windows/desktop/api/Wingdi/nf-wingdi-polyline) . La procédure de fenêtre définit également l’origine de la fenêtre d’affichage pour que l’étoile soit dessinée à l’aide du même ensemble de points, quelle que soit la position de l’étoile dans la zone cliente.

L’application utilise le message de [**\_ peinture WM**](wm-paint.md) pour dessiner l’étoile chaque fois que la fenêtre doit être mise à jour. La procédure de fenêtre dessine l’étoile uniquement si elle n’est pas visible. autrement dit, uniquement s’il a été effacé par le message [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) . La procédure de fenêtre intercepte le message **WM \_ ERASEBKGND** pour définir la variable *fVisible* , mais passe le message à [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) afin que le système puisse dessiner l’arrière-plan de la fenêtre.

L’application utilise le message de [**\_ taille WM**](../winmsg/wm-size.md) pour arrêter la minuterie lorsque la fenêtre est réduite et redémarrer la minuterie lors de la restauration de la fenêtre réduite. La procédure de fenêtre utilise également le message pour mettre à jour la position actuelle de l’étoile si la taille de la fenêtre a été réduite afin que l’étoile ne soit plus dans la zone cliente. L’application effectue le suivi de la position actuelle de l’étoile à l’aide de la structure spécifiée par rcCurrent, qui définit le rectangle englobant pour l’étoile. Conserver l’ensemble des angles du rectangle dans la zone client permet de conserver l’étoile dans la zone. La procédure de fenêtre Centre initialement l’étoile dans la zone cliente lors du traitement du message [**WM \_ Create**](../winmsg/wm-create.md) .

 

 
