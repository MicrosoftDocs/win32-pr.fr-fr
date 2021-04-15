---
description: Définit une maille définie par les correctifs de Bézier. Le premier tableau est une liste de vertex, et le deuxième tableau définit les correctifs pour le maillage en indexant dans le tableau de vertex.
ms.assetid: vs|directx_sdk|~\patchmesh.htm
title: PatchMesh
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fcdefac9799736c796aef7cbb7222ab1942540d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520892"
---
# <a name="patchmesh"></a><span data-ttu-id="2dff2-104">PatchMesh</span><span class="sxs-lookup"><span data-stu-id="2dff2-104">PatchMesh</span></span>

<span data-ttu-id="2dff2-105">Définit une maille définie par les correctifs de Bézier.</span><span class="sxs-lookup"><span data-stu-id="2dff2-105">Defines a mesh defined by Bézier patches.</span></span> <span data-ttu-id="2dff2-106">Le premier tableau est une liste de vertex, et le deuxième tableau définit les correctifs pour le maillage en indexant dans le tableau de vertex.</span><span class="sxs-lookup"><span data-stu-id="2dff2-106">The first array is a list of vertices, and the second array defines the patches for the mesh by indexing into the vertex array.</span></span>

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

<span data-ttu-id="2dff2-107">Où :</span><span class="sxs-lookup"><span data-stu-id="2dff2-107">Where:</span></span>

-   <span data-ttu-id="2dff2-108">nVertices-nombre de vertex.</span><span class="sxs-lookup"><span data-stu-id="2dff2-108">nVertices - Number of vertices.</span></span>
-   <span data-ttu-id="2dff2-109">vertex \[ nVertices \] -tableau de vertex.</span><span class="sxs-lookup"><span data-stu-id="2dff2-109">vertices\[nVertices\] - Array of vertices.</span></span> <span data-ttu-id="2dff2-110">Consultez [**Vector**](vector.md).</span><span class="sxs-lookup"><span data-stu-id="2dff2-110">See [**Vector**](vector.md).</span></span>
-   <span data-ttu-id="2dff2-111">nPatches : nombre de correctifs.</span><span class="sxs-lookup"><span data-stu-id="2dff2-111">nPatches - Number of patches.</span></span>
-   <span data-ttu-id="2dff2-112">patchs \[ nPatches \] -Array of patchs.</span><span class="sxs-lookup"><span data-stu-id="2dff2-112">patches\[nPatches\] - Array of patches.</span></span> <span data-ttu-id="2dff2-113">Consultez [**patch**](patch.md).</span><span class="sxs-lookup"><span data-stu-id="2dff2-113">See [**Patch**](patch.md).</span></span>
-   <span data-ttu-id="2dff2-114">\[ ... \] -N’importe quel modèle de fichier. x peut être utilisé ici.</span><span class="sxs-lookup"><span data-stu-id="2dff2-114">\[ ... \] - Any .x file template can be used here.</span></span> <span data-ttu-id="2dff2-115">L’architecture est ainsi extensible.</span><span class="sxs-lookup"><span data-stu-id="2dff2-115">This makes the architecture extensible.</span></span>

<span data-ttu-id="2dff2-116">Les correctifs utilisent les vertex dans le tableau de vertex comme points de contrôle pour chaque correctif.</span><span class="sxs-lookup"><span data-stu-id="2dff2-116">The patches use the vertices in the array of vertices as the control points for each patch.</span></span> <span data-ttu-id="2dff2-117">Il s’agit d’un modèle hérité.</span><span class="sxs-lookup"><span data-stu-id="2dff2-117">This is a legacy template.</span></span> <span data-ttu-id="2dff2-118">Le dernier modèle de maillage des correctifs est [**PatchMesh9**](patchmesh9.md).</span><span class="sxs-lookup"><span data-stu-id="2dff2-118">The latest patch mesh template is [**PatchMesh9**](patchmesh9.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="2dff2-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2dff2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dff2-120">Modèles</span><span class="sxs-lookup"><span data-stu-id="2dff2-120">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



