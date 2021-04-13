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
# <a name="manipulating-images-for-use-in-texturing"></a>Manipulation d’images à utiliser dans la texturation

La bibliothèque d’utilitaires OpenGL (GLU) fournit des fonctions de mise à l’échelle des images et de mappage MIP automatiques pour simplifier la spécification des images de texture. La fonction [**gluScaleImage**](gluscaleimage.md) met à l’échelle une image spécifiée à une taille de texture acceptée ; vous pouvez passer l’image résultante à OpenGL comme texture. Les fonctions mappage MIP automatiques, [**gluBuild1DMipmaps**](glubuild1dmipmaps.md) et [**gluBuild2DMipmaps**](glubuild2dmipmaps.md), créent des images de texture mipmapped à partir d’une image spécifiée et les transmettent à [**glTexImage1D**](glteximage1d.md) et [**glTexImage2D**](glteximage2d.md), respectivement.

 

 




