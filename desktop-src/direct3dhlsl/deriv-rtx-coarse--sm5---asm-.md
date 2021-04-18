---
title: deriv_rtx_coarse (SM5-ASM)
description: Calcule le taux de modification des composants. | deriv_rtx_coarse (SM5-ASM)
ms.assetid: 57743BB2-251C-4EA7-BDA9-70B2ECEE3B3F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2355b6db6aef9e85959d6359053fea76b48af0a5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991921"
---
# <a name="deriv_rtx_coarse-sm5---asm"></a><span data-ttu-id="9b819-104">Deriv \_ RTX \_ grossiste (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="9b819-104">deriv\_rtx\_coarse (sm5 - asm)</span></span>

<span data-ttu-id="9b819-105">Calcule le taux de modification des composants.</span><span class="sxs-lookup"><span data-stu-id="9b819-105">Computes the rate of change of components.</span></span>



| <span data-ttu-id="9b819-106">Deriv \_ RTX \_ grossiste \[ \_ \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="9b819-106">deriv\_rtx\_coarse\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\],</span></span> |
|----------------------------------------------------------------------------|



 



| <span data-ttu-id="9b819-107">Élément</span><span class="sxs-lookup"><span data-stu-id="9b819-107">Item</span></span>                                                            | <span data-ttu-id="9b819-108">Description</span><span class="sxs-lookup"><span data-stu-id="9b819-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="9b819-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="9b819-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="9b819-110">\[dans \] l’adresse des résultats de l’opération.</span><span class="sxs-lookup"><span data-stu-id="9b819-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="9b819-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="9b819-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="9b819-112">\[dans \] les composants de l’opération.</span><span class="sxs-lookup"><span data-stu-id="9b819-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="9b819-113">Notes</span><span class="sxs-lookup"><span data-stu-id="9b819-113">Remarks</span></span>

<span data-ttu-id="9b819-114">Cette instruction calcule le taux de modification du contenu de chaque composant float32 de *src0* (Swizzle), en ce qui concerne la direction renderTarget x (RTX) ou renderTarget y (voir [Deriv \_ propriété \_ grossiste](deriv-rty-coarse--sm5---asm-.md)).</span><span class="sxs-lookup"><span data-stu-id="9b819-114">This instruction computes the rate of change of contents of each float32 component of *src0* (post-swizzle), with regard to RenderTarget x direction (rtx) or RenderTarget y direction (see [deriv\_rty\_coarse](deriv-rty-coarse--sm5---asm-.md)).</span></span> <span data-ttu-id="9b819-115">Une seule paire dérivée x, y est calculée pour chaque tampon 2x2 de pixels.</span><span class="sxs-lookup"><span data-stu-id="9b819-115">Only a single x,y derivative pair is computed for each 2x2 stamp of pixels.</span></span>

<span data-ttu-id="9b819-116">Les données de l’appel de nuanceur de pixels actuel peuvent ou non participer au calcul de la dérivée demandée, car le dérivé est calculé une seule fois par 2x2 Quad.</span><span class="sxs-lookup"><span data-stu-id="9b819-116">The data in the current pixel shader invocation may or may not participate in the calculation of the requested derivative, because the derivative will be calculated only once per 2x2 quad.</span></span> <span data-ttu-id="9b819-117">Par exemple, la dérivée x peut être un Delta à partir de la ligne supérieure de pixels, tandis que la direction y ([Deriv \_ propriété \_ grossiste](deriv-rty-coarse--sm5---asm-.md)) peut être un delta de la colonne de gauche de pixels.</span><span class="sxs-lookup"><span data-stu-id="9b819-117">For example, the x derivative could be a delta from the top row of pixels, and the y direction ([deriv\_rty\_coarse](deriv-rty-coarse--sm5---asm-.md)) could be a delta from the left column of pixels.</span></span> <span data-ttu-id="9b819-118">Le calcul exact est effectué par le fournisseur de matériel.</span><span class="sxs-lookup"><span data-stu-id="9b819-118">The exact calculation is up to the hardware vendor.</span></span> <span data-ttu-id="9b819-119">Il n’y a pas non plus de spécification indiquant comment les quadruples 2x2 sont alignés ou en mosaïque sur une primitive.</span><span class="sxs-lookup"><span data-stu-id="9b819-119">There is also no specification dictating how the 2x2 quads will be aligned or tiled over a primitive.</span></span>

