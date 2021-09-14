---
title: Fonctions de mémoire tampon
description: Pour copier le contenu d’une mémoire tampon hors écran dans une mémoire tampon à l’écran, appelez SwapBuffers.
ms.assetid: 605eba4e-ee38-4e62-adf8-1b7894030cb0
keywords:
- WGL, mémoire tampon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a93858b8085171a9139bc5ab329e531ddbb699
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127110345"
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

 

 




