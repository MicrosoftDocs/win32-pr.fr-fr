---
description: Ce modèle est instancié au niveau de chaque maille.
ms.assetid: ac5289c6-989c-43b4-9190-ac8f831a05f0
title: SkinWeights
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 759239a3a7ec8ebb608cf9ede6624105cee321b4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520884"
---
# <a name="skinweights"></a><span data-ttu-id="428c3-103">SkinWeights</span><span class="sxs-lookup"><span data-stu-id="428c3-103">SkinWeights</span></span>

<span data-ttu-id="428c3-104">Ce modèle est instancié au niveau de chaque maille.</span><span class="sxs-lookup"><span data-stu-id="428c3-104">This template is instantiated on a per-mesh basis.</span></span> <span data-ttu-id="428c3-105">Au sein d’une maille, une séquence de n instances de ce modèle s’affiche, où n est le nombre d’OS (images de fichiers X) qui influencent les vertex de la maille.</span><span class="sxs-lookup"><span data-stu-id="428c3-105">Within a mesh, a sequence of n instances of this template will appear, where n is the number of bones (X file frames) that influence the vertices in the mesh.</span></span> <span data-ttu-id="428c3-106">Chaque instance du modèle définit fondamentalement l’influence d’un segment particulier sur la maille.</span><span class="sxs-lookup"><span data-stu-id="428c3-106">Each instance of the template basically defines the influence of a particular bone on the mesh.</span></span> <span data-ttu-id="428c3-107">Il existe une liste d’index de vertex et une liste correspondante de poids.</span><span class="sxs-lookup"><span data-stu-id="428c3-107">There is a list of vertex indices, and a corresponding list of weights.</span></span>

``` syntax
template SkinWeights 
{ 
    < 6F0D123B-BAD2-4167-A0D0-80224F25FABB > 
    STRING transformNodeName; 
    DWORD nWeights; 
    array DWORD vertexIndices[nWeights]; 
    array float weights[nWeights]; 
    Matrix4x4 matrixOffset; 
} 
```

<span data-ttu-id="428c3-108">Où :</span><span class="sxs-lookup"><span data-stu-id="428c3-108">Where:</span></span>

-   <span data-ttu-id="428c3-109">Le nom du segment dont l’influence est définie est transformNodeName et nWeights est le nombre de vertex affectés par ce segment.</span><span class="sxs-lookup"><span data-stu-id="428c3-109">The name of the bone whose influence is being defined is transformNodeName, and nWeights is the number of vertices affected by this bone.</span></span>
-   <span data-ttu-id="428c3-110">Les vertex influencés par ce segment sont contenus dans vertexIndices et les poids de chacun des vertex influencés par ce segment sont contenus dans les pondérations.</span><span class="sxs-lookup"><span data-stu-id="428c3-110">The vertices influenced by this bone are contained in vertexIndices, and the weights for each of the vertices influenced by this bone are contained in weights.</span></span>
-   <span data-ttu-id="428c3-111">La matrice matrixOffset transforme les sommets de maillage en espace du segment.</span><span class="sxs-lookup"><span data-stu-id="428c3-111">The matrix matrixOffset transforms the mesh vertices to the space of the bone.</span></span> <span data-ttu-id="428c3-112">En cas de concaténation à la transformation du segment, les coordonnées de l’espace universel du maillage sont affectées par le segment.</span><span class="sxs-lookup"><span data-stu-id="428c3-112">When concatenated to the bone's transform, this provides the world space coordinates of the mesh as affected by the bone.</span></span> <span data-ttu-id="428c3-113">Consultez [**Matrix4x4**](matrix4x4.md).</span><span class="sxs-lookup"><span data-stu-id="428c3-113">See [**Matrix4x4**](matrix4x4.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="428c3-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="428c3-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="428c3-115">Modèles</span><span class="sxs-lookup"><span data-stu-id="428c3-115">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



