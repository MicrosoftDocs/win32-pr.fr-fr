---
title: Mappage entre les déclarations D3D9 et D3D8
description: Ce tableau mappe les membres d’une déclaration D3DVERTEXELEMENT9 à une déclaration Direct3D 8.
ms.assetid: da02b2cd-5221-4d37-97d5-840df91e39a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5c52bd804907f201916386ef5fa5776a32a046b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745549"
---
# <a name="map-between-d3d9-and-d3d8-declarations"></a><span data-ttu-id="c4d65-103">Mappage entre les déclarations D3D9 et D3D8</span><span class="sxs-lookup"><span data-stu-id="c4d65-103">Map between D3D9 and D3D8 declarations</span></span>

<span data-ttu-id="c4d65-104">Ce tableau mappe les membres d’une déclaration [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) à une déclaration Direct3D 8.</span><span class="sxs-lookup"><span data-stu-id="c4d65-104">This table maps members of a [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) declaration to a Direct3D 8 declaration.</span></span>



| <span data-ttu-id="c4d65-105">Utilisation de Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="c4d65-105">Direct3D 9 Usage</span></span>           | <span data-ttu-id="c4d65-106">Index d’utilisation Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="c4d65-106">Direct3D 9 Usage index</span></span> | <span data-ttu-id="c4d65-107">Direct3D 8</span><span class="sxs-lookup"><span data-stu-id="c4d65-107">Direct3D 8</span></span>            |
|----------------------------|------------------------|-----------------------|
| <span data-ttu-id="c4d65-108">\_Position D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="c4d65-108">D3DDECLUSAGE\_POSITION</span></span>     | <span data-ttu-id="c4d65-109">0</span><span class="sxs-lookup"><span data-stu-id="c4d65-109">0</span></span>                      | <span data-ttu-id="c4d65-110">\_Position D3DVSDE</span><span class="sxs-lookup"><span data-stu-id="c4d65-110">D3DVSDE\_POSITION</span></span>     |
| <span data-ttu-id="c4d65-111">\_Position D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="c4d65-111">D3DDECLUSAGE\_POSITION</span></span>     | <span data-ttu-id="c4d65-112">1</span><span class="sxs-lookup"><span data-stu-id="c4d65-112">1</span></span>                      | <span data-ttu-id="c4d65-113">D3DVSDE \_ POSITION2</span><span class="sxs-lookup"><span data-stu-id="c4d65-113">D3DVSDE\_POSITION2</span></span>    |
| <span data-ttu-id="c4d65-114">D3DDECLUSAGE \_ normal</span><span class="sxs-lookup"><span data-stu-id="c4d65-114">D3DDECLUSAGE\_NORMAL</span></span>       | <span data-ttu-id="c4d65-115">0</span><span class="sxs-lookup"><span data-stu-id="c4d65-115">0</span></span>                      | <span data-ttu-id="c4d65-116">D3DVSDE \_ normal</span><span class="sxs-lookup"><span data-stu-id="c4d65-116">D3DVSDE\_NORMAL</span></span>       |
| <span data-ttu-id="c4d65-117">D3DDECLUSAGE \_ normal</span><span class="sxs-lookup"><span data-stu-id="c4d65-117">D3DDECLUSAGE\_NORMAL</span></span>       | <span data-ttu-id="c4d65-118">1</span><span class="sxs-lookup"><span data-stu-id="c4d65-118">1</span></span>                      | <span data-ttu-id="c4d65-119">D3DVSDE \_ NORMAL2</span><span class="sxs-lookup"><span data-stu-id="c4d65-119">D3DVSDE\_NORMAL2</span></span>      |
| <span data-ttu-id="c4d65-120">D3DDECLUSAGE \_ BLENDWEIGHT</span><span class="sxs-lookup"><span data-stu-id="c4d65-120">D3DDECLUSAGE\_BLENDWEIGHT</span></span>  | <span data-ttu-id="c4d65-121">0</span><span class="sxs-lookup"><span data-stu-id="c4d65-121">0</span></span>                      | <span data-ttu-id="c4d65-122">D3DVSDE \_ BLENDWEIGHT</span><span class="sxs-lookup"><span data-stu-id="c4d65-122">D3DVSDE\_BLENDWEIGHT</span></span>  |
| <span data-ttu-id="c4d65-123">D3DDECLUSAGE \_ BLENDINDICES</span><span class="sxs-lookup"><span data-stu-id="c4d65-123">D3DDECLUSAGE\_BLENDINDICES</span></span> | <span data-ttu-id="c4d65-124">0</span><span class="sxs-lookup"><span data-stu-id="c4d65-124">0</span></span>                      | <span data-ttu-id="c4d65-125">D3DVSDE \_ BLENDINDICES</span><span class="sxs-lookup"><span data-stu-id="c4d65-125">D3DVSDE\_BLENDINDICES</span></span> |
| <span data-ttu-id="c4d65-126">D3DDECLUSAGE \_ psize</span><span class="sxs-lookup"><span data-stu-id="c4d65-126">D3DDECLUSAGE\_PSIZE</span></span>        | <span data-ttu-id="c4d65-127">0</span><span class="sxs-lookup"><span data-stu-id="c4d65-127">0</span></span>                      | <span data-ttu-id="c4d65-128">D3DVSDE \_ psize</span><span class="sxs-lookup"><span data-stu-id="c4d65-128">D3DVSDE\_PSIZE</span></span>        |
| <span data-ttu-id="c4d65-129">\_Couleur D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="c4d65-129">D3DDECLUSAGE\_COLOR</span></span>        | <span data-ttu-id="c4d65-130">0</span><span class="sxs-lookup"><span data-stu-id="c4d65-130">0</span></span>                      | <span data-ttu-id="c4d65-131">\_Diffusion D3DVSDE</span><span class="sxs-lookup"><span data-stu-id="c4d65-131">D3DVSDE\_DIFFUSE</span></span>      |
| <span data-ttu-id="c4d65-132">\_Couleur D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="c4d65-132">D3DDECLUSAGE\_COLOR</span></span>        | <span data-ttu-id="c4d65-133">1</span><span class="sxs-lookup"><span data-stu-id="c4d65-133">1</span></span>                      | <span data-ttu-id="c4d65-134">D3DVSDE \_ spéculaire</span><span class="sxs-lookup"><span data-stu-id="c4d65-134">D3DVSDE\_SPECULAR</span></span>     |
| <span data-ttu-id="c4d65-135">D3DDECLUSAGE \_ texcoord</span><span class="sxs-lookup"><span data-stu-id="c4d65-135">D3DDECLUSAGE\_TEXCOORD</span></span>     | <span data-ttu-id="c4d65-136">n</span><span class="sxs-lookup"><span data-stu-id="c4d65-136">n</span></span>                      | <span data-ttu-id="c4d65-137">D3DVSDE \_ TEXCOORDn</span><span class="sxs-lookup"><span data-stu-id="c4d65-137">D3DVSDE\_TEXCOORDn</span></span>    |



 

