---
title: deriv_rty_coarse (SM5-ASM)
description: Calcule le taux de modification des composants. | deriv_rty_coarse (SM5-ASM)
ms.assetid: 1EBCC0B9-BD3E-46DD-AC17-F7167F892195
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df7fd539adf8587118a6bdfdcb5959925e6a97f8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992025"
---
# <a name="deriv_rty_coarse-sm5---asm"></a><span data-ttu-id="5384b-104">Deriv \_ propriété \_ grossiste (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="5384b-104">deriv\_rty\_coarse (sm5 - asm)</span></span>

<span data-ttu-id="5384b-105">Calcule le taux de modification des composants.</span><span class="sxs-lookup"><span data-stu-id="5384b-105">Computes the rate of change of components.</span></span>



| <span data-ttu-id="5384b-106">Deriv \_ propriété \_ grossiste \[ \_ \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="5384b-106">deriv\_rty\_coarse\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\],</span></span> |
|----------------------------------------------------------------------------|



 



| <span data-ttu-id="5384b-107">Élément</span><span class="sxs-lookup"><span data-stu-id="5384b-107">Item</span></span>                                                            | <span data-ttu-id="5384b-108">Description</span><span class="sxs-lookup"><span data-stu-id="5384b-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="5384b-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="5384b-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="5384b-110">\[dans \] l’adresse des résultats de l’opération.</span><span class="sxs-lookup"><span data-stu-id="5384b-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="5384b-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="5384b-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="5384b-112">\[dans \] les composants de l’opération.</span><span class="sxs-lookup"><span data-stu-id="5384b-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="5384b-113">Notes</span><span class="sxs-lookup"><span data-stu-id="5384b-113">Remarks</span></span>

<span data-ttu-id="5384b-114">Pour plus d’informations, consultez [Deriv \_ RTX \_ grossiste.](deriv-rtx-coarse--sm5---asm-.md)</span><span class="sxs-lookup"><span data-stu-id="5384b-114">For more information, see [deriv\_rtx\_coarse.](deriv-rtx-coarse--sm5---asm-.md)</span></span>

<span data-ttu-id="5384b-115">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="5384b-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="5384b-116">Sommet</span><span class="sxs-lookup"><span data-stu-id="5384b-116">Vertex</span></span> | <span data-ttu-id="5384b-117">Forme</span><span class="sxs-lookup"><span data-stu-id="5384b-117">Hull</span></span> | <span data-ttu-id="5384b-118">Domain</span><span class="sxs-lookup"><span data-stu-id="5384b-118">Domain</span></span> | <span data-ttu-id="5384b-119">Géométrie</span><span class="sxs-lookup"><span data-stu-id="5384b-119">Geometry</span></span> | <span data-ttu-id="5384b-120">Pixel</span><span class="sxs-lookup"><span data-stu-id="5384b-120">Pixel</span></span> | <span data-ttu-id="5384b-121">Compute</span><span class="sxs-lookup"><span data-stu-id="5384b-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="5384b-122">X</span><span class="sxs-lookup"><span data-stu-id="5384b-122">X</span></span>     |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5384b-123">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="5384b-123">Minimum Shader Model</span></span>

<span data-ttu-id="5384b-124">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="5384b-124">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="5384b-125">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="5384b-125">Shader Model</span></span>                                              | <span data-ttu-id="5384b-126">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="5384b-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5384b-127">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="5384b-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="5384b-128">Oui</span><span class="sxs-lookup"><span data-stu-id="5384b-128">yes</span></span>       |
| [<span data-ttu-id="5384b-129">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="5384b-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="5384b-130">non</span><span class="sxs-lookup"><span data-stu-id="5384b-130">no</span></span>        |
| [<span data-ttu-id="5384b-131">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="5384b-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5384b-132">non</span><span class="sxs-lookup"><span data-stu-id="5384b-132">no</span></span>        |
| [<span data-ttu-id="5384b-133">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5384b-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5384b-134">non</span><span class="sxs-lookup"><span data-stu-id="5384b-134">no</span></span>        |
| [<span data-ttu-id="5384b-135">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5384b-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5384b-136">non</span><span class="sxs-lookup"><span data-stu-id="5384b-136">no</span></span>        |
| [<span data-ttu-id="5384b-137">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5384b-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5384b-138">non</span><span class="sxs-lookup"><span data-stu-id="5384b-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5384b-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5384b-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5384b-140">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5384b-140">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





