---
description: Ce modèle est instancié par maillage, contenant des informations sur les vertex de la maille qui sont des doublons.
ms.assetid: 43417389-69c1-4af6-92c2-75b621f9c165
title: VertexDuplicationIndices
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d62278c206032c9a2dfed6ce9b2cd36c5e7456
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515299"
---
# <a name="vertexduplicationindices"></a><span data-ttu-id="02f2e-103">VertexDuplicationIndices</span><span class="sxs-lookup"><span data-stu-id="02f2e-103">VertexDuplicationIndices</span></span>

<span data-ttu-id="02f2e-104">Ce modèle est instancié par maillage, contenant des informations sur les vertex de la maille qui sont des doublons.</span><span class="sxs-lookup"><span data-stu-id="02f2e-104">This template is instantiated on a per-mesh basis, holding information about which vertices in the mesh are duplicates of each other.</span></span> <span data-ttu-id="02f2e-105">Le résultat est dupliqué lorsqu’un sommet se trouve sur un groupe de lissage ou une limite de matériau.</span><span class="sxs-lookup"><span data-stu-id="02f2e-105">Duplicates result when a vertex sits on a smoothing group or material boundary.</span></span> <span data-ttu-id="02f2e-106">L’objectif de ce modèle est de permettre au chargeur de déterminer quels vertex qui présentent des paramètres de périphérique différents sont en fait les mêmes sommets dans le modèle.</span><span class="sxs-lookup"><span data-stu-id="02f2e-106">The purpose of this template is to allow the loader to determine which vertices exhibiting different peripheral parameters are actually the same vertexes in the model.</span></span> <span data-ttu-id="02f2e-107">Certaines applications (telles que la simplification du maillage, par exemple) peuvent utiliser ces informations.</span><span class="sxs-lookup"><span data-stu-id="02f2e-107">Certain applications (mesh simplification, for example) can make use of this information.</span></span>

``` syntax
template VertexDuplicationIndices 
{ 
    < B8D65549-D7C9-4995-89CF-53A9A8B031E3 > 
    DWORD nIndices; 
    DWORD nOriginalVertices; 
    array DWORD indices[nIndices]; 
}
```

<span data-ttu-id="02f2e-108">Où :</span><span class="sxs-lookup"><span data-stu-id="02f2e-108">Where:</span></span>

-   <span data-ttu-id="02f2e-109">nIndices : nombre d’index de vertex.</span><span class="sxs-lookup"><span data-stu-id="02f2e-109">nIndices - Number of vertex indices.</span></span> <span data-ttu-id="02f2e-110">Il s’agit du nombre de vertex dans la maille.</span><span class="sxs-lookup"><span data-stu-id="02f2e-110">This is the number of vertices in the mesh.</span></span>
-   <span data-ttu-id="02f2e-111">nOriginalVertices : nombre de vertex dans la maille avant l’exécution d’une duplication.</span><span class="sxs-lookup"><span data-stu-id="02f2e-111">nOriginalVertices - Number of vertices in the mesh before any duplication occurs.</span></span>
-   <span data-ttu-id="02f2e-112">La valeur indices \[ n \] contient l’index de vertex que le vertex \[ n \] dans le tableau de vertex pour le maillage aurait eu si aucune duplication n’avait eu lieu.</span><span class="sxs-lookup"><span data-stu-id="02f2e-112">The value indices\[n\] holds the vertex index that vertex\[n\] in the vertex array for the mesh would have had if no duplication had occurred.</span></span> <span data-ttu-id="02f2e-113">Les index de ce tableau sont identiques, par conséquent, indiquent des vertex dupliqués.</span><span class="sxs-lookup"><span data-stu-id="02f2e-113">Indices in this array that are the same, therefore, indicate duplicate vertices.</span></span>

## <a name="see-also"></a><span data-ttu-id="02f2e-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02f2e-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02f2e-115">Modèles</span><span class="sxs-lookup"><span data-stu-id="02f2e-115">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



