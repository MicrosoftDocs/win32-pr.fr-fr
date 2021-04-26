---
title: Max (SM4-ASM)
description: Nombre maximal de virgule flottante au niveau du composant.
ms.assetid: 005468AA-577E-441F-ACD5-37A691E62CDD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f64d88c581828f2563f6d5d8a6c57de6400f9bbf
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994726"
---
# <a name="max-sm4---asm"></a><span data-ttu-id="16c4b-103">Max (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="16c4b-103">max (sm4 - asm)</span></span>

<span data-ttu-id="16c4b-104">Nombre maximal de virgule flottante au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="16c4b-104">Component-wise float maximum.</span></span>



| <span data-ttu-id="16c4b-105">Max \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="16c4b-105">max\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="16c4b-106">Élément</span><span class="sxs-lookup"><span data-stu-id="16c4b-106">Item</span></span>                                                            | <span data-ttu-id="16c4b-107">Description</span><span class="sxs-lookup"><span data-stu-id="16c4b-107">Description</span></span>                                                                                               |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16c4b-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="16c4b-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="16c4b-109">\[dans \] le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="16c4b-109">\[in\] The result of the operation.</span></span> <br/> <span data-ttu-id="16c4b-110">*dest*  =  . *src0*  >=  *src1* ?</span><span class="sxs-lookup"><span data-stu-id="16c4b-110">*dest* = *src0* >= *src1* ?</span></span> <span data-ttu-id="16c4b-111">*src0* : *src1*</span><span class="sxs-lookup"><span data-stu-id="16c4b-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="16c4b-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="16c4b-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="16c4b-113">\[dans \] les composants à comparer à *src1*.</span><span class="sxs-lookup"><span data-stu-id="16c4b-113">\[in\] The components to compare to *src1*.</span></span><br/>                                                    |
| <span data-ttu-id="16c4b-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="16c4b-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="16c4b-115">\[dans \] les composants à comparer à *src0*.</span><span class="sxs-lookup"><span data-stu-id="16c4b-115">\[in\] The components to compare to *src0*.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="16c4b-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="16c4b-116">Remarks</span></span>

><span data-ttu-id="16c4b-117">= est utilisé à la place de > afin que si min (x, y) = x, alors Max (x, y) = y.</span><span class="sxs-lookup"><span data-stu-id="16c4b-117">= is used instead of > so that if min(x,y) = x then max(x,y) = y.</span></span>

<span data-ttu-id="16c4b-118">NaN a une gestion spéciale.</span><span class="sxs-lookup"><span data-stu-id="16c4b-118">NaN has special handling.</span></span> <span data-ttu-id="16c4b-119">Si un opérande source est NaN, l’autre opérande source est retourné et le choix est effectué par composant.</span><span class="sxs-lookup"><span data-stu-id="16c4b-119">If one source operand is NaN, then the other source operand is returned and the choice is made per-component.</span></span> <span data-ttu-id="16c4b-120">Si les deux sont NaN, toute représentation NaN est retournée.</span><span class="sxs-lookup"><span data-stu-id="16c4b-120">If both are NaN, any NaN representation is returned.</span></span>

<span data-ttu-id="16c4b-121">Les dénormes sont vidées avec le signe préservé avant la comparaison.</span><span class="sxs-lookup"><span data-stu-id="16c4b-121">Denorms are flushed with sign preserved before the comparison.</span></span> <span data-ttu-id="16c4b-122">Toutefois, le résultat écrit dans *dest* peut ou non être vidé.</span><span class="sxs-lookup"><span data-stu-id="16c4b-122">However, the result written to *dest* may or may not be denorm flushed.</span></span>

<span data-ttu-id="16c4b-123">Le tableau suivant présente les résultats obtenus lors de l’exécution de l’instruction avec différentes classes de nombres, en supposant qu’aucun dépassement de capacité ou négatif ne se produit.</span><span class="sxs-lookup"><span data-stu-id="16c4b-123">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="16c4b-124">F signifie nombre réel fini.</span><span class="sxs-lookup"><span data-stu-id="16c4b-124">F means finite real number.</span></span>



