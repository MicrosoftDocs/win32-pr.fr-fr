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
ms.openlocfilehash: 873308c4ac64d496e344b1c71d440d4dc8321418
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127096682"
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



 

 




