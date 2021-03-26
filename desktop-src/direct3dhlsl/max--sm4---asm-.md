---
title: Max (SM4-ASM)
description: Nombre maximal de virgule flottante au niveau du composant.
ms.assetid: 005468AA-577E-441F-ACD5-37A691E62CDD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f24618897eacf250f2b924f6dde3745a32a7172
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381136"
---
# <a name="max-sm4---asm"></a><span data-ttu-id="406ab-103">Max (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="406ab-103">max (sm4 - asm)</span></span>

<span data-ttu-id="406ab-104">Nombre maximal de virgule flottante au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="406ab-104">Component-wise float maximum.</span></span>



| <span data-ttu-id="406ab-105">Max \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="406ab-105">max\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="406ab-106">Élément</span><span class="sxs-lookup"><span data-stu-id="406ab-106">Item</span></span>                                                            | <span data-ttu-id="406ab-107">Description</span><span class="sxs-lookup"><span data-stu-id="406ab-107">Description</span></span>                                                                                               |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="406ab-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="406ab-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="406ab-109">\[dans \] le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="406ab-109">\[in\] The result of the operation.</span></span> <br/> <span data-ttu-id="406ab-110">*dest*  =  . *src0*  >=  *src1* ?</span><span class="sxs-lookup"><span data-stu-id="406ab-110">*dest* = *src0* >= *src1* ?</span></span> <span data-ttu-id="406ab-111">*src0* : *src1*</span><span class="sxs-lookup"><span data-stu-id="406ab-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="406ab-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="406ab-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="406ab-113">\[dans \] les composants à comparer à *src1*.</span><span class="sxs-lookup"><span data-stu-id="406ab-113">\[in\] The components to compare to *src1*.</span></span><br/>                                                    |
| <span data-ttu-id="406ab-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="406ab-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="406ab-115">\[dans \] les composants à comparer à *src0*.</span><span class="sxs-lookup"><span data-stu-id="406ab-115">\[in\] The components to compare to *src0*.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="406ab-116">Notes</span><span class="sxs-lookup"><span data-stu-id="406ab-116">Remarks</span></span>

><span data-ttu-id="406ab-117">= est utilisé à la place de > afin que si min (x, y) = x, alors Max (x, y) = y.</span><span class="sxs-lookup"><span data-stu-id="406ab-117">= is used instead of > so that if min(x,y) = x then max(x,y) = y.</span></span>

<span data-ttu-id="406ab-118">NaN a une gestion spéciale.</span><span class="sxs-lookup"><span data-stu-id="406ab-118">NaN has special handling.</span></span> <span data-ttu-id="406ab-119">Si un opérande source est NaN, l’autre opérande source est retourné et le choix est effectué par composant.</span><span class="sxs-lookup"><span data-stu-id="406ab-119">If one source operand is NaN, then the other source operand is returned and the choice is made per-component.</span></span> <span data-ttu-id="406ab-120">Si les deux sont NaN, toute représentation NaN est retournée.</span><span class="sxs-lookup"><span data-stu-id="406ab-120">If both are NaN, any NaN representation is returned.</span></span>

<span data-ttu-id="406ab-121">Les dénormes sont vidées avec le signe préservé avant la comparaison.</span><span class="sxs-lookup"><span data-stu-id="406ab-121">Denorms are flushed with sign preserved before the comparison.</span></span> <span data-ttu-id="406ab-122">Toutefois, le résultat écrit dans *dest* peut ou non être vidé.</span><span class="sxs-lookup"><span data-stu-id="406ab-122">However, the result written to *dest* may or may not be denorm flushed.</span></span>

<span data-ttu-id="406ab-123">Le tableau suivant présente les résultats obtenus lors de l’exécution de l’instruction avec différentes classes de nombres, en supposant qu’aucun dépassement de capacité ou négatif ne se produit.</span><span class="sxs-lookup"><span data-stu-id="406ab-123">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="406ab-124">F signifie nombre réel fini.</span><span class="sxs-lookup"><span data-stu-id="406ab-124">F means finite real number.</span></span>