| <span data-ttu-id="16c4b-125">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="16c4b-125">**src0 src1->**</span></span> | <span data-ttu-id="16c4b-126">**-INF**</span><span class="sxs-lookup"><span data-stu-id="16c4b-126">**-inf**</span></span> | <span data-ttu-id="16c4b-127">**F**</span><span class="sxs-lookup"><span data-stu-id="16c4b-127">**F**</span></span>        | <span data-ttu-id="16c4b-128">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="16c4b-128">**+inf**</span></span> | <span data-ttu-id="16c4b-129">**NaN**</span><span class="sxs-lookup"><span data-stu-id="16c4b-129">**NaN**</span></span> |
|--------------------|----------|--------------|----------|---------|
| <span data-ttu-id="16c4b-130">**-INF**</span><span class="sxs-lookup"><span data-stu-id="16c4b-130">**-inf**</span></span>           | <span data-ttu-id="16c4b-131">-inf</span><span class="sxs-lookup"><span data-stu-id="16c4b-131">-inf</span></span>     | <span data-ttu-id="16c4b-132">src1</span><span class="sxs-lookup"><span data-stu-id="16c4b-132">src1</span></span>         | <span data-ttu-id="16c4b-133">+inf</span><span class="sxs-lookup"><span data-stu-id="16c4b-133">+inf</span></span>     | <span data-ttu-id="16c4b-134">-inf</span><span class="sxs-lookup"><span data-stu-id="16c4b-134">-inf</span></span>    |
| <span data-ttu-id="16c4b-135">**F**</span><span class="sxs-lookup"><span data-stu-id="16c4b-135">**F**</span></span>              | <span data-ttu-id="16c4b-136">src0</span><span class="sxs-lookup"><span data-stu-id="16c4b-136">src0</span></span>     | <span data-ttu-id="16c4b-137">src0 ou src1</span><span class="sxs-lookup"><span data-stu-id="16c4b-137">src0 or src1</span></span> | <span data-ttu-id="16c4b-138">+inf</span><span class="sxs-lookup"><span data-stu-id="16c4b-138">+inf</span></span>     | <span data-ttu-id="16c4b-139">src0</span><span class="sxs-lookup"><span data-stu-id="16c4b-139">src0</span></span>    |
| <span data-ttu-id="16c4b-140">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="16c4b-140">**+inf**</span></span>           | <span data-ttu-id="16c4b-141">+inf</span><span class="sxs-lookup"><span data-stu-id="16c4b-141">+inf</span></span>     | <span data-ttu-id="16c4b-142">+inf</span><span class="sxs-lookup"><span data-stu-id="16c4b-142">+inf</span></span>         | <span data-ttu-id="16c4b-143">+inf</span><span class="sxs-lookup"><span data-stu-id="16c4b-143">+inf</span></span>     | <span data-ttu-id="16c4b-144">+inf</span><span class="sxs-lookup"><span data-stu-id="16c4b-144">+inf</span></span>    |
| <span data-ttu-id="16c4b-145">**NaN**</span><span class="sxs-lookup"><span data-stu-id="16c4b-145">**NaN**</span></span>            | <span data-ttu-id="16c4b-146">-inf</span><span class="sxs-lookup"><span data-stu-id="16c4b-146">-inf</span></span>     | <span data-ttu-id="16c4b-147">src1</span><span class="sxs-lookup"><span data-stu-id="16c4b-147">src1</span></span>         | <span data-ttu-id="16c4b-148">+inf</span><span class="sxs-lookup"><span data-stu-id="16c4b-148">+inf</span></span>     | <span data-ttu-id="16c4b-149">NaN</span><span class="sxs-lookup"><span data-stu-id="16c4b-149">NaN</span></span>     |



 

<span data-ttu-id="16c4b-150">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="16c4b-150">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="16c4b-151">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="16c4b-151">Vertex Shader</span></span> | <span data-ttu-id="16c4b-152">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="16c4b-152">Geometry Shader</span></span> | <span data-ttu-id="16c4b-153">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="16c4b-153">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="16c4b-154">x</span><span class="sxs-lookup"><span data-stu-id="16c4b-154">x</span></span>             | <span data-ttu-id="16c4b-155">x</span><span class="sxs-lookup"><span data-stu-id="16c4b-155">x</span></span>               | <span data-ttu-id="16c4b-156">x</span><span class="sxs-lookup"><span data-stu-id="16c4b-156">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="16c4b-157">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="16c4b-157">Minimum Shader Model</span></span>

<span data-ttu-id="16c4b-158">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="16c4b-158">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="16c4b-159">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="16c4b-159">Shader Model</span></span>                                              | <span data-ttu-id="16c4b-160">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="16c4b-160">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="16c4b-161">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="16c4b-161">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="16c4b-162">oui</span><span class="sxs-lookup"><span data-stu-id="16c4b-162">yes</span></span>       |
| [<span data-ttu-id="16c4b-163">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="16c4b-163">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="16c4b-164">oui</span><span class="sxs-lookup"><span data-stu-id="16c4b-164">yes</span></span>       |
| [<span data-ttu-id="16c4b-165">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="16c4b-165">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="16c4b-166">oui</span><span class="sxs-lookup"><span data-stu-id="16c4b-166">yes</span></span>       |
| [<span data-ttu-id="16c4b-167">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="16c4b-167">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="16c4b-168">non</span><span class="sxs-lookup"><span data-stu-id="16c4b-168">no</span></span>        |
| [<span data-ttu-id="16c4b-169">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="16c4b-169">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="16c4b-170">non</span><span class="sxs-lookup"><span data-stu-id="16c4b-170">no</span></span>        |
| [<span data-ttu-id="16c4b-171">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="16c4b-171">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="16c4b-172">non</span><span class="sxs-lookup"><span data-stu-id="16c4b-172">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="16c4b-173">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="16c4b-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16c4b-174">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="16c4b-174">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





