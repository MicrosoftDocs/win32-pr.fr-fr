---
title: deriv_rtx_fine (SM5-ASM)
description: Calcule le taux de modification des composants. | deriv_rtx_fine (SM5-ASM)
ms.assetid: 5752C85B-2965-489C-BF27-968FAF5EAA52
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73061e3220704cf2c19e28b4d6d434fda43fb941
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992028"
---
# <a name="deriv_rtx_fine-sm5---asm"></a><span data-ttu-id="68dcf-104">Deriv \_ RTX \_ fine (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="68dcf-104">deriv\_rtx\_fine (sm5 - asm)</span></span>

<span data-ttu-id="68dcf-105">Calcule le taux de modification des composants.</span><span class="sxs-lookup"><span data-stu-id="68dcf-105">Computes the rate of change of components.</span></span>



| <span data-ttu-id="68dcf-106">Deriv \_ RTX \_ fine \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="68dcf-106">deriv\_rtx\_fine\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\],</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="68dcf-107">Élément</span><span class="sxs-lookup"><span data-stu-id="68dcf-107">Item</span></span>                                                            | <span data-ttu-id="68dcf-108">Description</span><span class="sxs-lookup"><span data-stu-id="68dcf-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="68dcf-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="68dcf-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="68dcf-110">\[dans \] l’adresse des résultats de l’opération.</span><span class="sxs-lookup"><span data-stu-id="68dcf-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="68dcf-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="68dcf-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="68dcf-112">\[dans \] les composants de l’opération.</span><span class="sxs-lookup"><span data-stu-id="68dcf-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="68dcf-113">Notes</span><span class="sxs-lookup"><span data-stu-id="68dcf-113">Remarks</span></span>

<span data-ttu-id="68dcf-114">Cette instruction calcule le taux de modification du contenu de chaque composant float32 de *src0* (Swizzle), en ce qui concerne la direction renderTarget x (RTX) ou l’axe des renderTarget y (consultez [Deriv \_ propriété \_ fine](deriv-rty-fine--sm5---asm-.md)).</span><span class="sxs-lookup"><span data-stu-id="68dcf-114">This instruction computes the rate of change of contents of each float32 component of *src0* (post-swizzle), with regard to RenderTarget x direction (rtx) or RenderTarget y direction (see [deriv\_rty\_fine](deriv-rty-fine--sm5---asm-.md)).</span></span> <span data-ttu-id="68dcf-115">Chaque pixel dans le tampon 2x2 obtient une paire unique de calculs de dérivés x/y</span><span class="sxs-lookup"><span data-stu-id="68dcf-115">Each pixel in the 2x2 stamp gets a unique pair of x/y derivative calculations</span></span>

<span data-ttu-id="68dcf-116">Les données de l’appel de nuanceur de pixels actuel participent toujours au calcul de la dérivée demandée.</span><span class="sxs-lookup"><span data-stu-id="68dcf-116">The data in the current pixel shader invocation always participates in the calculation of the requested derivative.</span></span> <span data-ttu-id="68dcf-117">Dans le quadruple pixel Quad, le pixel actuel se trouve dans, la dérivée x est le delta de la ligne de 2 pixels, y compris le pixel actuel.</span><span class="sxs-lookup"><span data-stu-id="68dcf-117">In the 2x2 pixel quad the current pixel falls within, the x derivative is the delta of the row of 2 pixels including the current pixel.</span></span> <span data-ttu-id="68dcf-118">Le dérivé de y est le delta de la colonne de 2 pixels, y compris le pixel actuel.</span><span class="sxs-lookup"><span data-stu-id="68dcf-118">The y derivative is the delta of the column of 2 pixels including the current pixel.</span></span> <span data-ttu-id="68dcf-119">Il n’existe aucune spécification qui dicte la manière dont les quadruples 2x2 sont alignés ou en mosaïque sur une primitive.</span><span class="sxs-lookup"><span data-stu-id="68dcf-119">There is no specification dictating how the 2x2 quads will be aligned or tiled over a primitive.</span></span>

