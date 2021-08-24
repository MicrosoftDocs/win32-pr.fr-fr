---
description: Vous utilisez les fonctions BeginPaint et EndPaint pour préparer et terminer le dessin dans la zone cliente.
ms.assetid: ed995bfd-a791-4d73-9a0b-daf65a9f7709
title: Dessin dans la zone cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5d01331ae60a7814602f6c10c0d9109ae665da39aa140223e31ac03303048b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832019"
---
# <a name="drawing-in-the-client-area"></a>Dessin dans la zone cliente

Vous utilisez les fonctions [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) et [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) pour préparer et terminer le dessin dans la zone cliente. **BeginPaint** retourne un handle vers le contexte de périphérique d’affichage utilisé pour le dessin dans la zone cliente. **EndPaint** termine la demande de peinture et libère le contexte de périphérique.

Dans l’exemple suivant, la procédure de fenêtre écrit le message « Hello, Windows ! » dans la zone cliente. Pour vous assurer que la chaîne est visible lors de la création de la fenêtre, la fonction [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) appelle [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) immédiatement après la création et l’affichage de la fenêtre. Cela entraîne l’envoi immédiat d’un message de [**\_ peinture WM**](wm-paint.md) à la procédure de fenêtre.


```C++
LRESULT APIENTRY WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    PAINTSTRUCT ps; 
    HDC hdc; 
 
    switch (message) 
    { 
        case WM_PAINT: 
            hdc = BeginPaint(hwnd, &ps); 
            TextOut(hdc, 0, 0, "Hello, Windows!", 15); 
            EndPaint(hwnd, &ps); 
            return 0L; 

        // Process other messages.   
    } 
} 
 
int APIENTRY WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow) 
{ 
    HWND hwnd; 
 
    hwnd = CreateWindowEx( 
        // parameters  
        ); 
 
    ShowWindow(hwnd, SW_SHOW); 
    UpdateWindow(hwnd); 
 
    return msg.wParam; 
} 
```



 

 
