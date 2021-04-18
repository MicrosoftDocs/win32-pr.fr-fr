---
title: Choix et définition d’un format de pixel Best-Match
description: Cette rubrique explique la procédure de mise en correspondance d’un contexte de périphérique et d’un format de pixel.
ms.assetid: 7b974fb5-e34d-4781-858c-572c4e7754bc
keywords:
- OpenGL sur Windows, pixels
- format de pixel de meilleure correspondance OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 143800a9c43d8c8a7779bb5e6cd119c6737f8129
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511824"
---
# <a name="choosing-and-setting-a-best-match-pixel-format"></a><span data-ttu-id="573ee-105">Choix et définition d’un format de pixel Best-Match</span><span class="sxs-lookup"><span data-stu-id="573ee-105">Choosing and Setting a Best-Match Pixel Format</span></span>

<span data-ttu-id="573ee-106">Cette rubrique explique la procédure de mise en correspondance d’un contexte de périphérique et d’un format de pixel.</span><span class="sxs-lookup"><span data-stu-id="573ee-106">This topic explains the procedure for matching a device context to a pixel format.</span></span>

<span data-ttu-id="573ee-107">**Pour obtenir la meilleure correspondance entre un contexte de périphérique et un format de pixel**</span><span class="sxs-lookup"><span data-stu-id="573ee-107">**To obtain a device context's best match to a pixel format**</span></span>

1.  <span data-ttu-id="573ee-108">Spécifiez le format de pixel souhaité dans une structure [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) .</span><span class="sxs-lookup"><span data-stu-id="573ee-108">Specify the desired pixel format in a [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) structure.</span></span>
2.  <span data-ttu-id="573ee-109">Appelez [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat).</span><span class="sxs-lookup"><span data-stu-id="573ee-109">Call [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat).</span></span>

    <span data-ttu-id="573ee-110">La fonction **ChoosePixelFormat** retourne un index de format de pixel, que vous pouvez ensuite passer à [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat) pour définir le meilleur format de pixel correspondant au format de pixel actuel du contexte de périphérique.</span><span class="sxs-lookup"><span data-stu-id="573ee-110">The **ChoosePixelFormat** function returns a pixel format index, which you can then pass to [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat) to set the best pixel format match as the device context's current pixel format.</span></span>

<span data-ttu-id="573ee-111">L’exemple de code suivant montre comment effectuer les étapes ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="573ee-111">The following code sample shows how to carry out the above steps.</span></span>


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



 

 




