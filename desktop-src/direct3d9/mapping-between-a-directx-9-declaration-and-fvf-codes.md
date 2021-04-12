---
description: Ce tableau mappe les membres d’une déclaration D3DVERTEXELEMENT9 à un code de la Commission.
ms.assetid: be4357b5-5b92-44ca-9100-ec9473930446
title: Mappage entre une déclaration Direct3D et les codes de la Commission de la Commission (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4831af7b8c03ae4abd5ac2847351d2a6c921fb97
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109154"
---
# <a name="mapping-between-a-direct3d-declaration-and-fvf-codes-direct3d-9"></a><span data-ttu-id="cb7d8-103">Mappage entre une déclaration Direct3D et les codes de la Commission de la Commission (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="cb7d8-103">Mapping between a Direct3D Declaration and FVF Codes (Direct3D 9)</span></span>

<span data-ttu-id="cb7d8-104">Ce tableau mappe les membres d’une déclaration [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) à un code de la Commission.</span><span class="sxs-lookup"><span data-stu-id="cb7d8-104">This table maps members of a [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) declaration to a FVF code.</span></span>



| <span data-ttu-id="cb7d8-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="cb7d8-105">Data type</span></span>             | <span data-ttu-id="cb7d8-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="cb7d8-106">Usage</span></span>                      | <span data-ttu-id="cb7d8-107">Index d’utilisation</span><span class="sxs-lookup"><span data-stu-id="cb7d8-107">Usage index</span></span> | <span data-ttu-id="cb7d8-108">CLOS</span><span class="sxs-lookup"><span data-stu-id="cb7d8-108">FVF</span></span>                       |
|-----------------------|----------------------------|-------------|---------------------------|
| <span data-ttu-id="cb7d8-109">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="cb7d8-109">D3DDECLTYPE\_FLOAT3</span></span>   | <span data-ttu-id="cb7d8-110">\_Position D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="cb7d8-110">D3DDECLUSAGE\_POSITION</span></span>     | <span data-ttu-id="cb7d8-111">0</span><span class="sxs-lookup"><span data-stu-id="cb7d8-111">0</span></span>           | <span data-ttu-id="cb7d8-112">D3DFVF \_ xyz</span><span class="sxs-lookup"><span data-stu-id="cb7d8-112">D3DFVF\_XYZ</span></span>               |
| <span data-ttu-id="cb7d8-113">D3DDECLTYPE \_ float4</span><span class="sxs-lookup"><span data-stu-id="cb7d8-113">D3DDECLTYPE\_FLOAT4</span></span>   | <span data-ttu-id="cb7d8-114">\_Position D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="cb7d8-114">D3DDECLUSAGE\_POSITIONT</span></span>    | <span data-ttu-id="cb7d8-115">0</span><span class="sxs-lookup"><span data-stu-id="cb7d8-115">0</span></span>           | <span data-ttu-id="cb7d8-116">D3DFVF \_ XYZRHW</span><span class="sxs-lookup"><span data-stu-id="cb7d8-116">D3DFVF\_XYZRHW</span></span>            |
| <span data-ttu-id="cb7d8-117">D3DDECLTYPE \_ floatn</span><span class="sxs-lookup"><span data-stu-id="cb7d8-117">D3DDECLTYPE\_FLOATn</span></span>   | <span data-ttu-id="cb7d8-118">D3DDECLUSAGE \_ BLENDWEIGHT</span><span class="sxs-lookup"><span data-stu-id="cb7d8-118">D3DDECLUSAGE\_BLENDWEIGHT</span></span>  | <span data-ttu-id="cb7d8-119">0</span><span class="sxs-lookup"><span data-stu-id="cb7d8-119">0</span></span>           | <span data-ttu-id="cb7d8-120">D3DFVF \_ XYZBn</span><span class="sxs-lookup"><span data-stu-id="cb7d8-120">D3DFVF\_XYZBn</span></span>             |
| <span data-ttu-id="cb7d8-121">D3DDECLTYPE \_ UBYTE4</span><span class="sxs-lookup"><span data-stu-id="cb7d8-121">D3DDECLTYPE\_UBYTE4</span></span>   | <span data-ttu-id="cb7d8-122">D3DDECLUSAGE \_ BLENDINDICES</span><span class="sxs-lookup"><span data-stu-id="cb7d8-122">D3DDECLUSAGE\_BLENDINDICES</span></span> | <span data-ttu-id="cb7d8-123">0</span><span class="sxs-lookup"><span data-stu-id="cb7d8-123">0</span></span>           | <span data-ttu-id="cb7d8-124">D3DFVF \_ XYZB (nWeights + 1)</span><span class="sxs-lookup"><span data-stu-id="cb7d8-124">D3DFVF\_XYZB (nWeights+1)</span></span> |
| <span data-ttu-id="cb7d8-125">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="cb7d8-125">D3DDECLTYPE\_FLOAT3</span></span>   | <span data-ttu-id="cb7d8-126">D3DDECLUSAGE \_ normal</span><span class="sxs-lookup"><span data-stu-id="cb7d8-126">D3DDECLUSAGE\_NORMAL</span></span>       | <span data-ttu-id="cb7d8-127">0</span><span class="sxs-lookup"><span data-stu-id="cb7d8-127">0</span></span>           | <span data-ttu-id="cb7d8-128">D3DFVF \_ normal</span><span class="sxs-lookup"><span data-stu-id="cb7d8-128">D3DFVF\_NORMAL</span></span>            |
| <span data-ttu-id="cb7d8-129">D3DDECLTYPE \_ FLOAT1</span><span class="sxs-lookup"><span data-stu-id="cb7d8-129">D3DDECLTYPE\_FLOAT1</span></span>   | <span data-ttu-id="cb7d8-130">D3DDECLUSAGE \_ psize</span><span class="sxs-lookup"><span data-stu-id="cb7d8-130">D3DDECLUSAGE\_PSIZE</span></span>        | <span data-ttu-id="cb7d8-131">0</span><span class="sxs-lookup"><span data-stu-id="cb7d8-131">0</span></span>           | <span data-ttu-id="cb7d8-132">D3DFVF \_ psize</span><span class="sxs-lookup"><span data-stu-id="cb7d8-132">D3DFVF\_PSIZE</span></span>             |
| <span data-ttu-id="cb7d8-133">D3DDECLTYPE \_ D3DCOLOR</span><span class="sxs-lookup"><span data-stu-id="cb7d8-133">D3DDECLTYPE\_D3DCOLOR</span></span> | <span data-ttu-id="cb7d8-134">\_Couleur D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="cb7d8-134">D3DDECLUSAGE\_COLOR</span></span>        | <span data-ttu-id="cb7d8-135">0</span><span class="sxs-lookup"><span data-stu-id="cb7d8-135">0</span></span>           | <span data-ttu-id="cb7d8-136">\_Diffusion D3DFVF</span><span class="sxs-lookup"><span data-stu-id="cb7d8-136">D3DFVF\_DIFFUSE</span></span>           |
| <span data-ttu-id="cb7d8-137">D3DDECLTYPE \_ D3DCOLOR</span><span class="sxs-lookup"><span data-stu-id="cb7d8-137">D3DDECLTYPE\_D3DCOLOR</span></span> | <span data-ttu-id="cb7d8-138">\_Couleur D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="cb7d8-138">D3DDECLUSAGE\_COLOR</span></span>        | <span data-ttu-id="cb7d8-139">1</span><span class="sxs-lookup"><span data-stu-id="cb7d8-139">1</span></span>           | <span data-ttu-id="cb7d8-140">D3DFVF \_ spéculaire</span><span class="sxs-lookup"><span data-stu-id="cb7d8-140">D3DFVF\_SPECULAR</span></span>          |
| <span data-ttu-id="cb7d8-141">D3DDECLTYPE \_ Floater</span><span class="sxs-lookup"><span data-stu-id="cb7d8-141">D3DDECLTYPE\_FLOATm</span></span>   | <span data-ttu-id="cb7d8-142">D3DDECLUSAGE \_ texcoord</span><span class="sxs-lookup"><span data-stu-id="cb7d8-142">D3DDECLUSAGE\_TEXCOORD</span></span>     | <span data-ttu-id="cb7d8-143">n</span><span class="sxs-lookup"><span data-stu-id="cb7d8-143">n</span></span>           | <span data-ttu-id="cb7d8-144">D3DFVF \_ TEXCOORDSIZEm (n)</span><span class="sxs-lookup"><span data-stu-id="cb7d8-144">D3DFVF\_TEXCOORDSIZEm(n)</span></span>  |
| <span data-ttu-id="cb7d8-145">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="cb7d8-145">D3DDECLTYPE\_FLOAT3</span></span>   | <span data-ttu-id="cb7d8-146">\_Position D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="cb7d8-146">D3DDECLUSAGE\_POSITION</span></span>     | <span data-ttu-id="cb7d8-147">1</span><span class="sxs-lookup"><span data-stu-id="cb7d8-147">1</span></span>           | <span data-ttu-id="cb7d8-148">N/A</span><span class="sxs-lookup"><span data-stu-id="cb7d8-148">N/A</span></span>                       |
| <span data-ttu-id="cb7d8-149">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="cb7d8-149">D3DDECLTYPE\_FLOAT3</span></span>   | <span data-ttu-id="cb7d8-150">D3DDECLUSAGE \_ normal</span><span class="sxs-lookup"><span data-stu-id="cb7d8-150">D3DDECLUSAGE\_NORMAL</span></span>       | <span data-ttu-id="cb7d8-151">1</span><span class="sxs-lookup"><span data-stu-id="cb7d8-151">1</span></span>           | <span data-ttu-id="cb7d8-152">N/A</span><span class="sxs-lookup"><span data-stu-id="cb7d8-152">N/A</span></span>                       |



 

## <a name="related-topics"></a><span data-ttu-id="cb7d8-153">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cb7d8-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb7d8-154">Déclaration de vertex</span><span class="sxs-lookup"><span data-stu-id="cb7d8-154">Vertex Declaration</span></span>](vertex-declaration.md)
</dt> </dl>

 

 



