---
description: 'VertexDuplicationIndices : ce modèle est instancié par maillage, en contenant des informations sur les vertex de la maille qui sont des doublons.'
ms.assetid: 43417389-69c1-4af6-92c2-75b621f9c165
title: VertexDuplicationIndices
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b33a8c5fca4f479eec6e9864d4528d4e3e4a1e32
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090176"
---
# <a name="vertexduplicationindices"></a><span data-ttu-id="3e11d-103">VertexDuplicationIndices</span><span class="sxs-lookup"><span data-stu-id="3e11d-103">VertexDuplicationIndices</span></span>

<span data-ttu-id="3e11d-104">Ce modèle est instancié par maillage, contenant des informations sur les vertex de la maille qui sont des doublons.</span><span class="sxs-lookup"><span data-stu-id="3e11d-104">This template is instantiated on a per-mesh basis, holding information about which vertices in the mesh are duplicates of each other.</span></span> <span data-ttu-id="3e11d-105">Le résultat est dupliqué lorsqu’un sommet se trouve sur un groupe de lissage ou une limite de matériau.</span><span class="sxs-lookup"><span data-stu-id="3e11d-105">Duplicates result when a vertex sits on a smoothing group or material boundary.</span></span> <span data-ttu-id="3e11d-106">L’objectif de ce modèle est de permettre au chargeur de déterminer quels vertex qui présentent des paramètres de périphérique différents sont en fait les mêmes sommets dans le modèle.</span><span class="sxs-lookup"><span data-stu-id="3e11d-106">The purpose of this template is to allow the loader to determine which vertices exhibiting different peripheral parameters are actually the same vertexes in the model.</span></span> <span data-ttu-id="3e11d-107">Certaines applications (telles que la simplification du maillage, par exemple) peuvent utiliser ces informations.</span><span class="sxs-lookup"><span data-stu-id="3e11d-107">Certain applications (mesh simplification, for example) can make use of this information.</span></span>

``` syntax
template VertexDuplicationIndices 
{ 
    < B8D65549-D7C9-4995-89CF-53A9A8B031E3 > 
    DWORD nIndices; 
    DWORD nOriginalVertices; 
    array DWORD indices[nIndices]; 
}
```

<span data-ttu-id="3e11d-108">Où :</span><span class="sxs-lookup"><span data-stu-id="3e11d-108">Where:</span></span>

-   <span data-ttu-id="3e11d-109">nIndices : nombre d’index de vertex.</span><span class="sxs-lookup"><span data-stu-id="3e11d-109">nIndices - Number of vertex indices.</span></span> <span data-ttu-id="3e11d-110">Il s’agit du nombre de vertex dans la maille.</span><span class="sxs-lookup"><span data-stu-id="3e11d-110">This is the number of vertices in the mesh.</span></span>
-   <span data-ttu-id="3e11d-111">nOriginalVertices : nombre de vertex dans la maille avant l’exécution d’une duplication.</span><span class="sxs-lookup"><span data-stu-id="3e11d-111">nOriginalVertices - Number of vertices in the mesh before any duplication occurs.</span></span>
-   <span data-ttu-id="3e11d-112">La valeur indices \[ n \] contient l’index de vertex que le vertex \[ n \] dans le tableau de vertex pour le maillage aurait eu si aucune duplication n’avait eu lieu.</span><span class="sxs-lookup"><span data-stu-id="3e11d-112">The value indices\[n\] holds the vertex index that vertex\[n\] in the vertex array for the mesh would have had if no duplication had occurred.</span></span> <span data-ttu-id="3e11d-113">Les index de ce tableau sont identiques, par conséquent, indiquent des vertex dupliqués.</span><span class="sxs-lookup"><span data-stu-id="3e11d-113">Indices in this array that are the same, therefore, indicate duplicate vertices.</span></span>

## <a name="see-also"></a><span data-ttu-id="3e11d-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e11d-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e11d-115">Modèles</span><span class="sxs-lookup"><span data-stu-id="3e11d-115">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



