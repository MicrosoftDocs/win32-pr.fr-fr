---
title: SinCos, (SM4-ASM)
description: Sin (thêta) et cos (thêta) du composant pour Theta en radians.
ms.assetid: 81FDEC8F-2C1C-4C60-A6DA-699C798F8316
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c03118ff9a1fc2d958eaa6eb1a550a6dbf672a2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997016"
---
# <a name="sincos-sm4---asm"></a><span data-ttu-id="a2d08-103">SinCos, (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="a2d08-103">sincos (sm4 - asm)</span></span>

<span data-ttu-id="a2d08-104">Sin (thêta) et cos (thêta) du composant pour Theta en radians.</span><span class="sxs-lookup"><span data-stu-id="a2d08-104">Component-wise sin(theta) and cos(theta) for theta in radians.</span></span>



| <span data-ttu-id="a2d08-105">SinCos, \[ \_ SAT \] destSIN \[ . Mask \] , destCOS \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="a2d08-105">sincos\[\_sat\] destSIN\[.mask\], destCOS\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------------------------------|



 



| <span data-ttu-id="a2d08-106">Élément</span><span class="sxs-lookup"><span data-stu-id="a2d08-106">Item</span></span>                                                                                               | <span data-ttu-id="a2d08-107">Description</span><span class="sxs-lookup"><span data-stu-id="a2d08-107">Description</span></span>                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="a2d08-108"><span id="destSIN"></span><span id="destsin"></span><span id="DESTSIN"></span>*destSIN*</span><span class="sxs-lookup"><span data-stu-id="a2d08-108"><span id="destSIN"></span><span id="destsin"></span><span id="DESTSIN"></span>*destSIN*</span></span><br/> | <span data-ttu-id="a2d08-109">\[dans \] l’adresse de Sin (*src0*), calculée par composant.</span><span class="sxs-lookup"><span data-stu-id="a2d08-109">\[in\] The address of sin(*src0*), computed per component.</span></span><br/> |
| <span data-ttu-id="a2d08-110"><span id="destCOS"></span><span id="destcos"></span><span id="DESTCOS"></span>*destCOS*</span><span class="sxs-lookup"><span data-stu-id="a2d08-110"><span id="destCOS"></span><span id="destcos"></span><span id="DESTCOS"></span>*destCOS*</span></span><br/> | <span data-ttu-id="a2d08-111">\[dans \] l’adresse cos (*src0*), calculée par composant.</span><span class="sxs-lookup"><span data-stu-id="a2d08-111">\[in\] The address of cos(*src0*), computed per component.</span></span><br/> |
| <span data-ttu-id="a2d08-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="a2d08-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                    | <span data-ttu-id="a2d08-113">\[dans \] les composants pour lesquels calculer des Sin et des COS.</span><span class="sxs-lookup"><span data-stu-id="a2d08-113">\[in\] The components for which to compute sin and cos.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="a2d08-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="a2d08-114">Remarks</span></span>

<span data-ttu-id="a2d08-115">Si le résultat n’est pas nécessaire, vous pouvez spécifier *destSIN* et *destCOS* comme null au lieu de spécifier un registre.</span><span class="sxs-lookup"><span data-stu-id="a2d08-115">If the result is not needed, you can specify *destSIN* and *destCOS* as NULL instead of specifying a register.</span></span>

<span data-ttu-id="a2d08-116">Les valeurs Thêta peuvent être n’importe quelle valeur à virgule flottante IEEE 32 bits.</span><span class="sxs-lookup"><span data-stu-id="a2d08-116">Theta values can be any IEEE 32-bit floating point values.</span></span>

<span data-ttu-id="a2d08-117">L’erreur absolue maximale est 0,0008 dans l’intervalle compris entre-100 \* pi et + 100 \* pi.</span><span class="sxs-lookup"><span data-stu-id="a2d08-117">The maximum absolute error is 0.0008 in the interval from -100\*Pi to +100\*Pi.</span></span>

<span data-ttu-id="a2d08-118">Le tableau suivant présente les résultats obtenus lors de l’exécution de l’instruction avec différentes classes de nombres.</span><span class="sxs-lookup"><span data-stu-id="a2d08-118">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>

<span data-ttu-id="a2d08-119">F signifie nombre fini-réel.</span><span class="sxs-lookup"><span data-stu-id="a2d08-119">F means finite-real number.</span></span>



