---
title: log (SM4-ASM)
description: Base du journal des composants 2.
ms.assetid: 6D28864A-C2BA-44AF-9E78-7C2B34F5E462
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88e4b89b4dcc085cf4fd4fda762d96fb71271af2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998316"
---
# <a name="log-sm4---asm"></a><span data-ttu-id="ba306-103">log (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="ba306-103">log (sm4 - asm)</span></span>

<span data-ttu-id="ba306-104">Base du journal des composants 2.</span><span class="sxs-lookup"><span data-stu-id="ba306-104">Component-wise log base 2.</span></span>



| <span data-ttu-id="ba306-105">log \[ \_ sam \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle</span><span class="sxs-lookup"><span data-stu-id="ba306-105">log\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle</span></span> |
|----------------------------------------------------------|



 



| <span data-ttu-id="ba306-106">Élément</span><span class="sxs-lookup"><span data-stu-id="ba306-106">Item</span></span>                                                            | <span data-ttu-id="ba306-107">Description</span><span class="sxs-lookup"><span data-stu-id="ba306-107">Description</span></span>                                                                                |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba306-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="ba306-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="ba306-109">\[dans \] l’adresse du résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="ba306-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="ba306-110">dest = Log2 (src0)</span><span class="sxs-lookup"><span data-stu-id="ba306-110">dest = log2(src0)</span></span><br/> |
| <span data-ttu-id="ba306-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="ba306-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="ba306-112">\[dans \] la valeur de l’opération.</span><span class="sxs-lookup"><span data-stu-id="ba306-112">\[in\] The value for the operation.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="ba306-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="ba306-113">Remarks</span></span>

### <a name="restrictions"></a><span data-ttu-id="ba306-114">Restrictions</span><span class="sxs-lookup"><span data-stu-id="ba306-114">Restrictions</span></span>

-   <span data-ttu-id="ba306-115">Suit la théorie des limites.</span><span class="sxs-lookup"><span data-stu-id="ba306-115">Follows limit theory.</span></span>
-   <span data-ttu-id="ba306-116">Tolérance d’erreur : si *src0* est \[ 0.5.. 2 \] , l’erreur absolue ne doit pas être supérieure à 2-21.</span><span class="sxs-lookup"><span data-stu-id="ba306-116">Error tolerance: If *src0* is \[0.5..2\], absolue error must be no more than 2-21.</span></span> <span data-ttu-id="ba306-117">Si *src0* est (0.. 0.5) ou (2.. + inf \] , l’erreur relative ne doit pas être supérieure à 2-21.</span><span class="sxs-lookup"><span data-stu-id="ba306-117">If *src0* is (0..0.5) or (2..+INF\], relative error must be no more than 2-21.</span></span>

<span data-ttu-id="ba306-118">Le tableau suivant présente les résultats obtenus lors de l’exécution de l’instruction avec différentes classes de nombres, en supposant qu’aucun dépassement de capacité ou négatif ne se produit.</span><span class="sxs-lookup"><span data-stu-id="ba306-118">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="ba306-119">F signifie nombre fini-réel.</span><span class="sxs-lookup"><span data-stu-id="ba306-119">F means finite-real number.</span></span>



| <span data-ttu-id="ba306-120">**src**</span><span class="sxs-lookup"><span data-stu-id="ba306-120">**src**</span></span>  | <span data-ttu-id="ba306-121">**-INF**</span><span class="sxs-lookup"><span data-stu-id="ba306-121">**-inf**</span></span> | <span data-ttu-id="ba306-122">**-F**</span><span class="sxs-lookup"><span data-stu-id="ba306-122">**-F**</span></span> | <span data-ttu-id="ba306-123">**-dénorme**</span><span class="sxs-lookup"><span data-stu-id="ba306-123">**-denorm**</span></span> | <span data-ttu-id="ba306-124">**-0**</span><span class="sxs-lookup"><span data-stu-id="ba306-124">**-0**</span></span> | <span data-ttu-id="ba306-125">**+0**</span><span class="sxs-lookup"><span data-stu-id="ba306-125">**+0**</span></span> | <span data-ttu-id="ba306-126">**+ dénorme**</span><span class="sxs-lookup"><span data-stu-id="ba306-126">**+denorm**</span></span> | <span data-ttu-id="ba306-127">**+ F**</span><span class="sxs-lookup"><span data-stu-id="ba306-127">**+F**</span></span> | <span data-ttu-id="ba306-128">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="ba306-128">**+inf**</span></span> | <span data-ttu-id="ba306-129">**NaN**</span><span class="sxs-lookup"><span data-stu-id="ba306-129">**NaN**</span></span> |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="ba306-130">**dest**</span><span class="sxs-lookup"><span data-stu-id="ba306-130">**dest**</span></span> | <span data-ttu-id="ba306-131">NaN</span><span class="sxs-lookup"><span data-stu-id="ba306-131">NaN</span></span>      | <span data-ttu-id="ba306-132">NaN</span><span class="sxs-lookup"><span data-stu-id="ba306-132">NaN</span></span>    | <span data-ttu-id="ba306-133">-inf</span><span class="sxs-lookup"><span data-stu-id="ba306-133">-inf</span></span>        | <span data-ttu-id="ba306-134">-inf</span><span class="sxs-lookup"><span data-stu-id="ba306-134">-inf</span></span>   | <span data-ttu-id="ba306-135">-inf</span><span class="sxs-lookup"><span data-stu-id="ba306-135">-inf</span></span>   | <span data-ttu-id="ba306-136">-inf</span><span class="sxs-lookup"><span data-stu-id="ba306-136">-inf</span></span>        | <span data-ttu-id="ba306-137">F</span><span class="sxs-lookup"><span data-stu-id="ba306-137">F</span></span>      | <span data-ttu-id="ba306-138">+inf</span><span class="sxs-lookup"><span data-stu-id="ba306-138">+inf</span></span>     | <span data-ttu-id="ba306-139">NaN</span><span class="sxs-lookup"><span data-stu-id="ba306-139">NaN</span></span>     |



 

<span data-ttu-id="ba306-140">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="ba306-140">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ba306-141">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="ba306-141">Vertex Shader</span></span> | <span data-ttu-id="ba306-142">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="ba306-142">Geometry Shader</span></span> | <span data-ttu-id="ba306-143">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="ba306-143">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="ba306-144">x</span><span class="sxs-lookup"><span data-stu-id="ba306-144">x</span></span>             | <span data-ttu-id="ba306-145">x</span><span class="sxs-lookup"><span data-stu-id="ba306-145">x</span></span>               | <span data-ttu-id="ba306-146">x</span><span class="sxs-lookup"><span data-stu-id="ba306-146">x</span></span>            |



 

### <a name="minimum-shader-model"></a><span data-ttu-id="ba306-147">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="ba306-147">Minimum Shader Model</span></span>

<span data-ttu-id="ba306-148">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="ba306-148">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ba306-149">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="ba306-149">Shader Model</span></span>                                              | <span data-ttu-id="ba306-150">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba306-150">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ba306-151">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="ba306-151">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ba306-152">oui</span><span class="sxs-lookup"><span data-stu-id="ba306-152">yes</span></span>       |
| [<span data-ttu-id="ba306-153">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="ba306-153">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ba306-154">oui</span><span class="sxs-lookup"><span data-stu-id="ba306-154">yes</span></span>       |
| [<span data-ttu-id="ba306-155">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="ba306-155">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ba306-156">oui</span><span class="sxs-lookup"><span data-stu-id="ba306-156">yes</span></span>       |
| [<span data-ttu-id="ba306-157">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ba306-157">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ba306-158">non</span><span class="sxs-lookup"><span data-stu-id="ba306-158">no</span></span>        |
| [<span data-ttu-id="ba306-159">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ba306-159">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ba306-160">non</span><span class="sxs-lookup"><span data-stu-id="ba306-160">no</span></span>        |
| [<span data-ttu-id="ba306-161">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ba306-161">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ba306-162">non</span><span class="sxs-lookup"><span data-stu-id="ba306-162">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ba306-163">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ba306-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba306-164">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ba306-164">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