<span data-ttu-id="c4d65-138">Quand une déclaration est utilisée avec le traitement du vertex matériel sur un pilote Direct3D 7, le runtime Direct3D le convertit en une Commission des prix à la une, avec les règles suivantes :</span><span class="sxs-lookup"><span data-stu-id="c4d65-138">When a declaration is used with hardware vertex processing on a Direct3D 7 driver, the Direct3D runtime converts it to a FVF with the following rules:</span></span>

-   <span data-ttu-id="c4d65-139">Seul Stream 0 doit être utilisé (évident à partir de l’extrémité MaxStreams).</span><span class="sxs-lookup"><span data-stu-id="c4d65-139">Only stream 0 should be used (evident from the MaxStreams cap).</span></span>
-   <span data-ttu-id="c4d65-140">L’ordre des éléments de vertex doit être le même que l’ordre des bits de la Commission.</span><span class="sxs-lookup"><span data-stu-id="c4d65-140">The order of vertex elements should be the same as order of FVF bits.</span></span>
-   <span data-ttu-id="c4d65-141">Les écarts dans les coordonnées de texture ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="c4d65-141">Gaps in texture coordinates are not allowed.</span></span>
-   <span data-ttu-id="c4d65-142">Tout élément vertex non décrit la table ne peut pas être convertie en une Commission valide pour tous les pilotes antérieurs à DirectX 8 et, par conséquent, ne peut pas être utilisée sur ces pilotes.</span><span class="sxs-lookup"><span data-stu-id="c4d65-142">Any vertex element not described the table cannot be converted into a valid FVF for all pre-DirectX 8 drivers and, hence, cannot be used on those drivers.</span></span>
-   <span data-ttu-id="c4d65-143">Seul D3DDECLTYPE \_ FLOAT2 est autorisé pour les éléments de vertex avec D3DDECLUSAGE \_ texcoord si l’appareil n’a pas défini l’une des deux \_ majuscules D3DPTEXTURECAPS Projected ou D3DPTEXTURECAPS carte cubique \_ .</span><span class="sxs-lookup"><span data-stu-id="c4d65-143">Only D3DDECLTYPE\_FLOAT2 is allowed for vertex elements with D3DDECLUSAGE\_TEXCOORD if device does not set either of the D3DPTEXTURECAPS\_PROJECTED or D3DPTEXTURECAPS\_CUBEMAP caps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4d65-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c4d65-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4d65-145">Déclaration de vertex</span><span class="sxs-lookup"><span data-stu-id="c4d65-145">Vertex Declaration</span></span>](vertex-declaration.md)
</dt> </dl>

 

 



