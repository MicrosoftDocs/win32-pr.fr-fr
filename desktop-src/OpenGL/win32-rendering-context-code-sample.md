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
ms.openlocfilehash: 9693b140083210ce0865b18463f4595c2f1fc731c8fc1d837f61342ede50b9d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117794692"
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



 

 




