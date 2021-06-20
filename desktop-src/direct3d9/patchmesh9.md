---
description: PatchMesh9 définit une maille définie par les correctifs de Bézier, y compris une liste de vertex et les correctifs pour la maille en indexant dans le tableau de vertex.
ms.assetid: 642ca513-c83e-4c6d-845c-0eaecc232728
title: PatchMesh9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 811e593117f2ec57a4718ea8078d96bcea87e71f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404702"
---
# <a name="patchmesh9"></a><span data-ttu-id="dffe6-103">PatchMesh9</span><span class="sxs-lookup"><span data-stu-id="dffe6-103">PatchMesh9</span></span>

<span data-ttu-id="dffe6-104">Définit une maille définie par les correctifs de Bézier.</span><span class="sxs-lookup"><span data-stu-id="dffe6-104">Defines a mesh defined by Bézier patches.</span></span> <span data-ttu-id="dffe6-105">Le premier tableau est une liste de vertex, et le deuxième tableau définit les correctifs pour le maillage en indexant dans le tableau de vertex.</span><span class="sxs-lookup"><span data-stu-id="dffe6-105">The first array is a list of vertices, and the second array defines the patches for the mesh by indexing into the vertex array.</span></span>

``` syntax
template PatchMesh9
{
    < B9EC94E1-B9A6-4251-BA18-94893F02C0EA >
    DWORD Type;
    DWORD Degree;
    DWORD Basis;
    DWORD nVertices;
    array Vector vertices[nVertices];
    DWORD nPatches;
    array Patch patches[nPatches];
    [ ... ]
} 
```

<span data-ttu-id="dffe6-106">Où :</span><span class="sxs-lookup"><span data-stu-id="dffe6-106">Where:</span></span>

-   <span data-ttu-id="dffe6-107">Type-type de maillage des correctifs : rectangle, triangle ou N-patch.</span><span class="sxs-lookup"><span data-stu-id="dffe6-107">Type - Patch mesh type: rectangle, triangle, or N-patch.</span></span>
-   <span data-ttu-id="dffe6-108">Degré-degré des variables dans l’équation de la courbe.</span><span class="sxs-lookup"><span data-stu-id="dffe6-108">Degree - Degree of the variables in the curve equation.</span></span>
-   <span data-ttu-id="dffe6-109">Base : type de base d’une surface corrective de poids fort.</span><span class="sxs-lookup"><span data-stu-id="dffe6-109">Basis - Basis type of a high-order patch surface.</span></span>
-   <span data-ttu-id="dffe6-110">nVertices-nombre de vertex.</span><span class="sxs-lookup"><span data-stu-id="dffe6-110">nVertices - Number of vertices.</span></span>
-   <span data-ttu-id="dffe6-111">vertex \[ nVertices \] -tableau de vertex.</span><span class="sxs-lookup"><span data-stu-id="dffe6-111">vertices\[nVertices\] - Array of vertices.</span></span> <span data-ttu-id="dffe6-112">Consultez [**Vector**](vector.md).</span><span class="sxs-lookup"><span data-stu-id="dffe6-112">See [**Vector**](vector.md).</span></span>
-   <span data-ttu-id="dffe6-113">nPatches : nombre de correctifs.</span><span class="sxs-lookup"><span data-stu-id="dffe6-113">nPatches - Number of patches.</span></span>
-   <span data-ttu-id="dffe6-114">patchs \[ nPatches \] -Array of patchs.</span><span class="sxs-lookup"><span data-stu-id="dffe6-114">patches\[nPatches\] - Array of patches.</span></span> <span data-ttu-id="dffe6-115">Consultez [**patch**](patch.md).</span><span class="sxs-lookup"><span data-stu-id="dffe6-115">See [**Patch**](patch.md).</span></span>
-   <span data-ttu-id="dffe6-116">\[ ... \] -N’importe quel modèle de fichier. x peut être utilisé ici.</span><span class="sxs-lookup"><span data-stu-id="dffe6-116">\[ ... \] - Any .x file template can be used here.</span></span> <span data-ttu-id="dffe6-117">L’architecture est ainsi extensible.</span><span class="sxs-lookup"><span data-stu-id="dffe6-117">This makes the architecture extensible.</span></span>

<span data-ttu-id="dffe6-118">Les correctifs utilisent les vertex dans le tableau de vertex comme points de contrôle pour chaque correctif.</span><span class="sxs-lookup"><span data-stu-id="dffe6-118">The patches use the vertices in the array of vertices as the control points for each patch.</span></span>

## <a name="see-also"></a><span data-ttu-id="dffe6-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dffe6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dffe6-120">Modèles</span><span class="sxs-lookup"><span data-stu-id="dffe6-120">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



