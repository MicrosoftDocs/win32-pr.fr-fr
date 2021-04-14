---
title: SinCos, (SM4-ASM)
description: Sin (thêta) et cos (thêta) du composant pour Theta en radians.
ms.assetid: 81FDEC8F-2C1C-4C60-A6DA-699C798F8316
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2dd8fc3b011758f071cdcd273e34eb8a7f6421f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990720"
---
# <a name="sincos-sm4---asm"></a><span data-ttu-id="2f3b4-103">SinCos, (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="2f3b4-103">sincos (sm4 - asm)</span></span>

<span data-ttu-id="2f3b4-104">Sin (thêta) et cos (thêta) du composant pour Theta en radians.</span><span class="sxs-lookup"><span data-stu-id="2f3b4-104">Component-wise sin(theta) and cos(theta) for theta in radians.</span></span>



| <span data-ttu-id="2f3b4-105">SinCos, \[ \_ SAT \] destSIN \[ . Mask \] , destCOS \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="2f3b4-105">sincos\[\_sat\] destSIN\[.mask\], destCOS\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------------------------------|



 



| <span data-ttu-id="2f3b4-106">Élément</span><span class="sxs-lookup"><span data-stu-id="2f3b4-106">Item</span></span>                                                                                               | <span data-ttu-id="2f3b4-107">Description</span><span class="sxs-lookup"><span data-stu-id="2f3b4-107">Description</span></span>                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="2f3b4-108"><span id="destSIN"></span><span id="destsin"></span><span id="DESTSIN"></span>*destSIN*</span><span class="sxs-lookup"><span data-stu-id="2f3b4-108"><span id="destSIN"></span><span id="destsin"></span><span id="DESTSIN"></span>*destSIN*</span></span><br/> | <span data-ttu-id="2f3b4-109">\[dans \] l’adresse de Sin (*src0*), calculée par composant.</span><span class="sxs-lookup"><span data-stu-id="2f3b4-109">\[in\] The address of sin(*src0*), computed per component.</span></span><br/> |
| <span data-ttu-id="2f3b4-110"><span id="destCOS"></span><span id="destcos"></span><span id="DESTCOS"></span>*destCOS*</span><span class="sxs-lookup"><span data-stu-id="2f3b4-110"><span id="destCOS"></span><span id="destcos"></span><span id="DESTCOS"></span>*destCOS*</span></span><br/> | <span data-ttu-id="2f3b4-111">\[dans \] l’adresse cos (*src0*), calculée par composant.</span><span class="sxs-lookup"><span data-stu-id="2f3b4-111">\[in\] The address of cos(*src0*), computed per component.</span></span><br/> |
| <span data-ttu-id="2f3b4-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="2f3b4-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                    | <span data-ttu-id="2f3b4-113">\[dans \] les composants pour lesquels calculer des Sin et des COS.</span><span class="sxs-lookup"><span data-stu-id="2f3b4-113">\[in\] The components for which to compute sin and cos.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="2f3b4-114">Notes</span><span class="sxs-lookup"><span data-stu-id="2f3b4-114">Remarks</span></span>

<span data-ttu-id="2f3b4-115">Si le résultat n’est pas nécessaire, vous pouvez spécifier *destSIN* et *destCOS* comme null au lieu de spécifier un registre.</span><span class="sxs-lookup"><span data-stu-id="2f3b4-115">If the result is not needed, you can specify *destSIN* and *destCOS* as NULL instead of specifying a register.</span></span>

<span data-ttu-id="2f3b4-116">Les valeurs Thêta peuvent être n’importe quelle valeur à virgule flottante IEEE 32 bits.</span><span class="sxs-lookup"><span data-stu-id="2f3b4-116">Theta values can be any IEEE 32-bit floating point values.</span></span>

<span data-ttu-id="2f3b4-117">L’erreur absolue maximale est 0,0008 dans l’intervalle compris entre-100 \* pi et + 100 \* pi.</span><span class="sxs-lookup"><span data-stu-id="2f3b4-117">The maximum absolute error is 0.0008 in the interval from -100\*Pi to +100\*Pi.</span></span>

