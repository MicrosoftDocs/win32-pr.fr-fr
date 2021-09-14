---
description: Vous pouvez dessiner votre propre arrière-plan de fenêtre au lieu de le dessiner pour vous.
ms.assetid: 72a342dc-2766-4ec9-b4c6-5ac3c550ea25
title: Dessin d’un arrière-plan de fenêtre personnalisé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 437a88bec680a6f35e84f5444fc90a45f98da533
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127415952"
---
# <a name="drawing-a-custom-window-background"></a>Dessin d’un arrière-plan de fenêtre personnalisé

Vous pouvez dessiner votre propre arrière-plan de fenêtre au lieu de le dessiner pour vous. La plupart des applications spécifient une valeur de handle de pinceau ou de couleur système pour le pinceau d’arrière-plan de classe lors de l’inscription de la classe de fenêtre ; le système utilise le pinceau ou la couleur pour dessiner l’arrière-plan. Toutefois, si vous définissez le pinceau d’arrière-plan de la classe sur **null**, le système envoie un message [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) à votre procédure de fenêtre chaque fois que l’arrière-plan de la fenêtre doit être dessiné, ce qui vous permet de dessiner un arrière-plan personnalisé.

Dans l’exemple suivant, la procédure de fenêtre dessine un grand modèle de damier qui s’ajuste bien à la fenêtre. La procédure remplit la zone cliente avec un pinceau blanc, puis dessine des rectangles de 13 20 par 20 à l’aide d’un pinceau gris. Le contexte de périphérique d’affichage à utiliser lors du dessin de l’arrière-plan est spécifié dans le paramètre *wParam* du message.


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



Si l’application dessine sa propre fenêtre réduite, le système envoie également le message [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) à la procédure de fenêtre pour dessiner l’arrière-plan de la fenêtre réduite. Vous pouvez utiliser la même technique que celle utilisée par [**WM \_ Paint**](wm-paint.md) pour déterminer si la fenêtre est réduite, appeler la fonction [**IsIconic**](/windows/win32/api/winuser/nf-winuser-isiconic) et vérifier si la valeur de retour est **true**.

 

 
