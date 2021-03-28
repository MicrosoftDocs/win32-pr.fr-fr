---
description: Le système n’est pas la seule source de \_ messages de peinture WM. La fonction InvalidateRect ou InvalidateRgn peut générer indirectement \_ des messages de peinture WM pour votre Windows. Ces fonctions marquent la totalité ou une partie d’une zone client comme non valide (qui doit être redessinée).
ms.assetid: 41c2bc07-768b-4d27-a869-69b072f3e033
title: Invalidation de la zone cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76fb02be44f600b80f87ec8f05c022fa3c35d827
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991204"
---
# <a name="invalidating-the-client-area"></a><span data-ttu-id="ba617-105">Invalidation de la zone cliente</span><span class="sxs-lookup"><span data-stu-id="ba617-105">Invalidating the Client Area</span></span>

<span data-ttu-id="ba617-106">Le système n’est pas la seule source de messages de [**\_ peinture WM**](wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="ba617-106">The system is not the only source of [**WM\_PAINT**](wm-paint.md) messages.</span></span> <span data-ttu-id="ba617-107">La fonction [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) ou [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) peut générer indirectement des messages de **\_ peinture WM** pour votre Windows.</span><span class="sxs-lookup"><span data-stu-id="ba617-107">The [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) or [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) function can indirectly generate **WM\_PAINT** messages for your windows.</span></span> <span data-ttu-id="ba617-108">Ces fonctions marquent la totalité ou une partie d’une zone client comme non valide (qui doit être redessinée).</span><span class="sxs-lookup"><span data-stu-id="ba617-108">These functions mark all or part of a client area as invalid (that must be redrawn).</span></span>

<span data-ttu-id="ba617-109">Dans l’exemple suivant, la procédure de fenêtre invalide l’intégralité de la zone cliente lors du traitement des messages [**WM \_ char**](../inputdev/wm-char.md) .</span><span class="sxs-lookup"><span data-stu-id="ba617-109">In the following example, the window procedure invalidates the entire client area when processing [**WM\_CHAR**](../inputdev/wm-char.md) messages.</span></span> <span data-ttu-id="ba617-110">Cela permet à l’utilisateur de modifier la figure en tapant un nombre et en vue d’afficher les résultats. Ces résultats sont dessinés dès qu’aucun autre message n’est présent dans la file d’attente des messages de l’application.</span><span class="sxs-lookup"><span data-stu-id="ba617-110">This allows the user to change the figure by typing a number and view the results; these results are drawn as soon as there are no other messages in the application's message queue.</span></span>


```C++
RECT rc;
POINT aptPentagon[6] = {50,2, 98,35, 79,90, 21,90, 2,35, 50,2}, 
      aptHexagon[7]  = {50,2, 93,25, 93,75, 50,98, 7,75, 7,25, 50,2}; 
POINT *ppt = aptPentagon; 
int cpt = 6; 
 
  . 
  . 
  . 
 
case WM_CHAR: 
    switch (wParam) 
    { 
        case '5': 
            ppt = aptPentagon; 
            cpt = 6; 
            break; 
        case '6': 
            ppt = aptHexagon; 
            cpt = 7; 
            break; 
    } 
    InvalidateRect(hwnd, NULL, TRUE); 
    return 0L; 
 
case WM_PAINT: 
    hdc = BeginPaint(hwnd, &ps); 
    GetClientRect(hwnd, &rc); 
    SetMapMode(hdc, MM_ANISOTROPIC); 
    SetWindowExtEx(hdc, 100, 100, NULL); 
    SetViewportExtEx(hdc, rc.right, rc.bottom, NULL); 
    Polyline(hdc, ppt, cpt); 
    EndPaint(hwnd, &ps); 
    return 0L; 
```



<span data-ttu-id="ba617-111">Dans cet exemple, l’argument **null** utilisé par [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) spécifie l’intégralité de la zone cliente ; l’argument **true** entraîne l’effacement de l’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="ba617-111">In this example, the **NULL** argument used by [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) specifies the entire client area; the **TRUE** argument causes the background to be erased.</span></span> <span data-ttu-id="ba617-112">Si vous ne souhaitez pas que l’application attende que la file d’attente de messages de l’application n’ait pas d’autres messages, utilisez la fonction [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) pour forcer l’envoi immédiat du message de [**\_ peinture WM**](wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="ba617-112">If you do not want the application to wait until the application's message queue has no other messages, use the [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) function to force the [**WM\_PAINT**](wm-paint.md) message to be sent immediately.</span></span> <span data-ttu-id="ba617-113">Si une partie de la zone cliente n’est pas valide, **UpdateWindow** envoie le message de **\_ peinture WM** pour la fenêtre spécifiée directement à la procédure de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="ba617-113">If there is any invalid part of the client area, **UpdateWindow** sends the **WM\_PAINT** message for the specified window directly to the window procedure.</span></span>

 

 
