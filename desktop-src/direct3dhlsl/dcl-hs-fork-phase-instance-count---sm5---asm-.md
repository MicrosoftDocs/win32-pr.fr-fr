---
title: dcl_hs_fork_phase_instance_count (SM5-ASM)
description: Déclarez le nombre d’instances de la phase fourche dans une phase de bifurcation de nuanceur de coque.
ms.assetid: E38C48BB-3439-4F63-8DF8-21CF562CF5E6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3459b43c22f60699445f3ef05e5323e268eeb71
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381240"
---
# <a name="dcl_hs_fork_phase_instance_count-sm5---asm"></a><span data-ttu-id="44cb4-103">\_nombre d' \_ instances de la phase de duplication DCL HS \_ \_ \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="44cb4-103">dcl\_hs\_fork\_phase\_instance\_count (sm5 - asm)</span></span>

<span data-ttu-id="44cb4-104">Déclarez le nombre d’instances de la phase fourche dans une phase de bifurcation de nuanceur de coque.</span><span class="sxs-lookup"><span data-stu-id="44cb4-104">Declare the fork phase instance count in a hull shader fork phase.</span></span>



| <span data-ttu-id="44cb4-105">\_nombre d' \_ instances de la phase de duplication DCL HS \_ \_ \_ {1... Max 32-bit uint}</span><span class="sxs-lookup"><span data-stu-id="44cb4-105">dcl\_hs\_fork\_phase\_instance\_count {1...max 32-bit UINT}</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="44cb4-106">Élément</span><span class="sxs-lookup"><span data-stu-id="44cb4-106">Item</span></span>                                                   | <span data-ttu-id="44cb4-107">Description</span><span class="sxs-lookup"><span data-stu-id="44cb4-107">Description</span></span>                           |
|--------------------------------------------------------|---------------------------------------|
| <span data-ttu-id="44cb4-108"><span id="N"></span><span id="n"></span>*N*</span><span class="sxs-lookup"><span data-stu-id="44cb4-108"><span id="N"></span><span id="n"></span>*N*</span></span><br/> | <span data-ttu-id="44cb4-109">\[dans \] le nombre d’instances.</span><span class="sxs-lookup"><span data-stu-id="44cb4-109">\[in\] The instance count.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="44cb4-110">Notes</span><span class="sxs-lookup"><span data-stu-id="44cb4-110">Remarks</span></span>

<span data-ttu-id="44cb4-111">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="44cb4-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="44cb4-112">Sommet</span><span class="sxs-lookup"><span data-stu-id="44cb4-112">Vertex</span></span> | <span data-ttu-id="44cb4-113">Forme</span><span class="sxs-lookup"><span data-stu-id="44cb4-113">Hull</span></span> | <span data-ttu-id="44cb4-114">Domain</span><span class="sxs-lookup"><span data-stu-id="44cb4-114">Domain</span></span> | <span data-ttu-id="44cb4-115">Géométrie</span><span class="sxs-lookup"><span data-stu-id="44cb4-115">Geometry</span></span> | <span data-ttu-id="44cb4-116">Pixel</span><span class="sxs-lookup"><span data-stu-id="44cb4-116">Pixel</span></span> | <span data-ttu-id="44cb4-117">Compute</span><span class="sxs-lookup"><span data-stu-id="44cb4-117">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="44cb4-118">X</span><span class="sxs-lookup"><span data-stu-id="44cb4-118">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="44cb4-119">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="44cb4-119">Minimum Shader Model</span></span>

<span data-ttu-id="44cb4-120">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="44cb4-120">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="44cb4-121">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="44cb4-121">Shader Model</span></span>                                              | <span data-ttu-id="44cb4-122">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="44cb4-122">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="44cb4-123">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="44cb4-123">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="44cb4-124">Oui</span><span class="sxs-lookup"><span data-stu-id="44cb4-124">yes</span></span>       |
| [<span data-ttu-id="44cb4-125">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="44cb4-125">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="44cb4-126">non</span><span class="sxs-lookup"><span data-stu-id="44cb4-126">no</span></span>        |
| [<span data-ttu-id="44cb4-127">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="44cb4-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="44cb4-128">non</span><span class="sxs-lookup"><span data-stu-id="44cb4-128">no</span></span>        |
| [<span data-ttu-id="44cb4-129">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="44cb4-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="44cb4-130">non</span><span class="sxs-lookup"><span data-stu-id="44cb4-130">no</span></span>        |
| [<span data-ttu-id="44cb4-131">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="44cb4-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="44cb4-132">non</span><span class="sxs-lookup"><span data-stu-id="44cb4-132">no</span></span>        |
| [<span data-ttu-id="44cb4-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="44cb4-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="44cb4-134">non</span><span class="sxs-lookup"><span data-stu-id="44cb4-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="44cb4-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="44cb4-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44cb4-136">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="44cb4-136">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





