---
title: Fonctions de mémoire tampon
description: Pour copier le contenu d’une mémoire tampon hors écran dans une mémoire tampon à l’écran, appelez SwapBuffers.
ms.assetid: 605eba4e-ee38-4e62-adf8-1b7894030cb0
keywords:
- WGL, mémoire tampon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96b03a12cd07b76d1329f51cc982508c707e011701b072a42b099df05327842d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118618593"
---
# <a name="buffer-functions"></a>Fonctions de mémoire tampon

Pour copier le contenu d’une mémoire tampon hors écran dans une mémoire tampon à l’écran, appelez [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers). La fonction **SwapBuffers** prend un handle vers un contexte de périphérique (Device Context). Le format de pixel actuel du contexte de périphérique spécifié doit inclure une mémoire tampon d’arrière-plan. Par défaut, la mémoire tampon d’arrière-plan est hors écran et la mémoire tampon d’affichage est à l’écran.

> [!Note]  
> La fonction **SwapBuffers** n’échange pas vraiment le contenu des deux mémoires tampons, mais copie le contenu d’une mémoire tampon vers une autre. Le contenu de la mémoire tampon hors écran n’est pas défini après un appel à **SwapBuffers**. Ainsi, le résultat de deux appels consécutifs à **SwapBuffers** n’est pas défini.

 

L’illustration suivante montre comment le contenu des mémoires tampons est copié lors de l’appel de **SwapBuffers**.

![Diagramme montrant les résultats non définis des appels consécutifs à la fonction SwapBuffers.](images/opengl00.png)

Plusieurs fonctions OpenGL Core gèrent également les mémoires tampons. La fonction [**glDrawBuffer**](gldrawbuffer.md) est celle qui est la plus pertinente pour la double mise en mémoire tampon ; Il spécifie les trame ou les mémoires tampons dans lesquelles OpenGL crée des dessins.

Les fonctions suivantes affectent également les mémoires tampons :

-   [**glReadBuffer**](glreadbuffer.md)
-   [**glReadPixels**](glreadpixels.md)
-   [**glCopyPixels**](glcopypixels.md)
-   [**glAccum**](glaccum.md)
-   [**glColorMask**](glcolormask.md)
-   [**glDepthMask**](gldepthmask.md)
-   [**glIndexMask**](glindexmask.md)
-   [**glStencilMask**](glstencilmask.md)
-   [**glClearAccum**](glclearaccum.md)
-   [**glClearColor**](glclearcolor.md)
-   [**glClearDepth**](glcleardepth.md)
-   [**glClearIndex**](glclearindex.md)
-   [**glClearStencil**](glclearstencil.md)

 

 




