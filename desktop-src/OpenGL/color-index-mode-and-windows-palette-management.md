---
title: Mode Color-Index et gestion des palettes Windows
description: Le mode d’index des couleurs spécifie les couleurs d’une palette logique avec un index d’une entrée spécifique de la palette logique.
ms.assetid: 8cf07c3e-8a8b-4f28-a363-34d3c0d33890
keywords:
- OpenGL sur Windows, gestion de palette
- OpenGL sur Windows, mode index des couleurs
- mode d’index de couleurs OpenGL
- gestion de la palette OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 873308c4ac64d496e344b1c71d440d4dc8321418
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029488"
---
# <a name="color-index-mode-and-windows-palette-management"></a><span data-ttu-id="b94b7-107">Mode Color-Index et gestion des palettes Windows</span><span class="sxs-lookup"><span data-stu-id="b94b7-107">Color-Index Mode and Windows Palette Management</span></span>

<span data-ttu-id="b94b7-108">Le mode d’index des couleurs spécifie les couleurs d’une palette logique avec un index d’une entrée spécifique de la palette logique.</span><span class="sxs-lookup"><span data-stu-id="b94b7-108">The color-index mode specifies colors in a logical palette with an index to a specific logical-palette entry.</span></span> <span data-ttu-id="b94b7-109">La plupart des programmes GDI utilisent des palettes d’index de couleurs, mais le mode RVBA fonctionne mieux pour OpenGL pour plusieurs effets, tels que l’ombrage, l’éclairage, le brouillard et le mappage de texture.</span><span class="sxs-lookup"><span data-stu-id="b94b7-109">Most GDI programs use color-index palettes, but the RGBA mode works better for OpenGL for several effects, such as shading, lighting, fog, and texture mapping.</span></span> <span data-ttu-id="b94b7-110">Si la couleur la plus vraie n’est pas critique pour votre application OpenGL, vous pouvez choisir d’utiliser le mode d’index des couleurs (par exemple, pour une carte topographique qui utilise « false Color » pour mettre en évidence le dégradé d’élévation).</span><span class="sxs-lookup"><span data-stu-id="b94b7-110">If having the truest color isn't critical for your OpenGL application, you might choose to use the color-index mode (for example, for a topographic map that uses "false color" to emphasize the elevation gradient).</span></span>

## <a name="color-index-mode-palette-sample"></a><span data-ttu-id="b94b7-111">Exemple de palette en mode Color-Index</span><span class="sxs-lookup"><span data-stu-id="b94b7-111">Color-Index Mode Palette Sample</span></span>

<span data-ttu-id="b94b7-112">Le code suivant configure une structure [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) qui définit l’indicateur du membre **iPixelType** sur PFD \_ type \_ ColorIndex.</span><span class="sxs-lookup"><span data-stu-id="b94b7-112">The following code sets up a [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) structure that sets the flag of the **iPixelType** member to PFD\_TYPE\_COLORINDEX.</span></span> <span data-ttu-id="b94b7-113">Cela spécifie que l’application utilise une palette d’index de couleurs.</span><span class="sxs-lookup"><span data-stu-id="b94b7-113">This specifies that the application use a color-index palette.</span></span>


```C++
BOOL bSetupPixelFormat(HDC hdc) 
{ 
    PIXELFORMATDESCRIPTOR pfd, *ppfd; 
    int pixelformat; 
 
    ppfd = &pfd; 
 
    ppfd->nSize = sizeof(PIXELFORMATDESCRIPTOR); 
    ppfd->nVersion = 1; 
    ppfd->dwFlags = PFD_DRAW_TO_WINDOW | PFD_SUPPORT_OPENGL |  
                        PFD_DOUBLEBUFFER; 
    ppfd->dwLayerMask = PFD_MAIN_PLANE; 
 
    /* Set to color-index mode and use the default color palette. */ 
    ppfd->iPixelType = PFD_TYPE_COLORINDEX;  
 
    ppfd->cColorBits = 8; 
    ppfd->cDepthBits = 16; 
    ppfd->cAccumBits = 0; 
    ppfd->cStencilBits = 0; 
 
    pixelformat = ChoosePixelFormat(hdc, ppfd); 
 
    if ( (pixelformat = ChoosePixelFormat(hdc, ppfd)) == 0 ) 
    { 
        MessageBox(NULL, "ChoosePixelFormat failed", "Error", MB_OK); 
        return FALSE; 
    } 
 
    if (SetPixelFormat(hdc, pixelformat, ppfd) == FALSE) 
    { 
        MessageBox(NULL, "SetPixelFormat failed", "Error", MB_OK); 
        return FALSE; 
    } 
 
    return TRUE; 
}
```



 

 




