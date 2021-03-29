---
title: deriv_rty_fine (SM5-ASM)
description: Calcule le taux de modification des composants. | deriv_rty_fine (SM5-ASM)
ms.assetid: 7C5769A6-443C-4208-BD09-3DF3C5902624
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f0274fd04ae88ee412c95947691628754ba197
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991968"
---
# <a name="deriv_rty_fine-sm5---asm"></a><span data-ttu-id="d5464-104">Deriv \_ propriété \_ fine (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="d5464-104">deriv\_rty\_fine (sm5 - asm)</span></span>

<span data-ttu-id="d5464-105">Calcule le taux de modification des composants.</span><span class="sxs-lookup"><span data-stu-id="d5464-105">Computes the rate of change of components.</span></span>



| <span data-ttu-id="d5464-106">Deriv \_ propriété \_ fine \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="d5464-106">deriv\_rty\_fine\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\],</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="d5464-107">Élément</span><span class="sxs-lookup"><span data-stu-id="d5464-107">Item</span></span>                                                            | <span data-ttu-id="d5464-108">Description</span><span class="sxs-lookup"><span data-stu-id="d5464-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="d5464-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="d5464-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="d5464-110">\[dans \] l’adresse des résultats de l’opération.</span><span class="sxs-lookup"><span data-stu-id="d5464-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="d5464-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="d5464-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="d5464-112">\[dans \] les composants de l’opération.</span><span class="sxs-lookup"><span data-stu-id="d5464-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="d5464-113">Notes</span><span class="sxs-lookup"><span data-stu-id="d5464-113">Remarks</span></span>

<span data-ttu-id="d5464-114">Pour plus d’informations, consultez [Deriv \_ RTX \_ fine.](deriv-rtx-fine--sm5---asm-.md)</span><span class="sxs-lookup"><span data-stu-id="d5464-114">For more information, see [deriv\_rtx\_fine.](deriv-rtx-fine--sm5---asm-.md)</span></span>

<span data-ttu-id="d5464-115">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="d5464-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d5464-116">Sommet</span><span class="sxs-lookup"><span data-stu-id="d5464-116">Vertex</span></span> | <span data-ttu-id="d5464-117">Forme</span><span class="sxs-lookup"><span data-stu-id="d5464-117">Hull</span></span> | <span data-ttu-id="d5464-118">Domain</span><span class="sxs-lookup"><span data-stu-id="d5464-118">Domain</span></span> | <span data-ttu-id="d5464-119">Géométrie</span><span class="sxs-lookup"><span data-stu-id="d5464-119">Geometry</span></span> | <span data-ttu-id="d5464-120">Pixel</span><span class="sxs-lookup"><span data-stu-id="d5464-120">Pixel</span></span> | <span data-ttu-id="d5464-121">Compute</span><span class="sxs-lookup"><span data-stu-id="d5464-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="d5464-122">X</span><span class="sxs-lookup"><span data-stu-id="d5464-122">X</span></span>     |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d5464-123">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="d5464-123">Minimum Shader Model</span></span>

<span data-ttu-id="d5464-124">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="d5464-124">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="d5464-125">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="d5464-125">Shader Model</span></span>                                              | <span data-ttu-id="d5464-126">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="d5464-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d5464-127">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="d5464-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d5464-128">Oui</span><span class="sxs-lookup"><span data-stu-id="d5464-128">yes</span></span>       |
| [<span data-ttu-id="d5464-129">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="d5464-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d5464-130">non</span><span class="sxs-lookup"><span data-stu-id="d5464-130">no</span></span>        |
| [<span data-ttu-id="d5464-131">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="d5464-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d5464-132">non</span><span class="sxs-lookup"><span data-stu-id="d5464-132">no</span></span>        |
| [<span data-ttu-id="d5464-133">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d5464-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d5464-134">non</span><span class="sxs-lookup"><span data-stu-id="d5464-134">no</span></span>        |
| [<span data-ttu-id="d5464-135">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d5464-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d5464-136">non</span><span class="sxs-lookup"><span data-stu-id="d5464-136">no</span></span>        |
| [<span data-ttu-id="d5464-137">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d5464-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d5464-138">non</span><span class="sxs-lookup"><span data-stu-id="d5464-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d5464-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d5464-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5464-140">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d5464-140">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





