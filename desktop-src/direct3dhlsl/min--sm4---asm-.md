---
title: min (SM4-ASM)
description: Valeur minimale à virgule flottante au niveau du composant.
ms.assetid: 8EDD5503-76D5-4078-BFBA-1DA9260C6E68
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8791589b77edc66eeab4b48f10f4a9b16b5cb2d9
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993896"
---
# <a name="min-sm4---asm"></a><span data-ttu-id="c82f0-103">min (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="c82f0-103">min (sm4 - asm)</span></span>

<span data-ttu-id="c82f0-104">Valeur minimale à virgule flottante au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="c82f0-104">Component-wise float minimum.</span></span>



| <span data-ttu-id="c82f0-105">min \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="c82f0-105">min\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="c82f0-106">Élément</span><span class="sxs-lookup"><span data-stu-id="c82f0-106">Item</span></span>                                                            | <span data-ttu-id="c82f0-107">Description</span><span class="sxs-lookup"><span data-stu-id="c82f0-107">Description</span></span>                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c82f0-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="c82f0-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="c82f0-109">\[dans \] le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="c82f0-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="c82f0-110">*dest*  =  . *src0*  <  *src1* ?</span><span class="sxs-lookup"><span data-stu-id="c82f0-110">*dest* = *src0* < *src1* ?</span></span> <span data-ttu-id="c82f0-111">*src0* : *src1*</span><span class="sxs-lookup"><span data-stu-id="c82f0-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="c82f0-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="c82f0-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="c82f0-113">\[dans \] les composants à comparer à *src1*.</span><span class="sxs-lookup"><span data-stu-id="c82f0-113">\[in\] The components to compare to *src1*.</span></span><br/>                                                  |
| <span data-ttu-id="c82f0-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="c82f0-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="c82f0-115">\[dans \] les composants à comparer à *src0*.</span><span class="sxs-lookup"><span data-stu-id="c82f0-115">\[in\] The components to compare to *src0*.</span></span><br/>                                                  |



 

## <a name="remarks"></a><span data-ttu-id="c82f0-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="c82f0-116">Remarks</span></span>

><span data-ttu-id="c82f0-117">= est utilisé à la place de > afin que si min (x, y) = x, alors Max (x, y) = y.</span><span class="sxs-lookup"><span data-stu-id="c82f0-117">= is used instead of > so that if min(x,y) = x then max(x,y) = y.</span></span>

<span data-ttu-id="c82f0-118">NaN a une gestion spéciale.</span><span class="sxs-lookup"><span data-stu-id="c82f0-118">NaN has special handling.</span></span> <span data-ttu-id="c82f0-119">Si un opérande source est NaN, l’autre opérande source est retourné et le choix est effectué par composant.</span><span class="sxs-lookup"><span data-stu-id="c82f0-119">If one source operand is NaN, then the other source operand is returned and the choice is made per-component.</span></span> <span data-ttu-id="c82f0-120">Si les deux sont NaN, toute représentation NaN est retournée.</span><span class="sxs-lookup"><span data-stu-id="c82f0-120">If both are NaN, any NaN representation is returned.</span></span> <span data-ttu-id="c82f0-121">Cela est conforme aux nouvelles règles IEEE 754R.</span><span class="sxs-lookup"><span data-stu-id="c82f0-121">This conforms to new IEEE 754R rules.</span></span>

<span data-ttu-id="c82f0-122">Les dénormes sont vidées, le signe étant préservé, avant la comparaison.</span><span class="sxs-lookup"><span data-stu-id="c82f0-122">Denorms are flushed, with the sign preserved, before comparison.</span></span> <span data-ttu-id="c82f0-123">Toutefois, le résultat écrit dans *dest* peut ou non être vidé.</span><span class="sxs-lookup"><span data-stu-id="c82f0-123">However, the result written to *dest* may or may not be denorm flushed.</span></span>

<span data-ttu-id="c82f0-124">Le tableau suivant présente les résultats obtenus lors de l’exécution de l’instruction avec différentes classes de nombres, en supposant qu’aucun dépassement de capacité ou négatif ne se produit.</span><span class="sxs-lookup"><span data-stu-id="c82f0-124">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="c82f0-125">F signifie nombre réel fini.</span><span class="sxs-lookup"><span data-stu-id="c82f0-125">F means finite real number.</span></span>



