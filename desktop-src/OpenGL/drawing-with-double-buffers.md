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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413690"
---
# <a name="drawing-with-double-buffers"></a>Dessiner avec deux mémoires tampons

Les doubles mémoires tampons lissent la transition entre une image et une autre à l’écran. L’échange de mémoires tampons est généralement effectué à la fin d’une séquence de commandes de dessin. par défaut, l’implémentation Microsoft de OpenGL dans Windows dessine dans la mémoire tampon hors écran. une fois le dessin terminé, vous appelez la fonction [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) pour copier la mémoire tampon hors écran dans la mémoire tampon à l’écran. L’exemple de code suivant prépare le dessin, appelle une fonction de dessin, puis copie l’image terminée sur l’écran si la double mise en mémoire tampon est disponible.


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



L’exemple de code suivant obtient un contexte de périphérique Windows, génère le rendu d’une scène, copie l’image à l’écran (pour afficher le rendu), puis libère le contexte de périphérique.


```C++
hdc = GetDC(hwnd); 
mySceneRenderingFunction(); 
SwapBuffers(hdc); 
ReleaseDC(hWnd, hdc);
```



 

 




