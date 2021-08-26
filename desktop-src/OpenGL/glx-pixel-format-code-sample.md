---
title: Exemple de code de format de pixel GLX
description: L’exemple de code ci-dessous montre comment un programme X Window System OpenGL utilise des fonctions de mise en forme de GLX Visual/pixel.
ms.assetid: f01193a9-c0ff-4399-a86e-06bb4603b3f1
keywords:
- portage vers OpenGL, pixels
- Portage OpenGL, pixels
- X système de fenêtre, pixels
- GLX fonctions, pixels
- pixels, exemple GLX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 312b95fb2ff4719c9ecda863b67ac926905b09d0e4b8aecbcc673a03c18c307a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035384"
---
# <a name="glx-pixel-format-code-sample"></a>Exemple de code de format de pixel GLX

L’exemple de code ci-dessous montre comment un programme X Window System OpenGL utilise des fonctions de mise en forme de GLX Visual/pixel.


```C++
/* X globals, defines, and prototypes */ 
Display *dpy; 
Window glwin; 
static int attributes[] = {GLX_DEPTH_SIZE, 16, GLX_DOUBLEBUFFER, None}; 
        
    /* find an OpenGL-capable Color Index visual with depth buffer */ 
    vi = glXChooseVisual(dpy, DefaultScreen(dpy), attributes); 
    if (vi == NULL) { 
        fprintf(stderr, "could not get visual\n"); 
        exit(1); 
    }
```



Le visuel peut être utilisé pour créer une fenêtre et un contexte de rendu.

 

 




