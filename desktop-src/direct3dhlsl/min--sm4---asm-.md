---
title: min (SM4-ASM)
description: Valeur minimale à virgule flottante au niveau du composant.
ms.assetid: 8EDD5503-76D5-4078-BFBA-1DA9260C6E68
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e584aee077735b717bf76d148d4d0db4357a7d95
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104101105"
---
# <a name="min-sm4---asm"></a><span data-ttu-id="7e049-103">min (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="7e049-103">min (sm4 - asm)</span></span>

<span data-ttu-id="7e049-104">Valeur minimale à virgule flottante au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="7e049-104">Component-wise float minimum.</span></span>



| <span data-ttu-id="7e049-105">min \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="7e049-105">min\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="7e049-106">Élément</span><span class="sxs-lookup"><span data-stu-id="7e049-106">Item</span></span>                                                            | <span data-ttu-id="7e049-107">Description</span><span class="sxs-lookup"><span data-stu-id="7e049-107">Description</span></span>                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e049-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="7e049-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="7e049-109">\[dans \] le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="7e049-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="7e049-110">*dest*  =  . *src0*  <  *src1* ?</span><span class="sxs-lookup"><span data-stu-id="7e049-110">*dest* = *src0* < *src1* ?</span></span> <span data-ttu-id="7e049-111">*src0* : *src1*</span><span class="sxs-lookup"><span data-stu-id="7e049-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="7e049-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="7e049-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="7e049-113">\[dans \] les composants à comparer à *src1*.</span><span class="sxs-lookup"><span data-stu-id="7e049-113">\[in\] The components to compare to *src1*.</span></span><br/>                                                  |
| <span data-ttu-id="7e049-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="7e049-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="7e049-115">\[dans \] les composants à comparer à *src0*.</span><span class="sxs-lookup"><span data-stu-id="7e049-115">\[in\] The components to compare to *src0*.</span></span><br/>                                                  |



 

## <a name="remarks"></a><span data-ttu-id="7e049-116">Notes</span><span class="sxs-lookup"><span data-stu-id="7e049-116">Remarks</span></span>

><span data-ttu-id="7e049-117">= est utilisé à la place de > afin que si min (x, y) = x, alors Max (x, y) = y.</span><span class="sxs-lookup"><span data-stu-id="7e049-117">= is used instead of > so that if min(x,y) = x then max(x,y) = y.</span></span>

<span data-ttu-id="7e049-118">NaN a une gestion spéciale.</span><span class="sxs-lookup"><span data-stu-id="7e049-118">NaN has special handling.</span></span> <span data-ttu-id="7e049-119">Si un opérande source est NaN, l’autre opérande source est retourné et le choix est effectué par composant.</span><span class="sxs-lookup"><span data-stu-id="7e049-119">If one source operand is NaN, then the other source operand is returned and the choice is made per-component.</span></span> <span data-ttu-id="7e049-120">Si les deux sont NaN, toute représentation NaN est retournée.</span><span class="sxs-lookup"><span data-stu-id="7e049-120">If both are NaN, any NaN representation is returned.</span></span> <span data-ttu-id="7e049-121">Cela est conforme aux nouvelles règles IEEE 754R.</span><span class="sxs-lookup"><span data-stu-id="7e049-121">This conforms to new IEEE 754R rules.</span></span>

<span data-ttu-id="7e049-122">Les dénormes sont vidées, le signe étant préservé, avant la comparaison.</span><span class="sxs-lookup"><span data-stu-id="7e049-122">Denorms are flushed, with the sign preserved, before comparison.</span></span> <span data-ttu-id="7e049-123">Toutefois, le résultat écrit dans *dest* peut ou non être vidé.</span><span class="sxs-lookup"><span data-stu-id="7e049-123">However, the result written to *dest* may or may not be denorm flushed.</span></span>

<span data-ttu-id="7e049-124">Le tableau suivant présente les résultats obtenus lors de l’exécution de l’instruction avec différentes classes de nombres, en supposant qu’aucun dépassement de capacité ou négatif ne se produit.</span><span class="sxs-lookup"><span data-stu-id="7e049-124">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="7e049-125">F signifie nombre réel fini.</span><span class="sxs-lookup"><span data-stu-id="7e049-125">F means finite real number.</span></span>



