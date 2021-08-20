---
title: Choix et définition d’un format de pixel Best-Match
description: Cette rubrique explique la procédure de mise en correspondance d’un contexte de périphérique et d’un format de pixel.
ms.assetid: 7b974fb5-e34d-4781-858c-572c4e7754bc
keywords:
- OpenGL sur Windows, pixels
- format de pixel de meilleure correspondance OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 258364e18ff38cb67edd1315f261a55a91f58fe940b026e1fcb7b63ed2e12eac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063299"
---
# <a name="choosing-and-setting-a-best-match-pixel-format"></a>Choix et définition d’un format de pixel Best-Match

Cette rubrique explique la procédure de mise en correspondance d’un contexte de périphérique et d’un format de pixel.

**Pour obtenir la meilleure correspondance entre un contexte de périphérique et un format de pixel**

1.  Spécifiez le format de pixel souhaité dans une structure [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) .
2.  Appelez [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat).

    La fonction **ChoosePixelFormat** retourne un index de format de pixel, que vous pouvez ensuite passer à [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat) pour définir le meilleur format de pixel correspondant au format de pixel actuel du contexte de périphérique.

L’exemple de code suivant montre comment effectuer les étapes ci-dessus.


```C++
PIXELFORMATDESCRIPTOR pfd = { 
    sizeof(PIXELFORMATDESCRIPTOR),    // size of this pfd  
    1,                                // version number  
    PFD_DRAW_TO_WINDOW |              // support window  
    PFD_SUPPORT_OPENGL |              // support OpenGL  
    PFD_DOUBLEBUFFER,                 // double buffered  
    PFD_TYPE_RGBA,                    // RGBA type  
    24,                               // 24-bit color depth  
    0, 0, 0, 0, 0, 0,                 // color bits ignored  
    0,                                // no alpha buffer  
    0,                                // shift bit ignored  
    0,                                // no accumulation buffer  
    0, 0, 0, 0,                       // accum bits ignored  
    32,                               // 32-bit z-buffer      
    0,                                // no stencil buffer  
    0,                                // no auxiliary buffer  
    PFD_MAIN_PLANE,                   // main layer  
    0,                                // reserved  
    0, 0, 0                           // layer masks ignored  
}; 
HDC  hdc; 
int  iPixelFormat; 
 
// get the device context's best, available pixel format match  
iPixelFormat = ChoosePixelFormat(hdc, &pfd); 
 
// make that match the device context's current pixel format  
SetPixelFormat(hdc, iPixelFormat, &pfd);
```



 

 