| <span data-ttu-id="a2d08-120">**src**</span><span class="sxs-lookup"><span data-stu-id="a2d08-120">**src**</span></span>     | <span data-ttu-id="a2d08-121">**-INF**</span><span class="sxs-lookup"><span data-stu-id="a2d08-121">**-inf**</span></span> | <span data-ttu-id="a2d08-122">**-F**</span><span class="sxs-lookup"><span data-stu-id="a2d08-122">**-F**</span></span>       | <span data-ttu-id="a2d08-123">**-dénorme**</span><span class="sxs-lookup"><span data-stu-id="a2d08-123">**-denorm**</span></span> | <span data-ttu-id="a2d08-124">**-0**</span><span class="sxs-lookup"><span data-stu-id="a2d08-124">**-0**</span></span> | <span data-ttu-id="a2d08-125">**+0**</span><span class="sxs-lookup"><span data-stu-id="a2d08-125">**+0**</span></span> | <span data-ttu-id="a2d08-126">**+ dénorme**</span><span class="sxs-lookup"><span data-stu-id="a2d08-126">**+denorm**</span></span> | <span data-ttu-id="a2d08-127">**+ F**</span><span class="sxs-lookup"><span data-stu-id="a2d08-127">**+F**</span></span>       | <span data-ttu-id="a2d08-128">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="a2d08-128">**+inf**</span></span> | <span data-ttu-id="a2d08-129">**NaN**</span><span class="sxs-lookup"><span data-stu-id="a2d08-129">**NaN**</span></span> |
|-------------|----------|--------------|-------------|--------|--------|-------------|--------------|----------|---------|
| <span data-ttu-id="a2d08-130">**destSIN**</span><span class="sxs-lookup"><span data-stu-id="a2d08-130">**destSIN**</span></span> | <span data-ttu-id="a2d08-131">NaN</span><span class="sxs-lookup"><span data-stu-id="a2d08-131">NaN</span></span>      | <span data-ttu-id="a2d08-132">\[-1 à + 1\]</span><span class="sxs-lookup"><span data-stu-id="a2d08-132">\[-1 to +1\]</span></span> | <span data-ttu-id="a2d08-133">-0</span><span class="sxs-lookup"><span data-stu-id="a2d08-133">-0</span></span>          | <span data-ttu-id="a2d08-134">-0</span><span class="sxs-lookup"><span data-stu-id="a2d08-134">-0</span></span>     | <span data-ttu-id="a2d08-135">+0</span><span class="sxs-lookup"><span data-stu-id="a2d08-135">+0</span></span>     | <span data-ttu-id="a2d08-136">+0</span><span class="sxs-lookup"><span data-stu-id="a2d08-136">+0</span></span>          | <span data-ttu-id="a2d08-137">\[-1 à + 1\]</span><span class="sxs-lookup"><span data-stu-id="a2d08-137">\[-1 to +1\]</span></span> | <span data-ttu-id="a2d08-138">NaN</span><span class="sxs-lookup"><span data-stu-id="a2d08-138">NaN</span></span>      | <span data-ttu-id="a2d08-139">NaN</span><span class="sxs-lookup"><span data-stu-id="a2d08-139">NaN</span></span>     |
| <span data-ttu-id="a2d08-140">**destCOS**</span><span class="sxs-lookup"><span data-stu-id="a2d08-140">**destCOS**</span></span> | <span data-ttu-id="a2d08-141">NaN</span><span class="sxs-lookup"><span data-stu-id="a2d08-141">NaN</span></span>      | <span data-ttu-id="a2d08-142">\[-1 à + 1\]</span><span class="sxs-lookup"><span data-stu-id="a2d08-142">\[-1 to +1\]</span></span> | <span data-ttu-id="a2d08-143">+1</span><span class="sxs-lookup"><span data-stu-id="a2d08-143">+1</span></span>          | <span data-ttu-id="a2d08-144">+1</span><span class="sxs-lookup"><span data-stu-id="a2d08-144">+1</span></span>     | <span data-ttu-id="a2d08-145">+1</span><span class="sxs-lookup"><span data-stu-id="a2d08-145">+1</span></span>     | <span data-ttu-id="a2d08-146">+1</span><span class="sxs-lookup"><span data-stu-id="a2d08-146">+1</span></span>          | <span data-ttu-id="a2d08-147">\[-1 à + 1\]</span><span class="sxs-lookup"><span data-stu-id="a2d08-147">\[-1 to +1\]</span></span> | <span data-ttu-id="a2d08-148">NaN</span><span class="sxs-lookup"><span data-stu-id="a2d08-148">NaN</span></span>      | <span data-ttu-id="a2d08-149">NaN</span><span class="sxs-lookup"><span data-stu-id="a2d08-149">NaN</span></span>     |



 

<span data-ttu-id="a2d08-150">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="a2d08-150">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a2d08-151">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="a2d08-151">Vertex Shader</span></span> | <span data-ttu-id="a2d08-152">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="a2d08-152">Geometry Shader</span></span> | <span data-ttu-id="a2d08-153">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="a2d08-153">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="a2d08-154">x</span><span class="sxs-lookup"><span data-stu-id="a2d08-154">x</span></span>             | <span data-ttu-id="a2d08-155">x</span><span class="sxs-lookup"><span data-stu-id="a2d08-155">x</span></span>               | <span data-ttu-id="a2d08-156">x</span><span class="sxs-lookup"><span data-stu-id="a2d08-156">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a2d08-157">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="a2d08-157">Minimum Shader Model</span></span>

<span data-ttu-id="a2d08-158">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="a2d08-158">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a2d08-159">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="a2d08-159">Shader Model</span></span>                                              | <span data-ttu-id="a2d08-160">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2d08-160">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a2d08-161">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="a2d08-161">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a2d08-162">oui</span><span class="sxs-lookup"><span data-stu-id="a2d08-162">yes</span></span>       |
| [<span data-ttu-id="a2d08-163">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="a2d08-163">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a2d08-164">oui</span><span class="sxs-lookup"><span data-stu-id="a2d08-164">yes</span></span>       |
| [<span data-ttu-id="a2d08-165">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="a2d08-165">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a2d08-166">oui</span><span class="sxs-lookup"><span data-stu-id="a2d08-166">yes</span></span>       |
| [<span data-ttu-id="a2d08-167">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a2d08-167">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a2d08-168">non</span><span class="sxs-lookup"><span data-stu-id="a2d08-168">no</span></span>        |
| [<span data-ttu-id="a2d08-169">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a2d08-169">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a2d08-170">non</span><span class="sxs-lookup"><span data-stu-id="a2d08-170">no</span></span>        |
| [<span data-ttu-id="a2d08-171">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a2d08-171">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a2d08-172">non</span><span class="sxs-lookup"><span data-stu-id="a2d08-172">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a2d08-173">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a2d08-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2d08-174">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a2d08-174">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





