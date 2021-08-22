---
description: Le système n’est pas la seule source de \_ messages de peinture WM. La fonction InvalidateRect ou InvalidateRgn peut générer indirectement \_ des messages de peinture WM pour votre Windows. Ces fonctions marquent la totalité ou une partie d’une zone client comme non valide (qui doit être redessinée).
ms.assetid: 41c2bc07-768b-4d27-a869-69b072f3e033
title: Invalidation de la zone cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d94a3a5b4e6903c549331788f9e81947dca44e7a699bb1a633bce46525585b2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558659"
---
# <a name="invalidating-the-client-area"></a>Invalidation de la zone cliente

Le système n’est pas la seule source de messages de [**\_ peinture WM**](wm-paint.md) . La fonction [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) ou [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) peut générer indirectement des messages de **\_ peinture WM** pour votre Windows. Ces fonctions marquent la totalité ou une partie d’une zone client comme non valide (qui doit être redessinée).

Dans l’exemple suivant, la procédure de fenêtre invalide l’intégralité de la zone cliente lors du traitement des messages [**WM \_ char**](../inputdev/wm-char.md) . Cela permet à l’utilisateur de modifier la figure en tapant un nombre et en vue d’afficher les résultats. Ces résultats sont dessinés dès qu’aucun autre message n’est présent dans la file d’attente des messages de l’application.


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



Dans cet exemple, l’argument **null** utilisé par [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) spécifie l’intégralité de la zone cliente ; l’argument **true** entraîne l’effacement de l’arrière-plan. Si vous ne souhaitez pas que l’application attende que la file d’attente de messages de l’application n’ait pas d’autres messages, utilisez la fonction [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) pour forcer l’envoi immédiat du message de [**\_ peinture WM**](wm-paint.md) . Si une partie de la zone cliente n’est pas valide, **UpdateWindow** envoie le message de **\_ peinture WM** pour la fenêtre spécifiée directement à la procédure de fenêtre.

 

 
