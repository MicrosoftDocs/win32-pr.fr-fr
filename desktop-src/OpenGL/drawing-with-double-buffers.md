---
title: Dessiner avec deux mémoires tampons
description: Les doubles mémoires tampons lissent la transition entre une image et une autre à l’écran.
ms.assetid: 10801cc7-d26c-4bfd-95c0-f352a1c7a1f5
keywords:
- OpenGL sur Windows, doubles mémoires tampons
- doubles mémoires tampons OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbe52d427467b2a6e460ea56a9e72e580ea6f97d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311080"
---
# <a name="drawing-with-double-buffers"></a><span data-ttu-id="64d7e-105">Dessiner avec deux mémoires tampons</span><span class="sxs-lookup"><span data-stu-id="64d7e-105">Drawing with Double Buffers</span></span>

<span data-ttu-id="64d7e-106">Les doubles mémoires tampons lissent la transition entre une image et une autre à l’écran.</span><span class="sxs-lookup"><span data-stu-id="64d7e-106">Double buffers smooth the transition between one image and another on the screen.</span></span> <span data-ttu-id="64d7e-107">L’échange de mémoires tampons est généralement effectué à la fin d’une séquence de commandes de dessin.</span><span class="sxs-lookup"><span data-stu-id="64d7e-107">Swapping buffers typically comes at the end of a sequence of drawing commands.</span></span> <span data-ttu-id="64d7e-108">Par défaut, l’implémentation Microsoft de OpenGL dans Windows s’appuie sur la mémoire tampon hors écran. une fois le dessin terminé, vous appelez la fonction [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) pour copier la mémoire tampon hors écran dans la mémoire tampon à l’écran.</span><span class="sxs-lookup"><span data-stu-id="64d7e-108">By default, the Microsoft implementation of OpenGL in Windows draws to the off-screen buffer; when drawing is complete, you call the [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) function to copy the off-screen buffer to the on-screen buffer.</span></span> <span data-ttu-id="64d7e-109">L’exemple de code suivant prépare le dessin, appelle une fonction de dessin, puis copie l’image terminée sur l’écran si la double mise en mémoire tampon est disponible.</span><span class="sxs-lookup"><span data-stu-id="64d7e-109">The following code sample prepares to draw, calls a drawing function, and then copies the completed image on to the screen if double buffering is available.</span></span>


```C++
void myRedraw(void) 
{ 
    // set up for drawing commands  
    glMatrixMode(GL_PROJECTION); 
    glLoadIdentity(); 
    gluPerspective(45, 1.0, 0.1, 100.0); 
 
    // draw our objects  
    myDrawAllObjects(GL_FALSE); 
 
    // if we're double-buffering ...  
    if (bDoubleBuffering)  
 
        // ...draw the copied image to the screen  
        SwapBuffers(hdc); 
}
```



<span data-ttu-id="64d7e-110">L’exemple de code suivant obtient un contexte de périphérique Windows, génère le rendu d’une scène, copie l’image à l’écran (pour afficher le rendu), puis libère le contexte de périphérique.</span><span class="sxs-lookup"><span data-stu-id="64d7e-110">The following code sample obtains a window device context, renders a scene, copies the image to the screen (to show the rendering), and then releases the device context.</span></span>


```C++
hdc = GetDC(hwnd); 
mySceneRenderingFunction(); 
SwapBuffers(hdc); 
ReleaseDC(hWnd, hdc);
```



 

 