|                    |          |              |          |         |
|--------------------|----------|--------------|----------|---------|
| <span data-ttu-id="406ab-125">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="406ab-125">**src0 src1->**</span></span> | <span data-ttu-id="406ab-126">**-INF**</span><span class="sxs-lookup"><span data-stu-id="406ab-126">**-inf**</span></span> | <span data-ttu-id="406ab-127">**F**</span><span class="sxs-lookup"><span data-stu-id="406ab-127">**F**</span></span>        | <span data-ttu-id="406ab-128">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="406ab-128">**+inf**</span></span> | <span data-ttu-id="406ab-129">**NaN**</span><span class="sxs-lookup"><span data-stu-id="406ab-129">**NaN**</span></span> |
| <span data-ttu-id="406ab-130">**-INF**</span><span class="sxs-lookup"><span data-stu-id="406ab-130">**-inf**</span></span>           | <span data-ttu-id="406ab-131">-inf</span><span class="sxs-lookup"><span data-stu-id="406ab-131">-inf</span></span>     | <span data-ttu-id="406ab-132">src1</span><span class="sxs-lookup"><span data-stu-id="406ab-132">src1</span></span>         | <span data-ttu-id="406ab-133">+inf</span><span class="sxs-lookup"><span data-stu-id="406ab-133">+inf</span></span>     | <span data-ttu-id="406ab-134">-inf</span><span class="sxs-lookup"><span data-stu-id="406ab-134">-inf</span></span>    |
| <span data-ttu-id="406ab-135">**F**</span><span class="sxs-lookup"><span data-stu-id="406ab-135">**F**</span></span>              | <span data-ttu-id="406ab-136">src0</span><span class="sxs-lookup"><span data-stu-id="406ab-136">src0</span></span>     | <span data-ttu-id="406ab-137">src0 ou src1</span><span class="sxs-lookup"><span data-stu-id="406ab-137">src0 or src1</span></span> | <span data-ttu-id="406ab-138">+inf</span><span class="sxs-lookup"><span data-stu-id="406ab-138">+inf</span></span>     | <span data-ttu-id="406ab-139">src0</span><span class="sxs-lookup"><span data-stu-id="406ab-139">src0</span></span>    |
| <span data-ttu-id="406ab-140">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="406ab-140">**+inf**</span></span>           | <span data-ttu-id="406ab-141">+inf</span><span class="sxs-lookup"><span data-stu-id="406ab-141">+inf</span></span>     | <span data-ttu-id="406ab-142">+inf</span><span class="sxs-lookup"><span data-stu-id="406ab-142">+inf</span></span>         | <span data-ttu-id="406ab-143">+inf</span><span class="sxs-lookup"><span data-stu-id="406ab-143">+inf</span></span>     | <span data-ttu-id="406ab-144">+inf</span><span class="sxs-lookup"><span data-stu-id="406ab-144">+inf</span></span>    |
| <span data-ttu-id="406ab-145">**NaN**</span><span class="sxs-lookup"><span data-stu-id="406ab-145">**NaN**</span></span>            | <span data-ttu-id="406ab-146">-inf</span><span class="sxs-lookup"><span data-stu-id="406ab-146">-inf</span></span>     | <span data-ttu-id="406ab-147">src1</span><span class="sxs-lookup"><span data-stu-id="406ab-147">src1</span></span>         | <span data-ttu-id="406ab-148">+inf</span><span class="sxs-lookup"><span data-stu-id="406ab-148">+inf</span></span>     | <span data-ttu-id="406ab-149">NaN</span><span class="sxs-lookup"><span data-stu-id="406ab-149">NaN</span></span>     |



 

<span data-ttu-id="406ab-150">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="406ab-150">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="406ab-151">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="406ab-151">Vertex Shader</span></span> | <span data-ttu-id="406ab-152">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="406ab-152">Geometry Shader</span></span> | <span data-ttu-id="406ab-153">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="406ab-153">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="406ab-154">x</span><span class="sxs-lookup"><span data-stu-id="406ab-154">x</span></span>             | <span data-ttu-id="406ab-155">x</span><span class="sxs-lookup"><span data-stu-id="406ab-155">x</span></span>               | <span data-ttu-id="406ab-156">x</span><span class="sxs-lookup"><span data-stu-id="406ab-156">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="406ab-157">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="406ab-157">Minimum Shader Model</span></span>

<span data-ttu-id="406ab-158">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="406ab-158">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="406ab-159">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="406ab-159">Shader Model</span></span>                                              | <span data-ttu-id="406ab-160">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="406ab-160">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="406ab-161">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="406ab-161">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="406ab-162">Oui</span><span class="sxs-lookup"><span data-stu-id="406ab-162">yes</span></span>       |
| [<span data-ttu-id="406ab-163">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="406ab-163">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="406ab-164">Oui</span><span class="sxs-lookup"><span data-stu-id="406ab-164">yes</span></span>       |
| [<span data-ttu-id="406ab-165">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="406ab-165">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="406ab-166">Oui</span><span class="sxs-lookup"><span data-stu-id="406ab-166">yes</span></span>       |
| [<span data-ttu-id="406ab-167">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="406ab-167">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="406ab-168">non</span><span class="sxs-lookup"><span data-stu-id="406ab-168">no</span></span>        |
| [<span data-ttu-id="406ab-169">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="406ab-169">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="406ab-170">non</span><span class="sxs-lookup"><span data-stu-id="406ab-170">no</span></span>        |
| [<span data-ttu-id="406ab-171">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="406ab-171">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="406ab-172">non</span><span class="sxs-lookup"><span data-stu-id="406ab-172">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="406ab-173">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="406ab-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="406ab-174">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="406ab-174">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