<span data-ttu-id="68dcf-120">Les dérivés sont calculés à un niveau précis (calcul unique de la paire de dérivés x/y pour chaque pixel dans un quadruple quad).</span><span class="sxs-lookup"><span data-stu-id="68dcf-120">Derivatives are calculated at a fine level (unique calculation of the x/y derivative pair for each pixel in a 2x2 quad).</span></span> <span data-ttu-id="68dcf-121">Cette instruction et [Deriv \_ propriété \_ fine](deriv-rty-fine--sm5---asm-.md) sont des alternatives à [Deriv \_ RTX \_ grossiste](deriv-rtx-coarse--sm5---asm-.md) et [Deriv \_ propriété \_ grossiste](deriv-rty-coarse--sm5---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="68dcf-121">This instruction and [deriv\_rty\_fine](deriv-rty-fine--sm5---asm-.md) are alternatives to [deriv\_rtx\_coarse](deriv-rtx-coarse--sm5---asm-.md) and [deriv\_rty\_coarse](deriv-rty-coarse--sm5---asm-.md).</span></span> <span data-ttu-id="68dcf-122">Ces \_ \_ instructions dérivées grossières et fine remplacent **Deriv \_ RTX** ces \_ instructions de gros grain et de \_ dérivées fine remplacent les **Deriv \_ RTX** et **Deriv \_ propriété** des modèles de nuanceur précédents.</span><span class="sxs-lookup"><span data-stu-id="68dcf-122">These \_coarse and \_fine derivative instructions are a replacement for **deriv\_rtx** These \_coarse and \_fine derivative instructions are a replacement for **deriv\_rtx** and **deriv\_rty** from previous shader models.</span></span>

<span data-ttu-id="68dcf-123">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="68dcf-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="68dcf-124">Sommet</span><span class="sxs-lookup"><span data-stu-id="68dcf-124">Vertex</span></span> | <span data-ttu-id="68dcf-125">Forme</span><span class="sxs-lookup"><span data-stu-id="68dcf-125">Hull</span></span> | <span data-ttu-id="68dcf-126">Domain</span><span class="sxs-lookup"><span data-stu-id="68dcf-126">Domain</span></span> | <span data-ttu-id="68dcf-127">Géométrie</span><span class="sxs-lookup"><span data-stu-id="68dcf-127">Geometry</span></span> | <span data-ttu-id="68dcf-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="68dcf-128">Pixel</span></span> | <span data-ttu-id="68dcf-129">Compute</span><span class="sxs-lookup"><span data-stu-id="68dcf-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="68dcf-130">X</span><span class="sxs-lookup"><span data-stu-id="68dcf-130">X</span></span>     |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="68dcf-131">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="68dcf-131">Minimum Shader Model</span></span>

<span data-ttu-id="68dcf-132">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="68dcf-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="68dcf-133">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="68dcf-133">Shader Model</span></span>                                              | <span data-ttu-id="68dcf-134">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="68dcf-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="68dcf-135">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="68dcf-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="68dcf-136">Oui</span><span class="sxs-lookup"><span data-stu-id="68dcf-136">yes</span></span>       |
| [<span data-ttu-id="68dcf-137">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="68dcf-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="68dcf-138">non</span><span class="sxs-lookup"><span data-stu-id="68dcf-138">no</span></span>        |
| [<span data-ttu-id="68dcf-139">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="68dcf-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="68dcf-140">non</span><span class="sxs-lookup"><span data-stu-id="68dcf-140">no</span></span>        |
| [<span data-ttu-id="68dcf-141">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="68dcf-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="68dcf-142">non</span><span class="sxs-lookup"><span data-stu-id="68dcf-142">no</span></span>        |
| [<span data-ttu-id="68dcf-143">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="68dcf-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="68dcf-144">non</span><span class="sxs-lookup"><span data-stu-id="68dcf-144">no</span></span>        |
| [<span data-ttu-id="68dcf-145">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="68dcf-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="68dcf-146">non</span><span class="sxs-lookup"><span data-stu-id="68dcf-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="68dcf-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="68dcf-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68dcf-148">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="68dcf-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





