---
title: Manipulation d’images à utiliser dans la texturation
description: La bibliothèque d’utilitaires OpenGL (GLU) fournit des fonctions de mise à l’échelle des images et de mappage MIP automatiques pour simplifier la spécification des images de texture.
ms.assetid: 20edf665-1fed-4761-b8b1-beee02c78b0d
keywords:
- Utilitaire OpenGL (GLU), mise à l’échelle des images
- GLU (utilitaire OpenGL), mise à l’échelle des images
- Utilitaire OpenGL (GLU), mappage MIP automatique
- GLU (utilitaire OpenGL), mappage MIP automatique
- Utilitaire OpenGL (GLU), images de texture
- GLU (utilitaire OpenGL), images de texture
- Bibliothèque GLU, images de texture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16726493bbcb6e0116e4c158e470029f34f5b652
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309794"
---
# <a name="manipulating-images-for-use-in-texturing"></a><span data-ttu-id="024ec-110">Manipulation d’images à utiliser dans la texturation</span><span class="sxs-lookup"><span data-stu-id="024ec-110">Manipulating Images for Use in Texturing</span></span>

<span data-ttu-id="024ec-111">La bibliothèque d’utilitaires OpenGL (GLU) fournit des fonctions de mise à l’échelle des images et de mappage MIP automatiques pour simplifier la spécification des images de texture.</span><span class="sxs-lookup"><span data-stu-id="024ec-111">The OpenGL Utility library (GLU) provides image scaling and automatic mipmapping functions to simplify the specification of texture images.</span></span> <span data-ttu-id="024ec-112">La fonction [**gluScaleImage**](gluscaleimage.md) met à l’échelle une image spécifiée à une taille de texture acceptée ; vous pouvez passer l’image résultante à OpenGL comme texture.</span><span class="sxs-lookup"><span data-stu-id="024ec-112">The [**gluScaleImage**](gluscaleimage.md) function scales a specified image to an accepted texture size; you can pass the resulting image to OpenGL as a texture.</span></span> <span data-ttu-id="024ec-113">Les fonctions mappage MIP automatiques, [**gluBuild1DMipmaps**](glubuild1dmipmaps.md) et [**gluBuild2DMipmaps**](glubuild2dmipmaps.md), créent des images de texture mipmapped à partir d’une image spécifiée et les transmettent à [**glTexImage1D**](glteximage1d.md) et [**glTexImage2D**](glteximage2d.md), respectivement.</span><span class="sxs-lookup"><span data-stu-id="024ec-113">The automatic mipmapping functions, [**gluBuild1DMipmaps**](glubuild1dmipmaps.md) and [**gluBuild2DMipmaps**](glubuild2dmipmaps.md), create mipmapped texture images from a specified image and pass them to [**glTexImage1D**](glteximage1d.md) and [**glTexImage2D**](glteximage2d.md), respectively.</span></span>

 

 




