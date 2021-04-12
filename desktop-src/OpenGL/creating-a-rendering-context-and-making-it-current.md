---
title: Création d’un contexte de rendu et mise à jour
description: L’exemple de code suivant montre comment créer un contexte de rendu OpenGL en réponse à un \_ message WM Create.
ms.assetid: eacf0475-6845-48f9-b016-7f0150679419
keywords:
- OpenGL sur Windows, contextes de rendu
- contextes de rendu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7bcb8eb5a3892aac977f465894808adc19809a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310622"
---
# <a name="creating-a-rendering-context-and-making-it-current"></a><span data-ttu-id="85e68-105">Création d’un contexte de rendu et mise à jour</span><span class="sxs-lookup"><span data-stu-id="85e68-105">Creating a Rendering Context and Making It Current</span></span>

<span data-ttu-id="85e68-106">L’exemple de code suivant montre comment créer un contexte de rendu OpenGL en réponse à un \_ message WM Create.</span><span class="sxs-lookup"><span data-stu-id="85e68-106">The following code sample shows how to create an OpenGL rendering context in response to a WM\_CREATE message.</span></span> <span data-ttu-id="85e68-107">Notez que vous configurez le format de pixel avant de créer le contexte de rendu.</span><span class="sxs-lookup"><span data-stu-id="85e68-107">Notice that you set up the pixel format before creating the rendering context.</span></span> <span data-ttu-id="85e68-108">Notez également que dans ce scénario, le contexte de périphérique n’est pas libéré localement ; vous le Libérez lorsque la fenêtre est fermée, après avoir rendu le contexte de rendu non actuel.</span><span class="sxs-lookup"><span data-stu-id="85e68-108">Also notice that in this scenario the device context is not released locally; you release it when the window is closed, after making the rendering context not current.</span></span> <span data-ttu-id="85e68-109">Pour plus d’informations, consultez [Suppression d’un contexte de rendu](deleting-a-rendering-context.md).</span><span class="sxs-lookup"><span data-stu-id="85e68-109">For more information, see [Deleting a Rendering Context](deleting-a-rendering-context.md).</span></span> <span data-ttu-id="85e68-110">Enfin, Notez que vous pouvez utiliser des variables locales pour le contexte de périphérique et les handles de contexte de rendu, car avec les fonctions [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext) et [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc) , vous pouvez obtenir des handles pour ces contextes si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="85e68-110">Finally, notice that you can use local variables for the device context and rendering context handles, because with the [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext) and [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc) functions you can obtain handles to those contexts as needed.</span></span>

``` syntax
// a window has been created, but is not yet visible  
case WM_CREATE: 
    { 
    // local variables  
    HDC      hdc ; 
    HGLRC    hglrc ; 
 
    // obtain a device context for the window  
    hdc = GetDC(hWnd); 
     
    // set an appropriate pixel format   
    myPixelFormatSetupFunction(hdc); 
 
    // if we can create a rendering context ...   
    if (hglrc = wglCreateContext( hdc ) ) { 
 
        // try to make it the thread's current rendering context  
        bHaveCurrentRC = wglMakeCurrent(hdc, hglrc) ; 
 
        } 
 
    // perform miscellaneous other WM_CREATE chores ...  
 
    }  
    break;
```

 

 




