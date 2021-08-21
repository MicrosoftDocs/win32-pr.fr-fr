---
description: Vous pouvez faire en sorte que votre application redessine le contenu entier de la zone cliente chaque fois que la fenêtre change de taille, en définissant les \_ styles CS HREDRAW et CS \_ VREDRAW pour la classe de fenêtre.
ms.assetid: ed68b85e-8382-4450-b07d-0422b44dc2e3
title: Redessin de la zone cliente entière
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e3c438fe36160f27b1015daf7874e237035f927825199b93b3a508668f40bd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118759145"
---
# <a name="redrawing-the-entire-client-area"></a>Redessin de la zone cliente entière

Vous pouvez faire en sorte que votre application redessine le contenu entier de la zone cliente chaque fois que la fenêtre change de taille, en définissant les \_ styles CS HREDRAW et CS \_ VREDRAW pour la classe de fenêtre. Les applications qui ajustent la taille du dessin en fonction de la taille de la fenêtre utilisent ces styles pour s’assurer qu’ils commencent avec une zone client complètement vide lors du dessin.

Dans l’exemple suivant, la procédure de fenêtre dessine une étoile à cinq branches qui s’intègre parfaitement dans la zone cliente. Il utilise un contexte de périphérique courant et doit définir le mode de mappage ainsi que les extensions de fenêtre et de fenêtre d’affichage chaque fois que le message de [**\_ peinture WM**](wm-paint.md) est traité.


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



 

 



