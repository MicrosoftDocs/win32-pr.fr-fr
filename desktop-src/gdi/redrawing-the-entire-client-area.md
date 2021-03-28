---
description: Vous pouvez faire en sorte que votre application redessine le contenu entier de la zone cliente chaque fois que la fenêtre change de taille, en définissant les \_ styles CS HREDRAW et CS \_ VREDRAW pour la classe de fenêtre.
ms.assetid: ed68b85e-8382-4450-b07d-0422b44dc2e3
title: Redessin de la zone cliente entière
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d67640d1b464173755029bef1d0feb91f215cda6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991161"
---
# <a name="redrawing-the-entire-client-area"></a><span data-ttu-id="fe34b-103">Redessin de la zone cliente entière</span><span class="sxs-lookup"><span data-stu-id="fe34b-103">Redrawing the Entire Client Area</span></span>

<span data-ttu-id="fe34b-104">Vous pouvez faire en sorte que votre application redessine le contenu entier de la zone cliente chaque fois que la fenêtre change de taille, en définissant les \_ styles CS HREDRAW et CS \_ VREDRAW pour la classe de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="fe34b-104">You can have your application redraw the entire contents of the client area whenever the window changes size by setting the CS\_HREDRAW and CS\_VREDRAW styles for the window class.</span></span> <span data-ttu-id="fe34b-105">Les applications qui ajustent la taille du dessin en fonction de la taille de la fenêtre utilisent ces styles pour s’assurer qu’ils commencent avec une zone client complètement vide lors du dessin.</span><span class="sxs-lookup"><span data-stu-id="fe34b-105">Applications that adjust the size of the drawing based on the size of the window use these styles to ensure that they start with a completely empty client area when drawing.</span></span>

<span data-ttu-id="fe34b-106">Dans l’exemple suivant, la procédure de fenêtre dessine une étoile à cinq branches qui s’intègre parfaitement dans la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="fe34b-106">In the following example, the window procedure draws a five-pointed star that fits neatly in the client area.</span></span> <span data-ttu-id="fe34b-107">Il utilise un contexte de périphérique courant et doit définir le mode de mappage ainsi que les extensions de fenêtre et de fenêtre d’affichage chaque fois que le message de [**\_ peinture WM**](wm-paint.md) est traité.</span><span class="sxs-lookup"><span data-stu-id="fe34b-107">It uses a common device context and must set the mapping mode as well as window and viewport extents each time the [**WM\_PAINT**](wm-paint.md) message is processed.</span></span>


```C++
LRESULT APIENTRY WndProc(HWMD hwnd, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    PAINTSTRUCT ps; 
    HDC hdc; 
    RECT rc; 
    POINT aptStar[6] = {50,2, 2,98, 98,33, 2,33, 98,98, 50,2}; 
 
    . 
    . 
    . 
 
        case WM_PAINT: 
            hdc = BeginPaint(hwnd, &ps); 
            GetClientRect(hwnd, &rc); 
            SetMapMode(hdc, MM_ANISOTROPIC); 
            SetWindowExtEx(hdc, 100, 100, NULL); 
            SetViewportExtEx(hdc, rc.right, rc.bottom, NULL); 
            Polyline(hdc, aptStar, 6); 
            EndPaint(hwnd, &ps); 
            return 0L; 
 
        . 
        . 
        . 
} 
 
 
int APIENTRY WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow) 
{ 
    WNDCLASS wc; 
 
    . 
    . 
    . 
 
        wc.style = CS_HREDRAW | CS_VREDRAW; 
        wc.lpfnWndProc = (WNDPROC) WndProc; 
 
    . 
    . 
    . 
 
        RegisterClass(&wc); 
 
    . 
    . 
    . 
 
    return msg.wParam; 
} 
```



 

 



