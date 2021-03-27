---
description: Vous utilisez les fonctions BeginPaint et EndPaint pour préparer et terminer le dessin dans la zone cliente.
ms.assetid: ed995bfd-a791-4d73-9a0b-daf65a9f7709
title: Dessin dans la zone cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1e14c8492a11a7ad9764416b2453cea3264fbf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863653"
---
# <a name="drawing-in-the-client-area"></a><span data-ttu-id="19777-103">Dessin dans la zone cliente</span><span class="sxs-lookup"><span data-stu-id="19777-103">Drawing in the Client Area</span></span>

<span data-ttu-id="19777-104">Vous utilisez les fonctions [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) et [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) pour préparer et terminer le dessin dans la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="19777-104">You use the [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) and [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) functions to prepare for and complete the drawing in the client area.</span></span> <span data-ttu-id="19777-105">**BeginPaint** retourne un handle vers le contexte de périphérique d’affichage utilisé pour le dessin dans la zone cliente. **EndPaint** termine la demande de peinture et libère le contexte de périphérique.</span><span class="sxs-lookup"><span data-stu-id="19777-105">**BeginPaint** returns a handle to the display device context used for drawing in the client area; **EndPaint** ends the paint request and releases the device context.</span></span>

<span data-ttu-id="19777-106">Dans l’exemple suivant, la procédure de fenêtre écrit le message « Hello, Windows ! »</span><span class="sxs-lookup"><span data-stu-id="19777-106">In the following example, the window procedure writes the message "Hello, Windows!"</span></span> <span data-ttu-id="19777-107">dans la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="19777-107">in the client area.</span></span> <span data-ttu-id="19777-108">Pour vous assurer que la chaîne est visible lors de la création de la fenêtre, la fonction [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) appelle [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) immédiatement après la création et l’affichage de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="19777-108">To make sure the string is visible when the window is first created, the [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) function calls [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) immediately after creating and showing the window.</span></span> <span data-ttu-id="19777-109">Cela entraîne l’envoi immédiat d’un message de [**\_ peinture WM**](wm-paint.md) à la procédure de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="19777-109">This causes a [**WM\_PAINT**](wm-paint.md) message to be sent immediately to the window procedure.</span></span>


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



 

 
