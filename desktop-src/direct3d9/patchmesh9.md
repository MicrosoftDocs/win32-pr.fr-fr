---
description: Définit une maille définie par les correctifs de Bézier. Le premier tableau est une liste de vertex, et le deuxième tableau définit les correctifs pour le maillage en indexant dans le tableau de vertex.
ms.assetid: 642ca513-c83e-4c6d-845c-0eaecc232728
title: PatchMesh9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b3d8232fe8c83358feb216acfb45a7877d7acb9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106513909"
---
# <a name="patchmesh9"></a><span data-ttu-id="e088c-104">PatchMesh9</span><span class="sxs-lookup"><span data-stu-id="e088c-104">PatchMesh9</span></span>

<span data-ttu-id="e088c-105">Définit une maille définie par les correctifs de Bézier.</span><span class="sxs-lookup"><span data-stu-id="e088c-105">Defines a mesh defined by Bézier patches.</span></span> <span data-ttu-id="e088c-106">Le premier tableau est une liste de vertex, et le deuxième tableau définit les correctifs pour le maillage en indexant dans le tableau de vertex.</span><span class="sxs-lookup"><span data-stu-id="e088c-106">The first array is a list of vertices, and the second array defines the patches for the mesh by indexing into the vertex array.</span></span>

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

<span data-ttu-id="e088c-107">Où :</span><span class="sxs-lookup"><span data-stu-id="e088c-107">Where:</span></span>

-   <span data-ttu-id="e088c-108">Type-type de maillage des correctifs : rectangle, triangle ou N-patch.</span><span class="sxs-lookup"><span data-stu-id="e088c-108">Type - Patch mesh type: rectangle, triangle, or N-patch.</span></span>
-   <span data-ttu-id="e088c-109">Degré-degré des variables dans l’équation de la courbe.</span><span class="sxs-lookup"><span data-stu-id="e088c-109">Degree - Degree of the variables in the curve equation.</span></span>
-   <span data-ttu-id="e088c-110">Base : type de base d’une surface corrective de poids fort.</span><span class="sxs-lookup"><span data-stu-id="e088c-110">Basis - Basis type of a high-order patch surface.</span></span>
-   <span data-ttu-id="e088c-111">nVertices-nombre de vertex.</span><span class="sxs-lookup"><span data-stu-id="e088c-111">nVertices - Number of vertices.</span></span>
-   <span data-ttu-id="e088c-112">vertex \[ nVertices \] -tableau de vertex.</span><span class="sxs-lookup"><span data-stu-id="e088c-112">vertices\[nVertices\] - Array of vertices.</span></span> <span data-ttu-id="e088c-113">Consultez [**Vector**](vector.md).</span><span class="sxs-lookup"><span data-stu-id="e088c-113">See [**Vector**](vector.md).</span></span>
-   <span data-ttu-id="e088c-114">nPatches : nombre de correctifs.</span><span class="sxs-lookup"><span data-stu-id="e088c-114">nPatches - Number of patches.</span></span>
-   <span data-ttu-id="e088c-115">patchs \[ nPatches \] -Array of patchs.</span><span class="sxs-lookup"><span data-stu-id="e088c-115">patches\[nPatches\] - Array of patches.</span></span> <span data-ttu-id="e088c-116">Consultez [**patch**](patch.md).</span><span class="sxs-lookup"><span data-stu-id="e088c-116">See [**Patch**](patch.md).</span></span>
-   <span data-ttu-id="e088c-117">\[ ... \] -N’importe quel modèle de fichier. x peut être utilisé ici.</span><span class="sxs-lookup"><span data-stu-id="e088c-117">\[ ... \] - Any .x file template can be used here.</span></span> <span data-ttu-id="e088c-118">L’architecture est ainsi extensible.</span><span class="sxs-lookup"><span data-stu-id="e088c-118">This makes the architecture extensible.</span></span>

<span data-ttu-id="e088c-119">Les correctifs utilisent les vertex dans le tableau de vertex comme points de contrôle pour chaque correctif.</span><span class="sxs-lookup"><span data-stu-id="e088c-119">The patches use the vertices in the array of vertices as the control points for each patch.</span></span>

## <a name="see-also"></a><span data-ttu-id="e088c-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e088c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e088c-121">Modèles</span><span class="sxs-lookup"><span data-stu-id="e088c-121">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



