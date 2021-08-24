---
description: Vous pouvez dessiner vos propres fenêtres réduites plutôt que de les dessiner pour vous.
ms.assetid: 607d987a-5bdc-46bc-bde7-6dc52745ac79
title: Dessin d’une fenêtre réduite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24ca955d3ff9f17b7f01e504b9e60c15200eb2b8191a5b4dba0e622956567f98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119360629"
---
# <a name="drawing-a-minimized-window"></a>Dessin d’une fenêtre réduite

Vous pouvez dessiner vos propres fenêtres réduites plutôt que de les dessiner pour vous. La plupart des applications définissent une icône de classe lors de l’inscription de la classe de fenêtre pour la fenêtre et le système dessine l’icône lorsque la fenêtre est réduite. Toutefois, si vous définissez l’icône de classe sur **null**, le système envoie un message [**WM \_ Paint**](wm-paint.md) à votre procédure de fenêtre chaque fois que la fenêtre est réduite, ce qui permet à la procédure de fenêtre de dessiner dans la fenêtre réduite.

Dans l’exemple suivant, la procédure de fenêtre dessine une étoile dans la fenêtre réduite. La procédure utilise la fonction [**IsIconic**](/windows/win32/api/winuser/nf-winuser-isiconic) pour déterminer quand la fenêtre est réduite. Cela permet de s’assurer que l’étoile est dessinée uniquement lorsque la fenêtre est réduite.


```C++
POINT aptStar[6] = {50,2, 2,98, 98,33, 2,33, 98,98, 50,2}; 
 
  . 
  . 
  . 
 
case WM_PAINT: 
    hdc = BeginPaint(hwnd, &ps); 
 
    // Determine whether the window is minimized.  
 
    if (IsIconic(hwnd)) 
    { 
        GetClientRect(hwnd, &rc); 
        SetMapMode(hdc, MM_ANISOTROPIC); 
        SetWindowExtEx(hdc, 100, 100, NULL); 
        SetViewportExtEx(hdc, rc.right, rc.bottom, NULL); 
        Polyline(hdc, aptStar, 6); 
    } 
    else 
    { 
        TextOut(hdc, 0,0, "Hello, Windows!", 15); 
    } 
    EndPaint(hwnd, &ps); 
    return 0L; 
```



Vous définissez l’icône de classe sur **null** en affectant la **valeur null** au membre **HICON** de la structure [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) avant d’appeler la fonction [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) pour la classe Window.

 

 
