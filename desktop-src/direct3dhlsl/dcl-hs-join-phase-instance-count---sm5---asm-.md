---
title: dcl_hs_join_phase_instance_count (SM5-ASM)
description: Déclarez le nombre d’instances de la phase de jointure dans une phase de jointure de nuanceur de coque.
ms.assetid: 9951B849-0537-4D08-9ADE-8CF6FF51A193
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34c3acc7074170ab4561a54e67668698d58b7ac1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381241"
---
# <a name="dcl_hs_join_phase_instance_count-sm5---asm"></a><span data-ttu-id="4340d-103">\_nombre d' \_ instances de la phase de jointure DCL HS \_ \_ \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="4340d-103">dcl\_hs\_join\_phase\_instance\_count (sm5 - asm)</span></span>

<span data-ttu-id="4340d-104">Déclarez le nombre d’instances de la phase de jointure dans une phase de jointure de nuanceur de coque.</span><span class="sxs-lookup"><span data-stu-id="4340d-104">Declare the join phase instance count in a hull shader join phase.</span></span>



| <span data-ttu-id="4340d-105">\_nombre d' \_ instances de la phase de jointure DCL HS \_ \_ \_ {1... Max 32-bit uint}</span><span class="sxs-lookup"><span data-stu-id="4340d-105">dcl\_hs\_join\_phase\_instance\_count {1... max 32-bit UINT}</span></span> |
|--------------------------------------------------------------|



 



| <span data-ttu-id="4340d-106">Élément</span><span class="sxs-lookup"><span data-stu-id="4340d-106">Item</span></span>                                                   | <span data-ttu-id="4340d-107">Description</span><span class="sxs-lookup"><span data-stu-id="4340d-107">Description</span></span>                           |
|--------------------------------------------------------|---------------------------------------|
| <span data-ttu-id="4340d-108"><span id="N"></span><span id="n"></span>*N*</span><span class="sxs-lookup"><span data-stu-id="4340d-108"><span id="N"></span><span id="n"></span>*N*</span></span><br/> | <span data-ttu-id="4340d-109">\[dans \] le nombre d’instances.</span><span class="sxs-lookup"><span data-stu-id="4340d-109">\[in\] The instance count.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4340d-110">Notes</span><span class="sxs-lookup"><span data-stu-id="4340d-110">Remarks</span></span>

<span data-ttu-id="4340d-111">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="4340d-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="4340d-112">Sommet</span><span class="sxs-lookup"><span data-stu-id="4340d-112">Vertex</span></span> | <span data-ttu-id="4340d-113">Forme</span><span class="sxs-lookup"><span data-stu-id="4340d-113">Hull</span></span> | <span data-ttu-id="4340d-114">Domain</span><span class="sxs-lookup"><span data-stu-id="4340d-114">Domain</span></span> | <span data-ttu-id="4340d-115">Géométrie</span><span class="sxs-lookup"><span data-stu-id="4340d-115">Geometry</span></span> | <span data-ttu-id="4340d-116">Pixel</span><span class="sxs-lookup"><span data-stu-id="4340d-116">Pixel</span></span> | <span data-ttu-id="4340d-117">Compute</span><span class="sxs-lookup"><span data-stu-id="4340d-117">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="4340d-118">X</span><span class="sxs-lookup"><span data-stu-id="4340d-118">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4340d-119">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="4340d-119">Minimum Shader Model</span></span>

<span data-ttu-id="4340d-120">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="4340d-120">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="4340d-121">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="4340d-121">Shader Model</span></span>                                              | <span data-ttu-id="4340d-122">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="4340d-122">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4340d-123">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="4340d-123">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4340d-124">Oui</span><span class="sxs-lookup"><span data-stu-id="4340d-124">yes</span></span>       |
| [<span data-ttu-id="4340d-125">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="4340d-125">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4340d-126">non</span><span class="sxs-lookup"><span data-stu-id="4340d-126">no</span></span>        |
| [<span data-ttu-id="4340d-127">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="4340d-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4340d-128">non</span><span class="sxs-lookup"><span data-stu-id="4340d-128">no</span></span>        |
| [<span data-ttu-id="4340d-129">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4340d-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4340d-130">non</span><span class="sxs-lookup"><span data-stu-id="4340d-130">no</span></span>        |
| [<span data-ttu-id="4340d-131">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4340d-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4340d-132">non</span><span class="sxs-lookup"><span data-stu-id="4340d-132">no</span></span>        |
| [<span data-ttu-id="4340d-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4340d-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4340d-134">non</span><span class="sxs-lookup"><span data-stu-id="4340d-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4340d-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4340d-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4340d-136">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4340d-136">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