<span data-ttu-id="2f3b4-118">Le tableau suivant présente les résultats obtenus lors de l’exécution de l’instruction avec différentes classes de nombres.</span><span class="sxs-lookup"><span data-stu-id="2f3b4-118">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>

<span data-ttu-id="2f3b4-119">F signifie nombre fini-réel.</span><span class="sxs-lookup"><span data-stu-id="2f3b4-119">F means finite-real number.</span></span>



|             |          |              |             |        |        |             |              |          |         |
|-------------|----------|--------------|-------------|--------|--------|-------------|--------------|----------|---------|
| <span data-ttu-id="2f3b4-120">**src**</span><span class="sxs-lookup"><span data-stu-id="2f3b4-120">**src**</span></span>     | <span data-ttu-id="2f3b4-121">**-INF**</span><span class="sxs-lookup"><span data-stu-id="2f3b4-121">**-inf**</span></span> | <span data-ttu-id="2f3b4-122">**-F**</span><span class="sxs-lookup"><span data-stu-id="2f3b4-122">**-F**</span></span>       | <span data-ttu-id="2f3b4-123">**-dénorme**</span><span class="sxs-lookup"><span data-stu-id="2f3b4-123">**-denorm**</span></span> | <span data-ttu-id="2f3b4-124">**-0**</span><span class="sxs-lookup"><span data-stu-id="2f3b4-124">**-0**</span></span> | <span data-ttu-id="2f3b4-125">**+0**</span><span class="sxs-lookup"><span data-stu-id="2f3b4-125">**+0**</span></span> | <span data-ttu-id="2f3b4-126">**+ dénorme**</span><span class="sxs-lookup"><span data-stu-id="2f3b4-126">**+denorm**</span></span> | <span data-ttu-id="2f3b4-127">**+ F**</span><span class="sxs-lookup"><span data-stu-id="2f3b4-127">**+F**</span></span>       | <span data-ttu-id="2f3b4-128">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="2f3b4-128">**+inf**</span></span> | <span data-ttu-id="2f3b4-129">**NaN**</span><span class="sxs-lookup"><span data-stu-id="2f3b4-129">**NaN**</span></span> |
| <span data-ttu-id="2f3b4-130">**destSIN**</span><span class="sxs-lookup"><span data-stu-id="2f3b4-130">**destSIN**</span></span> | <span data-ttu-id="2f3b4-131">NaN</span><span class="sxs-lookup"><span data-stu-id="2f3b4-131">NaN</span></span>      | <span data-ttu-id="2f3b4-132">\[-1 à + 1\]</span><span class="sxs-lookup"><span data-stu-id="2f3b4-132">\[-1 to +1\]</span></span> | <span data-ttu-id="2f3b4-133">-0</span><span class="sxs-lookup"><span data-stu-id="2f3b4-133">-0</span></span>          | <span data-ttu-id="2f3b4-134">-0</span><span class="sxs-lookup"><span data-stu-id="2f3b4-134">-0</span></span>     | <span data-ttu-id="2f3b4-135">+0</span><span class="sxs-lookup"><span data-stu-id="2f3b4-135">+0</span></span>     | <span data-ttu-id="2f3b4-136">+0</span><span class="sxs-lookup"><span data-stu-id="2f3b4-136">+0</span></span>          | <span data-ttu-id="2f3b4-137">\[-1 à + 1\]</span><span class="sxs-lookup"><span data-stu-id="2f3b4-137">\[-1 to +1\]</span></span> | <span data-ttu-id="2f3b4-138">NaN</span><span class="sxs-lookup"><span data-stu-id="2f3b4-138">NaN</span></span>      | <span data-ttu-id="2f3b4-139">NaN</span><span class="sxs-lookup"><span data-stu-id="2f3b4-139">NaN</span></span>     |
| <span data-ttu-id="2f3b4-140">**destCOS**</span><span class="sxs-lookup"><span data-stu-id="2f3b4-140">**destCOS**</span></span> | <span data-ttu-id="2f3b4-141">NaN</span><span class="sxs-lookup"><span data-stu-id="2f3b4-141">NaN</span></span>      | <span data-ttu-id="2f3b4-142">\[-1 à + 1\]</span><span class="sxs-lookup"><span data-stu-id="2f3b4-142">\[-1 to +1\]</span></span> | <span data-ttu-id="2f3b4-143">+1</span><span class="sxs-lookup"><span data-stu-id="2f3b4-143">+1</span></span>          | <span data-ttu-id="2f3b4-144">+1</span><span class="sxs-lookup"><span data-stu-id="2f3b4-144">+1</span></span>     | <span data-ttu-id="2f3b4-145">+1</span><span class="sxs-lookup"><span data-stu-id="2f3b4-145">+1</span></span>     | <span data-ttu-id="2f3b4-146">+1</span><span class="sxs-lookup"><span data-stu-id="2f3b4-146">+1</span></span>          | <span data-ttu-id="2f3b4-147">\[-1 à + 1\]</span><span class="sxs-lookup"><span data-stu-id="2f3b4-147">\[-1 to +1\]</span></span> | <span data-ttu-id="2f3b4-148">NaN</span><span class="sxs-lookup"><span data-stu-id="2f3b4-148">NaN</span></span>      | <span data-ttu-id="2f3b4-149">NaN</span><span class="sxs-lookup"><span data-stu-id="2f3b4-149">NaN</span></span>     |



 

