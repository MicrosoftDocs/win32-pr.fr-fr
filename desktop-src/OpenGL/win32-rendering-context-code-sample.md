---
title: Windows Exemple de code de contexte de rendu
description: L’exemple de code suivant montre comment le code de contexte de rendu GLX dans la section précédente se présente lorsqu’il a été porté à Windows.
ms.assetid: 12992faa-eb64-4a21-8015-3c73c2914189
keywords:
- contextes de rendu
- portage vers OpenGL, contextes de rendu
- Portage OpenGL, contextes de rendu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca0423f7458538f903a339f2f82dbff1c86c0626
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013965"
---
# <a name="windows-rendering-context-code-sample"></a>Windows Exemple de code de contexte de rendu

L’exemple de code suivant montre comment le code de contexte de rendu GLX dans la section précédente se présente lorsqu’il a été porté à Windows.


```C++
HGLRC hRC;           // rendering context variable  
 
/* Create and initialize a window */ 
        
/* Window message switch in a window procedure */ 
case WM_CREATE:      // Message when window is created  
{ 
    HDC hDC, hDCTemp;    // device context handles   
 
    /* Get the handle of the windows device context. */ 
    hDC = GetDC(hWnd); 
 
    /* Create a rendering context and make it the current context */  
    hRC = wglCreateContext(hDC); 
    if (!hRC)  
    { 
        MessageBox(NULL, "Cannot create context.", "Error", MB_OK); 
        return FALSE; 
    }  
    wglMakeCurrent(hDC, hRC); 
} 
break; 
        
        .    
case WM_DESTROYED:   // Message when window is destroyed  
{ 
    HGLRC hRC        // rendering context handle  
    HDC   hDC;       // device context handle  
 
    /* Release and free the device context and rendering context. */ 
    hDC = wglGetCurrentDC; 
    hRC = wglGetCurrentContext; 
 
    wglMakeCurrent(NULL, NULL); 
 
    if (hRC) 
        wglDeleteContext(hRC); 
 
    if (hDC) 
        ReleaseDC(hWnd, hDC); 
 
    PostQuitMessage (0); 
} 
break;
```



 

 




