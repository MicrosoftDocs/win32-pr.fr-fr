---
description: Utilisé par le modèle de maillage pour définir les visages d’un filet. Chaque élément du tableau nFaceVertexIndices fait référence à un vertex de maillage utilisé pour générer le visage.
ms.assetid: 38c40ebe-eca2-4dd9-95b8-b396225e3050
title: MeshFace
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a9e8b73efb214f7a767d986830cccc83ee6cbc1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108463"
---
# <a name="meshface"></a><span data-ttu-id="1632b-104">MeshFace</span><span class="sxs-lookup"><span data-stu-id="1632b-104">MeshFace</span></span>

<span data-ttu-id="1632b-105">Utilisé par le modèle de [**maillage**](mesh.md) pour définir les visages d’un filet.</span><span class="sxs-lookup"><span data-stu-id="1632b-105">Used by the [**Mesh**](mesh.md) template to define a mesh's faces.</span></span> <span data-ttu-id="1632b-106">Chaque élément du tableau nFaceVertexIndices fait référence à un vertex de maillage utilisé pour générer le visage.</span><span class="sxs-lookup"><span data-stu-id="1632b-106">Each element of the nFaceVertexIndices array references a mesh vertex used to build the face.</span></span>

``` syntax
template MeshFace
{
    < 3D82AB5F-62DA-11cf-AB39-0020AF71E433 >
    DWORD nFaceVertexIndices;
    array DWORD faceVertexIndices[nFaceVertexIndices];
} 
```

<span data-ttu-id="1632b-107">Où :</span><span class="sxs-lookup"><span data-stu-id="1632b-107">Where:</span></span>

-   <span data-ttu-id="1632b-108">nFaceVertexIndices-nombre d’index.</span><span class="sxs-lookup"><span data-stu-id="1632b-108">nFaceVertexIndices - Number of indices.</span></span>
-   <span data-ttu-id="1632b-109">Tableau DWORD faceVertexIndices \[ nFaceVertexIndices \] -tableau d’index.</span><span class="sxs-lookup"><span data-stu-id="1632b-109">array DWORD faceVertexIndices\[nFaceVertexIndices\] - Array of indices.</span></span>

## <a name="see-also"></a><span data-ttu-id="1632b-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1632b-110">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1632b-111">Modèles</span><span class="sxs-lookup"><span data-stu-id="1632b-111">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



