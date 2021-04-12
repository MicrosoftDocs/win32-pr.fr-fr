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
# <a name="creating-a-rendering-context-and-making-it-current"></a>Création d’un contexte de rendu et mise à jour

L’exemple de code suivant montre comment créer un contexte de rendu OpenGL en réponse à un \_ message WM Create. Notez que vous configurez le format de pixel avant de créer le contexte de rendu. Notez également que dans ce scénario, le contexte de périphérique n’est pas libéré localement ; vous le Libérez lorsque la fenêtre est fermée, après avoir rendu le contexte de rendu non actuel. Pour plus d’informations, consultez [Suppression d’un contexte de rendu](deleting-a-rendering-context.md). Enfin, Notez que vous pouvez utiliser des variables locales pour le contexte de périphérique et les handles de contexte de rendu, car avec les fonctions [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext) et [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc) , vous pouvez obtenir des handles pour ces contextes si nécessaire.

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

 

 




