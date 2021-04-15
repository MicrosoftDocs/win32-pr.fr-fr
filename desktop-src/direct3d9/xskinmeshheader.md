---
description: Ce modèle est instancié par maillage uniquement dans les maillages qui contiennent des informations d’enveloppement exportées. L’objectif de ce modèle est de fournir des informations sur la nature des informations d’habillage qui ont été exportées.
ms.assetid: 95a4fa45-63d1-4931-9c91-b26807d2b043
title: XSkinMeshHeader
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 306f8c183086846fca020040af00b9ccef2665cc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392784"
---
# <a name="xskinmeshheader"></a><span data-ttu-id="96e01-104">XSkinMeshHeader</span><span class="sxs-lookup"><span data-stu-id="96e01-104">XSkinMeshHeader</span></span>

<span data-ttu-id="96e01-105">Ce modèle est instancié par maillage uniquement dans les maillages qui contiennent des informations d’enveloppement exportées.</span><span class="sxs-lookup"><span data-stu-id="96e01-105">This template is instantiated on a per-mesh basis only in meshes that contain exported skinning information.</span></span> <span data-ttu-id="96e01-106">L’objectif de ce modèle est de fournir des informations sur la nature des informations d’habillage qui ont été exportées.</span><span class="sxs-lookup"><span data-stu-id="96e01-106">The purpose of this template is to provide information about the nature of the skinning information that was exported.</span></span>

``` syntax
template XSkinMeshHeader 
{ 
    < 3CF169CE-FF7C-44ab-93C0-F78F62D172E2 >  
    WORD nMaxSkinWeightsPerVertex; 
    WORD nMaxSkinWeightsPerFace; 
    WORD nBones; 
}
```

<span data-ttu-id="96e01-107">Où :</span><span class="sxs-lookup"><span data-stu-id="96e01-107">Where:</span></span>

-   <span data-ttu-id="96e01-108">nMaxSkinWeightsPerVertex : nombre maximal de transformations qui affectent un vertex dans la maille.</span><span class="sxs-lookup"><span data-stu-id="96e01-108">nMaxSkinWeightsPerVertex - Maximum number of transforms that affect a vertex in the mesh.</span></span>
-   <span data-ttu-id="96e01-109">nMaxSkinWeightsPerFace : nombre maximal de transformations uniques qui affectent les trois sommets de n’importe quelle face.</span><span class="sxs-lookup"><span data-stu-id="96e01-109">nMaxSkinWeightsPerFace - Maximum number of unique transforms that affect the three vertices of any face.</span></span>
-   <span data-ttu-id="96e01-110">nBones : nombre d’os qui affectent des vertex dans ce maillage.</span><span class="sxs-lookup"><span data-stu-id="96e01-110">nBones - Number of bones that affect vertices in this mesh.</span></span>

## <a name="see-also"></a><span data-ttu-id="96e01-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96e01-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96e01-112">Modèles</span><span class="sxs-lookup"><span data-stu-id="96e01-112">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