<span data-ttu-id="2f3b4-150">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="2f3b4-150">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2f3b4-151">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="2f3b4-151">Vertex Shader</span></span> | <span data-ttu-id="2f3b4-152">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="2f3b4-152">Geometry Shader</span></span> | <span data-ttu-id="2f3b4-153">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="2f3b4-153">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="2f3b4-154">x</span><span class="sxs-lookup"><span data-stu-id="2f3b4-154">x</span></span>             | <span data-ttu-id="2f3b4-155">x</span><span class="sxs-lookup"><span data-stu-id="2f3b4-155">x</span></span>               | <span data-ttu-id="2f3b4-156">x</span><span class="sxs-lookup"><span data-stu-id="2f3b4-156">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2f3b4-157">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="2f3b4-157">Minimum Shader Model</span></span>

<span data-ttu-id="2f3b4-158">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="2f3b4-158">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2f3b4-159">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="2f3b4-159">Shader Model</span></span>                                              | <span data-ttu-id="2f3b4-160">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="2f3b4-160">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2f3b4-161">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="2f3b4-161">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2f3b4-162">Oui</span><span class="sxs-lookup"><span data-stu-id="2f3b4-162">yes</span></span>       |
| [<span data-ttu-id="2f3b4-163">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="2f3b4-163">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2f3b4-164">Oui</span><span class="sxs-lookup"><span data-stu-id="2f3b4-164">yes</span></span>       |
| [<span data-ttu-id="2f3b4-165">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="2f3b4-165">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2f3b4-166">Oui</span><span class="sxs-lookup"><span data-stu-id="2f3b4-166">yes</span></span>       |
| [<span data-ttu-id="2f3b4-167">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2f3b4-167">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2f3b4-168">non</span><span class="sxs-lookup"><span data-stu-id="2f3b4-168">no</span></span>        |
| [<span data-ttu-id="2f3b4-169">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2f3b4-169">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2f3b4-170">non</span><span class="sxs-lookup"><span data-stu-id="2f3b4-170">no</span></span>        |
| [<span data-ttu-id="2f3b4-171">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2f3b4-171">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2f3b4-172">non</span><span class="sxs-lookup"><span data-stu-id="2f3b4-172">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2f3b4-173">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2f3b4-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f3b4-174">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2f3b4-174">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





