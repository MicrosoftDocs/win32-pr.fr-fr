---
title: gestion du Mode de Color-Index et de la Palette de Windows
description: Le mode d’index des couleurs spécifie les couleurs d’une palette logique avec un index d’une entrée spécifique de la palette logique.
ms.assetid: 8cf07c3e-8a8b-4f28-a363-34d3c0d33890
keywords:
- OpenGL sur Windows, gestion de la palette
- OpenGL sur Windows, mode index des couleurs
- mode d’index de couleurs OpenGL
- gestion de la palette OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72e4d7c9db02a80bdffdef93655e88cc5b2ca8197a58c5ffdb488c2b782f10d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889259"
---
# <a name="color-index-mode-and-windows-palette-management"></a>gestion du Mode de Color-Index et de la Palette de Windows

Le mode d’index des couleurs spécifie les couleurs d’une palette logique avec un index d’une entrée spécifique de la palette logique. La plupart des programmes GDI utilisent des palettes d’index de couleurs, mais le mode RVBA fonctionne mieux pour OpenGL pour plusieurs effets, tels que l’ombrage, l’éclairage, le brouillard et le mappage de texture. Si la couleur la plus vraie n’est pas critique pour votre application OpenGL, vous pouvez choisir d’utiliser le mode d’index des couleurs (par exemple, pour une carte topographique qui utilise « false Color » pour mettre en évidence le dégradé d’élévation).

## <a name="color-index-mode-palette-sample"></a>Exemple de palette en mode Color-Index

Le code suivant configure une structure [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) qui définit l’indicateur du membre **iPixelType** sur PFD \_ type \_ ColorIndex. Cela spécifie que l’application utilise une palette d’index de couleurs.


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



 

 




