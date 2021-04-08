---
title: Suppression d’un contexte de rendu
description: L’exemple de code suivant montre comment supprimer un contexte de rendu OpenGL lorsqu’une fenêtre OpenGL est fermée. Il s’agit d’une continuation du scénario utilisé pour créer un contexte de rendu et le mettre à jour.
ms.assetid: 562c4698-f5bb-418a-8479-0df07e9834e5
keywords:
- OpenGL sur Windows, contextes de rendu
- contextes de rendu OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 621abd0de46c874f40568f8361191b25df329f0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839073"
---
# <a name="deleting-a-rendering-context"></a><span data-ttu-id="fe70c-106">Suppression d’un contexte de rendu</span><span class="sxs-lookup"><span data-stu-id="fe70c-106">Deleting a Rendering Context</span></span>

<span data-ttu-id="fe70c-107">L’exemple de code suivant montre comment supprimer un contexte de rendu OpenGL lorsqu’une fenêtre OpenGL est fermée.</span><span class="sxs-lookup"><span data-stu-id="fe70c-107">The following code sample shows how to delete an OpenGL rendering context when an OpenGL window is closed.</span></span> <span data-ttu-id="fe70c-108">Il s’agit d’une continuation du scénario utilisé pour [créer un contexte de rendu et le mettre à jour](creating-a-rendering-context-and-making-it-current.md).</span><span class="sxs-lookup"><span data-stu-id="fe70c-108">It is a continuation of the scenario used in [Creating a Rendering Context and Making It Current](creating-a-rendering-context-and-making-it-current.md).</span></span>


```C++
// a window is about to be destroyed  
case WM_DESTROY: 
    { 
    // local variables  
    HGLRC    hglrc; 
    HDC      hdc ; 
 
    // if the thread has a current rendering context ...  
    if(hglrc = wglGetCurrentContext()) { 
 
        // obtain its associated device context  
        hdc = wglGetCurrentDC() ; 
 
        // make the rendering context not current  
        wglMakeCurrent(NULL, NULL) ; 
 
        // release the device context  
        ReleaseDC (hwnd, hdc) ; 
 
        // delete the rendering context  
        wglDeleteContext(hglrc); 
 
        }
```



 

 




