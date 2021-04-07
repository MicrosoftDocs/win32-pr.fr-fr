---
description: Ce modèle est instancié par maillage, contenant des informations sur les vertex de la maille qui sont des doublons.
ms.assetid: dd30b3d6-767a-4d87-9b5c-1324738bcbb2
title: FaceAdjacency
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a2fd0f0b2bb328aa8b5ec39e7481c0b7fd766fc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745572"
---
# <a name="faceadjacency"></a><span data-ttu-id="92ccb-103">FaceAdjacency</span><span class="sxs-lookup"><span data-stu-id="92ccb-103">FaceAdjacency</span></span>

<span data-ttu-id="92ccb-104">Ce modèle est instancié par maillage, contenant des informations sur les vertex de la maille qui sont des doublons.</span><span class="sxs-lookup"><span data-stu-id="92ccb-104">This template is instantiated on a per-mesh basis, holding information about which vertices in the mesh are duplicates of each other.</span></span> <span data-ttu-id="92ccb-105">Le résultat est dupliqué lorsqu’un sommet se trouve sur un groupe de lissage ou une limite de matériau.</span><span class="sxs-lookup"><span data-stu-id="92ccb-105">Duplicates result when a vertex sits on a smoothing group or material boundary.</span></span> <span data-ttu-id="92ccb-106">L’objectif de ce modèle est de permettre au chargeur de déterminer quels vertex qui présentent des paramètres de périphérique différents sont en fait les mêmes sommets dans le modèle.</span><span class="sxs-lookup"><span data-stu-id="92ccb-106">The purpose of this template is to allow the loader to determine which vertices exhibiting different peripheral parameters are actually the same vertexes in the model.</span></span> <span data-ttu-id="92ccb-107">Certaines applications (telles que la simplification du maillage, par exemple) peuvent utiliser ces informations.</span><span class="sxs-lookup"><span data-stu-id="92ccb-107">Certain applications (mesh simplification, for example) can make use of this information.</span></span>

``` syntax
template FaceAdjacency
{
    < A64C844A-E282-4756-8B80-250CDE04398C >
    DWORD nIndices;
    array DWORD indices[nIndices];
} 
```

<span data-ttu-id="92ccb-108">Où :</span><span class="sxs-lookup"><span data-stu-id="92ccb-108">Where:</span></span>

-   <span data-ttu-id="92ccb-109">nIndices : nombre d’index dans la maille.</span><span class="sxs-lookup"><span data-stu-id="92ccb-109">nIndices - Number of indices in the mesh.</span></span>
-   <span data-ttu-id="92ccb-110">index \[ nIndices \] -tableau d’index.</span><span class="sxs-lookup"><span data-stu-id="92ccb-110">indices\[nIndices\] - Array of indices.</span></span>

## <a name="see-also"></a><span data-ttu-id="92ccb-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92ccb-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92ccb-112">Modèles</span><span class="sxs-lookup"><span data-stu-id="92ccb-112">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



