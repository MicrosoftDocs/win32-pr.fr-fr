---
title: RCP (SM5-ASM)
description: Réciproque au niveau du composant.
ms.assetid: 499A14D6-36DB-4860-94D1-887D931E60D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa37499a981bae86333b071c2e96a37ccb8ac1a6
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998246"
---
# <a name="rcp-sm5---asm"></a><span data-ttu-id="862f3-103">RCP (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="862f3-103">rcp (sm5 - asm)</span></span>

<span data-ttu-id="862f3-104">Réciproque au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="862f3-104">Component-wise reciprocal.</span></span>



| <span data-ttu-id="862f3-105">RCP \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="862f3-105">rcp\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="862f3-106">Élément</span><span class="sxs-lookup"><span data-stu-id="862f3-106">Item</span></span>                                                            | <span data-ttu-id="862f3-107">Description</span><span class="sxs-lookup"><span data-stu-id="862f3-107">Description</span></span>                                                                         |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="862f3-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="862f3-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="862f3-109">\[dans \] l’adresse des résultats</span><span class="sxs-lookup"><span data-stu-id="862f3-109">\[in\] The address of the results</span></span><br/> <span data-ttu-id="862f3-110">*dest*  =  . **1.0 f**  /  *src0*.</span><span class="sxs-lookup"><span data-stu-id="862f3-110">*dest* = **1.0f** / *src0*.</span></span><br/> |
| <span data-ttu-id="862f3-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="862f3-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="862f3-112">\[dans \] le nombre à prendre la réciproque de.</span><span class="sxs-lookup"><span data-stu-id="862f3-112">\[in\] The number to take the reciprocal of.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="862f3-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="862f3-113">Remarks</span></span>

<span data-ttu-id="862f3-114">Utilisez cette instruction pour réduire la précision réciproque, indépendamment des exigences strictes pour la Division.</span><span class="sxs-lookup"><span data-stu-id="862f3-114">Use this instruction for reduced precision reciprocal, independent of the strict requirements for divide.</span></span>

<span data-ttu-id="862f3-115">L’erreur relative maximale est 2-21.</span><span class="sxs-lookup"><span data-stu-id="862f3-115">Maximum relative error is 2-21.</span></span> <span data-ttu-id="862f3-116">(La tolérance d’erreur correspond simplement à rsq)</span><span class="sxs-lookup"><span data-stu-id="862f3-116">(The error tolerance just matches rsq)</span></span>

<span data-ttu-id="862f3-117">Le tableau suivant présente les résultats obtenus lors de l’exécution de l’instruction avec différentes classes de nombres.</span><span class="sxs-lookup"><span data-stu-id="862f3-117">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>



| <span data-ttu-id="862f3-118">*src*</span><span class="sxs-lookup"><span data-stu-id="862f3-118">*src*</span></span>  | <span data-ttu-id="862f3-119">**-INF**</span><span class="sxs-lookup"><span data-stu-id="862f3-119">**-inf**</span></span> | <span data-ttu-id="862f3-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="862f3-120">**-F**</span></span> | <span data-ttu-id="862f3-121">**-dénorme**</span><span class="sxs-lookup"><span data-stu-id="862f3-121">**-denorm**</span></span> | <span data-ttu-id="862f3-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="862f3-122">**-0**</span></span> | <span data-ttu-id="862f3-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="862f3-123">**+0**</span></span> | <span data-ttu-id="862f3-124">**+ dénorme**</span><span class="sxs-lookup"><span data-stu-id="862f3-124">**+denorm**</span></span> | <span data-ttu-id="862f3-125">**+ F**</span><span class="sxs-lookup"><span data-stu-id="862f3-125">**+F**</span></span> | <span data-ttu-id="862f3-126">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="862f3-126">**+inf**</span></span> | <span data-ttu-id="862f3-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="862f3-127">**NaN**</span></span> |
|--------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="862f3-128">*dest*</span><span class="sxs-lookup"><span data-stu-id="862f3-128">*dest*</span></span> | <span data-ttu-id="862f3-129">-0</span><span class="sxs-lookup"><span data-stu-id="862f3-129">-0</span></span>       | <span data-ttu-id="862f3-130">-F</span><span class="sxs-lookup"><span data-stu-id="862f3-130">-F</span></span>     | <span data-ttu-id="862f3-131">-inf</span><span class="sxs-lookup"><span data-stu-id="862f3-131">-inf</span></span>        | <span data-ttu-id="862f3-132">-inf</span><span class="sxs-lookup"><span data-stu-id="862f3-132">-inf</span></span>   | <span data-ttu-id="862f3-133">+inf</span><span class="sxs-lookup"><span data-stu-id="862f3-133">+inf</span></span>   | <span data-ttu-id="862f3-134">+inf</span><span class="sxs-lookup"><span data-stu-id="862f3-134">+inf</span></span>        | <span data-ttu-id="862f3-135">+ F</span><span class="sxs-lookup"><span data-stu-id="862f3-135">+F</span></span>     | <span data-ttu-id="862f3-136">+0</span><span class="sxs-lookup"><span data-stu-id="862f3-136">+0</span></span>       | <span data-ttu-id="862f3-137">NaN</span><span class="sxs-lookup"><span data-stu-id="862f3-137">NaN</span></span>     |



 