| <span data-ttu-id="c82f0-126">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="c82f0-126">**src0 src1->**</span></span> | <span data-ttu-id="c82f0-127">**-INF**</span><span class="sxs-lookup"><span data-stu-id="c82f0-127">**-inf**</span></span> | <span data-ttu-id="c82f0-128">**F**</span><span class="sxs-lookup"><span data-stu-id="c82f0-128">**F**</span></span>        | <span data-ttu-id="c82f0-129">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="c82f0-129">**+inf**</span></span> | <span data-ttu-id="c82f0-130">**NaN**</span><span class="sxs-lookup"><span data-stu-id="c82f0-130">**NaN**</span></span> |
|--------------------|----------|--------------|----------|---------|
| <span data-ttu-id="c82f0-131">**-INF**</span><span class="sxs-lookup"><span data-stu-id="c82f0-131">**-inf**</span></span>           | <span data-ttu-id="c82f0-132">-inf</span><span class="sxs-lookup"><span data-stu-id="c82f0-132">-inf</span></span>     | <span data-ttu-id="c82f0-133">-inf</span><span class="sxs-lookup"><span data-stu-id="c82f0-133">-inf</span></span>         | <span data-ttu-id="c82f0-134">-inf</span><span class="sxs-lookup"><span data-stu-id="c82f0-134">-inf</span></span>     | <span data-ttu-id="c82f0-135">-inf</span><span class="sxs-lookup"><span data-stu-id="c82f0-135">-inf</span></span>    |
| <span data-ttu-id="c82f0-136">**F**</span><span class="sxs-lookup"><span data-stu-id="c82f0-136">**F**</span></span>              | <span data-ttu-id="c82f0-137">-inf</span><span class="sxs-lookup"><span data-stu-id="c82f0-137">-inf</span></span>     | <span data-ttu-id="c82f0-138">src0 ou src1</span><span class="sxs-lookup"><span data-stu-id="c82f0-138">src0 or src1</span></span> | <span data-ttu-id="c82f0-139">src0</span><span class="sxs-lookup"><span data-stu-id="c82f0-139">src0</span></span>     | <span data-ttu-id="c82f0-140">src0</span><span class="sxs-lookup"><span data-stu-id="c82f0-140">src0</span></span>    |
| <span data-ttu-id="c82f0-141">**-INF**</span><span class="sxs-lookup"><span data-stu-id="c82f0-141">**-inf**</span></span>           | <span data-ttu-id="c82f0-142">-inf</span><span class="sxs-lookup"><span data-stu-id="c82f0-142">-inf</span></span>     | <span data-ttu-id="c82f0-143">src1</span><span class="sxs-lookup"><span data-stu-id="c82f0-143">src1</span></span>         | <span data-ttu-id="c82f0-144">+inf</span><span class="sxs-lookup"><span data-stu-id="c82f0-144">+inf</span></span>     | <span data-ttu-id="c82f0-145">+inf</span><span class="sxs-lookup"><span data-stu-id="c82f0-145">+inf</span></span>    |
| <span data-ttu-id="c82f0-146">**NaN**</span><span class="sxs-lookup"><span data-stu-id="c82f0-146">**NaN**</span></span>            | <span data-ttu-id="c82f0-147">-inf</span><span class="sxs-lookup"><span data-stu-id="c82f0-147">-inf</span></span>     | <span data-ttu-id="c82f0-148">src1</span><span class="sxs-lookup"><span data-stu-id="c82f0-148">src1</span></span>         | <span data-ttu-id="c82f0-149">+inf</span><span class="sxs-lookup"><span data-stu-id="c82f0-149">+inf</span></span>     | <span data-ttu-id="c82f0-150">NaN</span><span class="sxs-lookup"><span data-stu-id="c82f0-150">NaN</span></span>     |



 

<span data-ttu-id="c82f0-151">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="c82f0-151">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c82f0-152">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="c82f0-152">Vertex Shader</span></span> | <span data-ttu-id="c82f0-153">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="c82f0-153">Geometry Shader</span></span> | <span data-ttu-id="c82f0-154">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="c82f0-154">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="c82f0-155">x</span><span class="sxs-lookup"><span data-stu-id="c82f0-155">x</span></span>             | <span data-ttu-id="c82f0-156">x</span><span class="sxs-lookup"><span data-stu-id="c82f0-156">x</span></span>               | <span data-ttu-id="c82f0-157">x</span><span class="sxs-lookup"><span data-stu-id="c82f0-157">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c82f0-158">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="c82f0-158">Minimum Shader Model</span></span>

<span data-ttu-id="c82f0-159">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="c82f0-159">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c82f0-160">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="c82f0-160">Shader Model</span></span>                                              | <span data-ttu-id="c82f0-161">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="c82f0-161">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c82f0-162">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="c82f0-162">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c82f0-163">oui</span><span class="sxs-lookup"><span data-stu-id="c82f0-163">yes</span></span>       |
| [<span data-ttu-id="c82f0-164">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="c82f0-164">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c82f0-165">oui</span><span class="sxs-lookup"><span data-stu-id="c82f0-165">yes</span></span>       |
| [<span data-ttu-id="c82f0-166">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="c82f0-166">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c82f0-167">oui</span><span class="sxs-lookup"><span data-stu-id="c82f0-167">yes</span></span>       |
| [<span data-ttu-id="c82f0-168">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c82f0-168">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c82f0-169">non</span><span class="sxs-lookup"><span data-stu-id="c82f0-169">no</span></span>        |
| [<span data-ttu-id="c82f0-170">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c82f0-170">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c82f0-171">non</span><span class="sxs-lookup"><span data-stu-id="c82f0-171">no</span></span>        |
| [<span data-ttu-id="c82f0-172">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c82f0-172">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c82f0-173">non</span><span class="sxs-lookup"><span data-stu-id="c82f0-173">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c82f0-174">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c82f0-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c82f0-175">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c82f0-175">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





