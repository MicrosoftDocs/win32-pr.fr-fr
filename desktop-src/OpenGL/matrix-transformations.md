---
title: Transformations de matrice
description: Les vertex et les normales sont transformés par les matrices de projection et de modelview avant d’être utilisées pour produire une image dans le trame.
ms.assetid: 9fd0b236-9152-4494-b5c7-dadb5943269e
keywords:
- Pipeline de traitement OpenGL, matrices
- matrices OpenGL
- matrice modelview
- matrice de projection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3db0ebd8bd13b8d2cee32b8873f697ab073140bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196674"
---
# <a name="matrix-transformations"></a><span data-ttu-id="87158-107">Transformations de matrice</span><span class="sxs-lookup"><span data-stu-id="87158-107">Matrix Transformations</span></span>

<span data-ttu-id="87158-108">Les vertex et les normales sont transformés par les matrices de projection et de modelview avant d’être utilisées pour produire une image dans le trame.</span><span class="sxs-lookup"><span data-stu-id="87158-108">Vertices and normals are transformed by the modelview and projection matrices before they're used to produce an image in the framebuffer.</span></span> <span data-ttu-id="87158-109">Utilisez des fonctions telles [**que glMatrixMode**](glmatrixmode.md), [**glMultMatrix \***](glmultmatrix.md), [**glRotate \***](glrotate.md), [**\* glTranslate**](gltranslate.md)et [**glScale \***](glscale.md) pour composer les transformations souhaitées.</span><span class="sxs-lookup"><span data-stu-id="87158-109">Use functions such as [**glMatrixMode**](glmatrixmode.md), [**glMultMatrix\***](glmultmatrix.md), [**glRotate\***](glrotate.md), [**glTranslate\***](gltranslate.md), and [**glScale\***](glscale.md) to compose the desired transformations.</span></span> <span data-ttu-id="87158-110">Ou spécifiez des matrices directement avec [**glLoadMatrix \***](glloadmatrix.md) et [**glLoadIdentity**](glloadidentity.md).</span><span class="sxs-lookup"><span data-stu-id="87158-110">Or specify matrices directly with [**glLoadMatrix\***](glloadmatrix.md) and [**glLoadIdentity**](glloadidentity.md).</span></span> <span data-ttu-id="87158-111">Utilisez [**glPushMatrix**](glpushmatrix.md) et [**glPopMatrix**](glpopmatrix.md) pour enregistrer et restaurer les matrices modelview et de projection sur leurs piles respectives.</span><span class="sxs-lookup"><span data-stu-id="87158-111">Use [**glPushMatrix**](glpushmatrix.md) and [**glPopMatrix**](glpopmatrix.md) to save and restore modelview and projection matrices on their respective stacks.</span></span>

 

 




