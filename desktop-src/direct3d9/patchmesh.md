---
description: PatchMesh définit une maille définie par les correctifs de Bézier, y compris une liste de vertex et les correctifs pour la maille en indexant dans le tableau de vertex.
ms.assetid: vs|directx_sdk|~\patchmesh.htm
title: PatchMesh
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fabb3846246c7fb76a7146baf0b30bd9730fe24b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404712"
---
# <a name="patchmesh"></a><span data-ttu-id="83f5f-103">PatchMesh</span><span class="sxs-lookup"><span data-stu-id="83f5f-103">PatchMesh</span></span>

<span data-ttu-id="83f5f-104">Définit une maille définie par les correctifs de Bézier.</span><span class="sxs-lookup"><span data-stu-id="83f5f-104">Defines a mesh defined by Bézier patches.</span></span> <span data-ttu-id="83f5f-105">Le premier tableau est une liste de vertex, et le deuxième tableau définit les correctifs pour le maillage en indexant dans le tableau de vertex.</span><span class="sxs-lookup"><span data-stu-id="83f5f-105">The first array is a list of vertices, and the second array defines the patches for the mesh by indexing into the vertex array.</span></span>

``` syntax
template PatchMesh
{
    < D02C95CC-EDBA-4305-9B5D-1820D7704BBF >
    DWORD nVertices;
    array Vector vertices[nVertices];
    DWORD nPatches;
    array Patch patches[nPatches];
    [ ... ]
}
```

<span data-ttu-id="83f5f-106">Où :</span><span class="sxs-lookup"><span data-stu-id="83f5f-106">Where:</span></span>

-   <span data-ttu-id="83f5f-107">nVertices-nombre de vertex.</span><span class="sxs-lookup"><span data-stu-id="83f5f-107">nVertices - Number of vertices.</span></span>
-   <span data-ttu-id="83f5f-108">vertex \[ nVertices \] -tableau de vertex.</span><span class="sxs-lookup"><span data-stu-id="83f5f-108">vertices\[nVertices\] - Array of vertices.</span></span> <span data-ttu-id="83f5f-109">Consultez [**Vector**](vector.md).</span><span class="sxs-lookup"><span data-stu-id="83f5f-109">See [**Vector**](vector.md).</span></span>
-   <span data-ttu-id="83f5f-110">nPatches : nombre de correctifs.</span><span class="sxs-lookup"><span data-stu-id="83f5f-110">nPatches - Number of patches.</span></span>
-   <span data-ttu-id="83f5f-111">patchs \[ nPatches \] -Array of patchs.</span><span class="sxs-lookup"><span data-stu-id="83f5f-111">patches\[nPatches\] - Array of patches.</span></span> <span data-ttu-id="83f5f-112">Consultez [**patch**](patch.md).</span><span class="sxs-lookup"><span data-stu-id="83f5f-112">See [**Patch**](patch.md).</span></span>
-   <span data-ttu-id="83f5f-113">\[ ... \] -N’importe quel modèle de fichier. x peut être utilisé ici.</span><span class="sxs-lookup"><span data-stu-id="83f5f-113">\[ ... \] - Any .x file template can be used here.</span></span> <span data-ttu-id="83f5f-114">L’architecture est ainsi extensible.</span><span class="sxs-lookup"><span data-stu-id="83f5f-114">This makes the architecture extensible.</span></span>

<span data-ttu-id="83f5f-115">Les correctifs utilisent les vertex dans le tableau de vertex comme points de contrôle pour chaque correctif.</span><span class="sxs-lookup"><span data-stu-id="83f5f-115">The patches use the vertices in the array of vertices as the control points for each patch.</span></span> <span data-ttu-id="83f5f-116">Il s’agit d’un modèle hérité.</span><span class="sxs-lookup"><span data-stu-id="83f5f-116">This is a legacy template.</span></span> <span data-ttu-id="83f5f-117">Le dernier modèle de maillage des correctifs est [**PatchMesh9**](patchmesh9.md).</span><span class="sxs-lookup"><span data-stu-id="83f5f-117">The latest patch mesh template is [**PatchMesh9**](patchmesh9.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="83f5f-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83f5f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83f5f-119">Modèles</span><span class="sxs-lookup"><span data-stu-id="83f5f-119">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