<span data-ttu-id="9b819-120">Les dérivés sont calculés à un niveau grossier, une fois par Quad pixel Quad.</span><span class="sxs-lookup"><span data-stu-id="9b819-120">Derivatives are calculated at a coarse level, once per 2x2 pixel quad.</span></span> <span data-ttu-id="9b819-121">Cette instruction et [Deriv \_ propriété \_ grossiste](deriv-rty-coarse--sm5---asm-.md) sont des alternatives à [Deriv \_ RTX \_ fine](deriv-rtx-fine--sm5---asm-.md) et [Deriv \_ propriété \_ ](deriv-rty-fine--sm5---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="9b819-121">This instruction and [deriv\_rty\_coarse](deriv-rty-coarse--sm5---asm-.md) are alternatives to [deriv\_rtx\_fine](deriv-rtx-fine--sm5---asm-.md) and [deriv\_rty\_fine](deriv-rty-fine--sm5---asm-.md).</span></span> <span data-ttu-id="9b819-122">Ces \_ \_ instructions dérivées grossières et fine remplacent **Deriv \_ rtxderiv \_ propriété** des modèles de nuanceur précédents.</span><span class="sxs-lookup"><span data-stu-id="9b819-122">These \_coarse and \_fine derivative instructions are a replacement for **deriv\_rtxderiv\_rty** from previous shader models .</span></span>

<span data-ttu-id="9b819-123">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="9b819-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9b819-124">Sommet</span><span class="sxs-lookup"><span data-stu-id="9b819-124">Vertex</span></span> | <span data-ttu-id="9b819-125">Forme</span><span class="sxs-lookup"><span data-stu-id="9b819-125">Hull</span></span> | <span data-ttu-id="9b819-126">Domain</span><span class="sxs-lookup"><span data-stu-id="9b819-126">Domain</span></span> | <span data-ttu-id="9b819-127">Géométrie</span><span class="sxs-lookup"><span data-stu-id="9b819-127">Geometry</span></span> | <span data-ttu-id="9b819-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="9b819-128">Pixel</span></span> | <span data-ttu-id="9b819-129">Compute</span><span class="sxs-lookup"><span data-stu-id="9b819-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="9b819-130">X</span><span class="sxs-lookup"><span data-stu-id="9b819-130">X</span></span>     |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9b819-131">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="9b819-131">Minimum Shader Model</span></span>

<span data-ttu-id="9b819-132">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="9b819-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="9b819-133">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="9b819-133">Shader Model</span></span>                                              | <span data-ttu-id="9b819-134">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="9b819-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9b819-135">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="9b819-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9b819-136">Oui</span><span class="sxs-lookup"><span data-stu-id="9b819-136">yes</span></span>       |
| [<span data-ttu-id="9b819-137">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="9b819-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9b819-138">non</span><span class="sxs-lookup"><span data-stu-id="9b819-138">no</span></span>        |
| [<span data-ttu-id="9b819-139">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="9b819-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9b819-140">non</span><span class="sxs-lookup"><span data-stu-id="9b819-140">no</span></span>        |
| [<span data-ttu-id="9b819-141">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9b819-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9b819-142">non</span><span class="sxs-lookup"><span data-stu-id="9b819-142">no</span></span>        |
| [<span data-ttu-id="9b819-143">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9b819-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9b819-144">non</span><span class="sxs-lookup"><span data-stu-id="9b819-144">no</span></span>        |
| [<span data-ttu-id="9b819-145">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9b819-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9b819-146">non</span><span class="sxs-lookup"><span data-stu-id="9b819-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9b819-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9b819-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b819-148">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9b819-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