<span data-ttu-id="862f3-138">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="862f3-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="862f3-139">Sommet</span><span class="sxs-lookup"><span data-stu-id="862f3-139">Vertex</span></span> | <span data-ttu-id="862f3-140">Forme</span><span class="sxs-lookup"><span data-stu-id="862f3-140">Hull</span></span> | <span data-ttu-id="862f3-141">Domain</span><span class="sxs-lookup"><span data-stu-id="862f3-141">Domain</span></span> | <span data-ttu-id="862f3-142">Géométrie</span><span class="sxs-lookup"><span data-stu-id="862f3-142">Geometry</span></span> | <span data-ttu-id="862f3-143">Pixel</span><span class="sxs-lookup"><span data-stu-id="862f3-143">Pixel</span></span> | <span data-ttu-id="862f3-144">Calcul</span><span class="sxs-lookup"><span data-stu-id="862f3-144">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="862f3-145">X</span><span class="sxs-lookup"><span data-stu-id="862f3-145">X</span></span>      | <span data-ttu-id="862f3-146">X</span><span class="sxs-lookup"><span data-stu-id="862f3-146">X</span></span>    | <span data-ttu-id="862f3-147">X</span><span class="sxs-lookup"><span data-stu-id="862f3-147">X</span></span>      | <span data-ttu-id="862f3-148">X</span><span class="sxs-lookup"><span data-stu-id="862f3-148">X</span></span>        | <span data-ttu-id="862f3-149">X</span><span class="sxs-lookup"><span data-stu-id="862f3-149">X</span></span>     | <span data-ttu-id="862f3-150">X</span><span class="sxs-lookup"><span data-stu-id="862f3-150">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="862f3-151">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="862f3-151">Minimum Shader Model</span></span>

<span data-ttu-id="862f3-152">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="862f3-152">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="862f3-153">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="862f3-153">Shader Model</span></span>                                              | <span data-ttu-id="862f3-154">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="862f3-154">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="862f3-155">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="862f3-155">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="862f3-156">oui</span><span class="sxs-lookup"><span data-stu-id="862f3-156">yes</span></span>       |
| [<span data-ttu-id="862f3-157">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="862f3-157">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="862f3-158">non</span><span class="sxs-lookup"><span data-stu-id="862f3-158">no</span></span>        |
| [<span data-ttu-id="862f3-159">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="862f3-159">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="862f3-160">non</span><span class="sxs-lookup"><span data-stu-id="862f3-160">no</span></span>        |
| [<span data-ttu-id="862f3-161">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="862f3-161">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="862f3-162">non</span><span class="sxs-lookup"><span data-stu-id="862f3-162">no</span></span>        |
| [<span data-ttu-id="862f3-163">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="862f3-163">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="862f3-164">non</span><span class="sxs-lookup"><span data-stu-id="862f3-164">no</span></span>        |
| [<span data-ttu-id="862f3-165">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="862f3-165">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="862f3-166">non</span><span class="sxs-lookup"><span data-stu-id="862f3-166">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="862f3-167">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="862f3-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="862f3-168">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="862f3-168">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





