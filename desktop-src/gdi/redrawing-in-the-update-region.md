---
description: Vous pouvez limiter la quantité de dessin de votre application pendant le traitement du \_ message de peinture WM en déterminant la taille et l’emplacement de la région de mise à jour.
ms.assetid: 3407014d-6427-45e9-8be4-b8037ca5438f
title: Redessiner dans la région de mise à jour
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4f90518db1a66b98fc7f4bd5961f2cfa581bb6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403509"
---
# <a name="redrawing-in-the-update-region"></a>Redessiner dans la région de mise à jour

Vous pouvez limiter la quantité de dessin de votre application pendant le traitement du message de [**\_ peinture WM**](wm-paint.md) en déterminant la taille et l’emplacement de la région de mise à jour. Étant donné que le système utilise la région de mise à jour lors de la création de la zone de découpage pour le contexte de périphérique d’affichage de la fenêtre, vous pouvez indirectement déterminer la région de mise à jour en examinant la zone de Découp

Dans l’exemple suivant, la procédure de fenêtre dessine un triangle, un rectangle, un Pentagone et un hexagone, mais uniquement si la totalité ou une partie de chaque figure se trouve dans la région de mise à jour. La procédure de fenêtre utilise la fonction [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) et un rectangle 100 par 100 pour déterminer si une figure se trouve dans la zone de découpage (et par conséquent la région de mise à jour) pour le contexte de périphérique courant récupéré par [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint).


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



Les coordonnées de chaque figure dans cet exemple se trouvent dans le même rectangle 100-par-100. Avant de dessiner une figure, la procédure de fenêtre définit l’origine de la fenêtre d’affichage sur une autre partie de la zone cliente à l’aide de la fonction [**SetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportorgex) . Cela empêche les figures d’être dessinées les unes au-dessus des autres. La modification de l’origine de la fenêtre d’affichage n’affecte pas la zone de découpage, mais affecte la façon dont les coordonnées du rectangle passé à [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) sont interprétées. La modification de l’origine vous permet également d’utiliser un seul rectangle pour vérifier la région de mise à jour plutôt que des rectangles individuels pour chaque figure.

 

 