|                    |          |              |          |         |
|--------------------|----------|--------------|----------|---------|
| <span data-ttu-id="7e049-126">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="7e049-126">**src0 src1->**</span></span> | <span data-ttu-id="7e049-127">**-INF**</span><span class="sxs-lookup"><span data-stu-id="7e049-127">**-inf**</span></span> | <span data-ttu-id="7e049-128">**F**</span><span class="sxs-lookup"><span data-stu-id="7e049-128">**F**</span></span>        | <span data-ttu-id="7e049-129">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="7e049-129">**+inf**</span></span> | <span data-ttu-id="7e049-130">**NaN**</span><span class="sxs-lookup"><span data-stu-id="7e049-130">**NaN**</span></span> |
| <span data-ttu-id="7e049-131">**-INF**</span><span class="sxs-lookup"><span data-stu-id="7e049-131">**-inf**</span></span>           | <span data-ttu-id="7e049-132">-inf</span><span class="sxs-lookup"><span data-stu-id="7e049-132">-inf</span></span>     | <span data-ttu-id="7e049-133">-inf</span><span class="sxs-lookup"><span data-stu-id="7e049-133">-inf</span></span>         | <span data-ttu-id="7e049-134">-inf</span><span class="sxs-lookup"><span data-stu-id="7e049-134">-inf</span></span>     | <span data-ttu-id="7e049-135">-inf</span><span class="sxs-lookup"><span data-stu-id="7e049-135">-inf</span></span>    |
| <span data-ttu-id="7e049-136">**F**</span><span class="sxs-lookup"><span data-stu-id="7e049-136">**F**</span></span>              | <span data-ttu-id="7e049-137">-inf</span><span class="sxs-lookup"><span data-stu-id="7e049-137">-inf</span></span>     | <span data-ttu-id="7e049-138">src0 ou src1</span><span class="sxs-lookup"><span data-stu-id="7e049-138">src0 or src1</span></span> | <span data-ttu-id="7e049-139">src0</span><span class="sxs-lookup"><span data-stu-id="7e049-139">src0</span></span>     | <span data-ttu-id="7e049-140">src0</span><span class="sxs-lookup"><span data-stu-id="7e049-140">src0</span></span>    |
| <span data-ttu-id="7e049-141">**-INF**</span><span class="sxs-lookup"><span data-stu-id="7e049-141">**-inf**</span></span>           | <span data-ttu-id="7e049-142">-inf</span><span class="sxs-lookup"><span data-stu-id="7e049-142">-inf</span></span>     | <span data-ttu-id="7e049-143">src1</span><span class="sxs-lookup"><span data-stu-id="7e049-143">src1</span></span>         | <span data-ttu-id="7e049-144">+inf</span><span class="sxs-lookup"><span data-stu-id="7e049-144">+inf</span></span>     | <span data-ttu-id="7e049-145">+inf</span><span class="sxs-lookup"><span data-stu-id="7e049-145">+inf</span></span>    |
| <span data-ttu-id="7e049-146">**NaN**</span><span class="sxs-lookup"><span data-stu-id="7e049-146">**NaN**</span></span>            | <span data-ttu-id="7e049-147">-inf</span><span class="sxs-lookup"><span data-stu-id="7e049-147">-inf</span></span>     | <span data-ttu-id="7e049-148">src1</span><span class="sxs-lookup"><span data-stu-id="7e049-148">src1</span></span>         | <span data-ttu-id="7e049-149">+inf</span><span class="sxs-lookup"><span data-stu-id="7e049-149">+inf</span></span>     | <span data-ttu-id="7e049-150">NaN</span><span class="sxs-lookup"><span data-stu-id="7e049-150">NaN</span></span>     |



 

<span data-ttu-id="7e049-151">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="7e049-151">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="7e049-152">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="7e049-152">Vertex Shader</span></span> | <span data-ttu-id="7e049-153">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="7e049-153">Geometry Shader</span></span> | <span data-ttu-id="7e049-154">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="7e049-154">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="7e049-155">x</span><span class="sxs-lookup"><span data-stu-id="7e049-155">x</span></span>             | <span data-ttu-id="7e049-156">x</span><span class="sxs-lookup"><span data-stu-id="7e049-156">x</span></span>               | <span data-ttu-id="7e049-157">x</span><span class="sxs-lookup"><span data-stu-id="7e049-157">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7e049-158">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="7e049-158">Minimum Shader Model</span></span>

<span data-ttu-id="7e049-159">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="7e049-159">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7e049-160">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="7e049-160">Shader Model</span></span>                                              | <span data-ttu-id="7e049-161">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="7e049-161">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="7e049-162">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="7e049-162">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="7e049-163">Oui</span><span class="sxs-lookup"><span data-stu-id="7e049-163">yes</span></span>       |
| [<span data-ttu-id="7e049-164">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="7e049-164">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="7e049-165">Oui</span><span class="sxs-lookup"><span data-stu-id="7e049-165">yes</span></span>       |
| [<span data-ttu-id="7e049-166">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="7e049-166">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="7e049-167">Oui</span><span class="sxs-lookup"><span data-stu-id="7e049-167">yes</span></span>       |
| [<span data-ttu-id="7e049-168">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7e049-168">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="7e049-169">non</span><span class="sxs-lookup"><span data-stu-id="7e049-169">no</span></span>        |
| [<span data-ttu-id="7e049-170">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7e049-170">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="7e049-171">non</span><span class="sxs-lookup"><span data-stu-id="7e049-171">no</span></span>        |
| [<span data-ttu-id="7e049-172">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7e049-172">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="7e049-173">non</span><span class="sxs-lookup"><span data-stu-id="7e049-173">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="7e049-174">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7e049-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e049-175">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7e049-175">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





