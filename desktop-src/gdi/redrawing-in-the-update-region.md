---
description: Vous pouvez limiter la quantité de dessin de votre application pendant le traitement du \_ message de peinture WM en déterminant la taille et l’emplacement de la région de mise à jour.
ms.assetid: 3407014d-6427-45e9-8be4-b8037ca5438f
title: Redessiner dans la région de mise à jour
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4f90518db1a66b98fc7f4bd5961f2cfa581bb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991164"
---
# <a name="redrawing-in-the-update-region"></a><span data-ttu-id="b5f95-103">Redessiner dans la région de mise à jour</span><span class="sxs-lookup"><span data-stu-id="b5f95-103">Redrawing in the Update Region</span></span>

<span data-ttu-id="b5f95-104">Vous pouvez limiter la quantité de dessin de votre application pendant le traitement du message de [**\_ peinture WM**](wm-paint.md) en déterminant la taille et l’emplacement de la région de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="b5f95-104">You can limit the amount of drawing your application carries out when processing the [**WM\_PAINT**](wm-paint.md) message by determining the size and location of the update region.</span></span> <span data-ttu-id="b5f95-105">Étant donné que le système utilise la région de mise à jour lors de la création de la zone de découpage pour le contexte de périphérique d’affichage de la fenêtre, vous pouvez indirectement déterminer la région de mise à jour en examinant la zone de Découp</span><span class="sxs-lookup"><span data-stu-id="b5f95-105">Because the system uses the update region when creating the clipping region for the window's display device context, you can indirectly determine the update region by examining the clipping region.</span></span>

<span data-ttu-id="b5f95-106">Dans l’exemple suivant, la procédure de fenêtre dessine un triangle, un rectangle, un Pentagone et un hexagone, mais uniquement si la totalité ou une partie de chaque figure se trouve dans la région de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="b5f95-106">In the following example, the window procedure draws a triangle, a rectangle, a pentagon, and a hexagon, but only if all or a portion of each figure lies within the update region.</span></span> <span data-ttu-id="b5f95-107">La procédure de fenêtre utilise la fonction [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) et un rectangle 100 par 100 pour déterminer si une figure se trouve dans la zone de découpage (et par conséquent la région de mise à jour) pour le contexte de périphérique courant récupéré par [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint).</span><span class="sxs-lookup"><span data-stu-id="b5f95-107">The window procedure uses the [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) function and a 100-by-100 rectangle to determine whether a figure is within the clipping region (and therefore the update region) for the common device context retrieved by [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint).</span></span>


```C++
POINT aptTriangle[4]  = {50,2, 98,86,  2,86, 50,2}, 
      aptRectangle[5] = { 2,2, 98,2,  98,98,  2,98, 2,2}, 
      aptPentagon[6]  = {50,2, 98,35, 79,90, 21,90, 2,35, 50,2}, 
      aptHexagon[7]   = {50,2, 93,25, 93,75, 50,98, 7,75, 7,25, 50,2}; 
  . 
  . 
  . 
 
        case WM_PAINT: 
            hdc = BeginPaint(hwnd, &ps); 
            SetRect(&rc, 0, 0, 100, 100); 
 
            if (RectVisible(hdc, &rc)) 
                Polyline(hdc, aptTriangle, 4); 
 
            SetViewportOrgEx(hdc, 100, 0, NULL); 
            if (RectVisible(hdc, &rc)) 
                Polyline(hdc, aptRectangle, 5); 
 
            SetViewportOrgEx(hdc, 0, 100, NULL); 
            if (RectVisible(hdc, &rc)) 
                Polyline(hdc, aptPentagon, 6); 
 
            SetViewportOrgEx(hdc, 100, 100, NULL); 
            if (RectVisible(hdc, &rc)) 
                Polyline(hdc, aptHexagon, 7); 
            EndPaint(hwnd, &ps); 
            return 0L; 
 
  . 
  . 
  . 
```



<span data-ttu-id="b5f95-108">Les coordonnées de chaque figure dans cet exemple se trouvent dans le même rectangle 100-par-100.</span><span class="sxs-lookup"><span data-stu-id="b5f95-108">The coordinates of each figure in this example lie within the same 100-by-100 rectangle.</span></span> <span data-ttu-id="b5f95-109">Avant de dessiner une figure, la procédure de fenêtre définit l’origine de la fenêtre d’affichage sur une autre partie de la zone cliente à l’aide de la fonction [**SetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportorgex) .</span><span class="sxs-lookup"><span data-stu-id="b5f95-109">Before drawing a figure, the window procedure sets the viewport origin to a different part of the client area by using the [**SetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportorgex) function.</span></span> <span data-ttu-id="b5f95-110">Cela empêche les figures d’être dessinées les unes au-dessus des autres.</span><span class="sxs-lookup"><span data-stu-id="b5f95-110">This prevents figures from being drawn one on top of the other.</span></span> <span data-ttu-id="b5f95-111">La modification de l’origine de la fenêtre d’affichage n’affecte pas la zone de découpage, mais affecte la façon dont les coordonnées du rectangle passé à [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) sont interprétées.</span><span class="sxs-lookup"><span data-stu-id="b5f95-111">Changing the viewport origin does not affect the clipping region, but does affect how the coordinates of the rectangle passed to [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) are interpreted.</span></span> <span data-ttu-id="b5f95-112">La modification de l’origine vous permet également d’utiliser un seul rectangle pour vérifier la région de mise à jour plutôt que des rectangles individuels pour chaque figure.</span><span class="sxs-lookup"><span data-stu-id="b5f95-112">Changing the origin also allows you to use a single rectangle to check the update region rather than individual rectangles for each figure.</span></span>

 

 



