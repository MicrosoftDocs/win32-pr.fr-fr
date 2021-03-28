---
title: Fonctions intrinsèques du modèle de nuanceur 5
description: Le nuancier Model 5 implémente les fonctions intrinsèques à partir du nuanceur modèle 4 et versions antérieures (consultez fonctions intrinsèques (DirectX HLSL) pour obtenir une liste complète des fonctions prises en charge), ainsi que les nouvelles fonctions suivantes
ms.assetid: 6f91fb40-d6d0-459f-adf7-cff263d7d346
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0cd5976526f75b676a853ef7480d4e81e0e00a91
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381150"
---
# <a name="shader-model-5-intrinsic-functions"></a><span data-ttu-id="3380b-103">Fonctions intrinsèques du modèle de nuanceur 5</span><span class="sxs-lookup"><span data-stu-id="3380b-103">Shader Model 5 Intrinsic Functions</span></span>

<span data-ttu-id="3380b-104">Le Shader Model 5 implémente les fonctions intrinsèques à partir du nuanceur modèle 4 et versions antérieures (consultez [**fonctions intrinsèques (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md) pour obtenir une liste complète des fonctions prises en charge), ainsi que les nouvelles fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="3380b-104">Shader Model 5 implements the intrinsic functions from Shader Model 4 and below (see [**Intrinsic Functions (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md) for a complete list of supported functions), as well as the following new functions:</span></span>

-   [<span data-ttu-id="3380b-105">**AllMemoryBarrier**</span><span class="sxs-lookup"><span data-stu-id="3380b-105">**AllMemoryBarrier**</span></span>](allmemorybarrier.md)
-   [<span data-ttu-id="3380b-106">**AllMemoryBarrierWithGroupSync**</span><span class="sxs-lookup"><span data-stu-id="3380b-106">**AllMemoryBarrierWithGroupSync**</span></span>](allmemorybarrierwithgroupsync.md)
-   [<span data-ttu-id="3380b-107">**asdouble**</span><span class="sxs-lookup"><span data-stu-id="3380b-107">**asdouble**</span></span>](asdouble.md)
-   [<span data-ttu-id="3380b-108">**asuint**</span><span class="sxs-lookup"><span data-stu-id="3380b-108">**asuint**</span></span>](asuint.md)
-   [<span data-ttu-id="3380b-109">**countbits**</span><span class="sxs-lookup"><span data-stu-id="3380b-109">**countbits**</span></span>](countbits.md)
-   [<span data-ttu-id="3380b-110">**\_grossiste DDX**</span><span class="sxs-lookup"><span data-stu-id="3380b-110">**ddx\_coarse**</span></span>](ddx-coarse.md)
-   [<span data-ttu-id="3380b-111">**\_grossiste d’ddy**</span><span class="sxs-lookup"><span data-stu-id="3380b-111">**ddy\_coarse**</span></span>](ddy-coarse.md)
-   [<span data-ttu-id="3380b-112">**DeviceMemoryBarrier**</span><span class="sxs-lookup"><span data-stu-id="3380b-112">**DeviceMemoryBarrier**</span></span>](devicememorybarrier.md)
-   [<span data-ttu-id="3380b-113">**DeviceMemoryBarrierWithGroupSync**</span><span class="sxs-lookup"><span data-stu-id="3380b-113">**DeviceMemoryBarrierWithGroupSync**</span></span>](devicememorybarrierwithgroupsync.md)
-   [<span data-ttu-id="3380b-114">**EvaluateAttributeAtCentroid**</span><span class="sxs-lookup"><span data-stu-id="3380b-114">**EvaluateAttributeAtCentroid**</span></span>](evaluateattributeatcentroid.md)
-   [<span data-ttu-id="3380b-115">**EvaluateAttributeAtSample**</span><span class="sxs-lookup"><span data-stu-id="3380b-115">**EvaluateAttributeAtSample**</span></span>](evaluateattributeatsample.md)
-   [<span data-ttu-id="3380b-116">**f16tof32**</span><span class="sxs-lookup"><span data-stu-id="3380b-116">**f16tof32**</span></span>](f16tof32.md)
-   [<span data-ttu-id="3380b-117">**f32tof16**</span><span class="sxs-lookup"><span data-stu-id="3380b-117">**f32tof16**</span></span>](f32tof16.md)
-   [<span data-ttu-id="3380b-118">**firstbithigh**</span><span class="sxs-lookup"><span data-stu-id="3380b-118">**firstbithigh**</span></span>](firstbithigh.md)
-   [<span data-ttu-id="3380b-119">**firstbitlow**</span><span class="sxs-lookup"><span data-stu-id="3380b-119">**firstbitlow**</span></span>](firstbitlow.md)
-   [<span data-ttu-id="3380b-120">**FMA**</span><span class="sxs-lookup"><span data-stu-id="3380b-120">**fma**</span></span>](dx-graphics-hlsl-fma.md)
-   [<span data-ttu-id="3380b-121">**GroupMemoryBarrier**</span><span class="sxs-lookup"><span data-stu-id="3380b-121">**GroupMemoryBarrier**</span></span>](groupmemorybarrier.md)
-   [<span data-ttu-id="3380b-122">**GroupMemoryBarrierWithGroupSync**</span><span class="sxs-lookup"><span data-stu-id="3380b-122">**GroupMemoryBarrierWithGroupSync**</span></span>](groupmemorybarrierwithgroupsync.md)
-   [<span data-ttu-id="3380b-123">**InterlockedAdd**</span><span class="sxs-lookup"><span data-stu-id="3380b-123">**InterlockedAdd**</span></span>](interlockedadd.md)
-   [<span data-ttu-id="3380b-124">**InterlockedAnd**</span><span class="sxs-lookup"><span data-stu-id="3380b-124">**InterlockedAnd**</span></span>](interlockedand.md)
-   [<span data-ttu-id="3380b-125">**InterlockedCompareExchange**</span><span class="sxs-lookup"><span data-stu-id="3380b-125">**InterlockedCompareExchange**</span></span>](interlockedcompareexchange.md)
-   [<span data-ttu-id="3380b-126">**InterlockedCompareStore**</span><span class="sxs-lookup"><span data-stu-id="3380b-126">**InterlockedCompareStore**</span></span>](interlockedcomparestore.md)
-   [<span data-ttu-id="3380b-127">**Interlockedexchang**</span><span class="sxs-lookup"><span data-stu-id="3380b-127">**InterlockedExchange**</span></span>](interlockedexchange.md)
-   [<span data-ttu-id="3380b-128">**InterlockedMax**</span><span class="sxs-lookup"><span data-stu-id="3380b-128">**InterlockedMax**</span></span>](interlockedmax.md)
-   [<span data-ttu-id="3380b-129">**InterlockedMin**</span><span class="sxs-lookup"><span data-stu-id="3380b-129">**InterlockedMin**</span></span>](interlockedmin.md)
-   [<span data-ttu-id="3380b-130">**Interverrouiller**</span><span class="sxs-lookup"><span data-stu-id="3380b-130">**InterlockedOr**</span></span>](interlockedor.md)
-   [<span data-ttu-id="3380b-131">**InterlockedXor**</span><span class="sxs-lookup"><span data-stu-id="3380b-131">**InterlockedXor**</span></span>](interlockedxor.md)
-   [<span data-ttu-id="3380b-132">**msad4**</span><span class="sxs-lookup"><span data-stu-id="3380b-132">**msad4**</span></span>](dx-graphics-hlsl-msad4.md)
-   [<span data-ttu-id="3380b-133">**Process2DQuadTessFactorsAvg**</span><span class="sxs-lookup"><span data-stu-id="3380b-133">**Process2DQuadTessFactorsAvg**</span></span>](process2dquadtessfactorsavg.md)
-   [<span data-ttu-id="3380b-134">**Process2DQuadTessFactorsMax**</span><span class="sxs-lookup"><span data-stu-id="3380b-134">**Process2DQuadTessFactorsMax**</span></span>](process2dquadtessfactorsmax.md)
-   [<span data-ttu-id="3380b-135">**Process2DQuadTessFactorsMin**</span><span class="sxs-lookup"><span data-stu-id="3380b-135">**Process2DQuadTessFactorsMin**</span></span>](process2dquadtessfactorsmin.md)
-   [<span data-ttu-id="3380b-136">**ProcessIsolineTessFactors**</span><span class="sxs-lookup"><span data-stu-id="3380b-136">**ProcessIsolineTessFactors**</span></span>](processisolinetessfactors.md)
-   [<span data-ttu-id="3380b-137">**ProcessQuadTessFactorsAvg**</span><span class="sxs-lookup"><span data-stu-id="3380b-137">**ProcessQuadTessFactorsAvg**</span></span>](processquadtessfactorsavg.md)
-   [<span data-ttu-id="3380b-138">**ProcessQuadTessFactorsMax**</span><span class="sxs-lookup"><span data-stu-id="3380b-138">**ProcessQuadTessFactorsMax**</span></span>](processquadtessfactorsmax.md)
-   [<span data-ttu-id="3380b-139">**ProcessQuadTessFactorsMin**</span><span class="sxs-lookup"><span data-stu-id="3380b-139">**ProcessQuadTessFactorsMin**</span></span>](processquadtessfactorsmin.md)
-   [<span data-ttu-id="3380b-140">**ProcessTriTessFactorsAvg**</span><span class="sxs-lookup"><span data-stu-id="3380b-140">**ProcessTriTessFactorsAvg**</span></span>](processtritessfactorsavg.md)
-   [<span data-ttu-id="3380b-141">**ProcessTriTessFactorsMax**</span><span class="sxs-lookup"><span data-stu-id="3380b-141">**ProcessTriTessFactorsMax**</span></span>](processtritessfactorsmax.md)
-   [<span data-ttu-id="3380b-142">**ProcessTriTessFactorsMin**</span><span class="sxs-lookup"><span data-stu-id="3380b-142">**ProcessTriTessFactorsMin**</span></span>](processtritessfactorsmin.md)
-   [<span data-ttu-id="3380b-143">**rcp**</span><span class="sxs-lookup"><span data-stu-id="3380b-143">**rcp**</span></span>](rcp.md)
-   [<span data-ttu-id="3380b-144">**reversebits**</span><span class="sxs-lookup"><span data-stu-id="3380b-144">**reversebits**</span></span>](reversebits.md)

## <a name="related-topics"></a><span data-ttu-id="3380b-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3380b-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3380b-146">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="3380b-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




