---
description: Vous pouvez dessiner votre propre arrière-plan de fenêtre au lieu de le dessiner pour vous.
ms.assetid: 72a342dc-2766-4ec9-b4c6-5ac3c550ea25
title: Dessin d’un arrière-plan de fenêtre personnalisé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 437a88bec680a6f35e84f5444fc90a45f98da533
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972698"
---
# <a name="drawing-a-custom-window-background"></a><span data-ttu-id="c71cc-103">Dessin d’un arrière-plan de fenêtre personnalisé</span><span class="sxs-lookup"><span data-stu-id="c71cc-103">Drawing a Custom Window Background</span></span>

<span data-ttu-id="c71cc-104">Vous pouvez dessiner votre propre arrière-plan de fenêtre au lieu de le dessiner pour vous.</span><span class="sxs-lookup"><span data-stu-id="c71cc-104">You can draw your own window background rather than having the system draw it for you.</span></span> <span data-ttu-id="c71cc-105">La plupart des applications spécifient une valeur de handle de pinceau ou de couleur système pour le pinceau d’arrière-plan de classe lors de l’inscription de la classe de fenêtre ; le système utilise le pinceau ou la couleur pour dessiner l’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="c71cc-105">Most applications specify a brush handle or system color value for the class background brush when registering the window class; the system uses the brush or color to draw the background.</span></span> <span data-ttu-id="c71cc-106">Toutefois, si vous définissez le pinceau d’arrière-plan de la classe sur **null**, le système envoie un message [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) à votre procédure de fenêtre chaque fois que l’arrière-plan de la fenêtre doit être dessiné, ce qui vous permet de dessiner un arrière-plan personnalisé.</span><span class="sxs-lookup"><span data-stu-id="c71cc-106">If you set the class background brush to **NULL**, however, the system sends a [**WM\_ERASEBKGND**](../winmsg/wm-erasebkgnd.md) message to your window procedure whenever the window background must be drawn, letting you draw a custom background.</span></span>

<span data-ttu-id="c71cc-107">Dans l’exemple suivant, la procédure de fenêtre dessine un grand modèle de damier qui s’ajuste bien à la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c71cc-107">In the following example, the window procedure draws a large checkerboard pattern that fits neatly in the window.</span></span> <span data-ttu-id="c71cc-108">La procédure remplit la zone cliente avec un pinceau blanc, puis dessine des rectangles de 13 20 par 20 à l’aide d’un pinceau gris.</span><span class="sxs-lookup"><span data-stu-id="c71cc-108">The procedure fills the client area with a white brush and then draws thirteen 20-by-20 rectangles using a gray brush.</span></span> <span data-ttu-id="c71cc-109">Le contexte de périphérique d’affichage à utiliser lors du dessin de l’arrière-plan est spécifié dans le paramètre *wParam* du message.</span><span class="sxs-lookup"><span data-stu-id="c71cc-109">The display device context to use when drawing the background is specified in the *wParam* parameter for the message.</span></span>


```C++
HBRUSH hbrWhite, hbrGray; 
 
  . 
  . 
  . 
 
case WM_CREATE: 
    hbrWhite = GetStockObject(WHITE_BRUSH); 
    hbrGray  = GetStockObject(GRAY_BRUSH); 
    return 0L; 
 
case WM_ERASEBKGND: 
    hdc = (HDC) wParam; 
    GetClientRect(hwnd, &rc); 
    SetMapMode(hdc, MM_ANISOTROPIC); 
    SetWindowExtEx(hdc, 100, 100, NULL); 
    SetViewportExtEx(hdc, rc.right, rc.bottom, NULL); 
    FillRect(hdc, &rc, hbrWhite); 
 
    for (i = 0; i < 13; i++) 
    { 
        x = (i * 40) % 100; 
        y = ((i * 40) / 100) * 20; 
        SetRect(&rc, x, y, x + 20, y + 20); 
        FillRect(hdc, &rc, hbrGray); 
    } 
  return 1L; 
```



<span data-ttu-id="c71cc-110">Si l’application dessine sa propre fenêtre réduite, le système envoie également le message [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) à la procédure de fenêtre pour dessiner l’arrière-plan de la fenêtre réduite.</span><span class="sxs-lookup"><span data-stu-id="c71cc-110">If the application draws its own minimized window, the system also sends the [**WM\_ERASEBKGND**](../winmsg/wm-erasebkgnd.md) message to the window procedure to draw the background for the minimized window.</span></span> <span data-ttu-id="c71cc-111">Vous pouvez utiliser la même technique que celle utilisée par [**WM \_ Paint**](wm-paint.md) pour déterminer si la fenêtre est réduite, appeler la fonction [**IsIconic**](/windows/win32/api/winuser/nf-winuser-isiconic) et vérifier si la valeur de retour est **true**.</span><span class="sxs-lookup"><span data-stu-id="c71cc-111">You can use the same technique used by [**WM\_PAINT**](wm-paint.md) to determine whether the window is minimized that is, call the [**IsIconic**](/windows/win32/api/winuser/nf-winuser-isiconic) function and check for the return value **TRUE**.</span></span>

 

 
