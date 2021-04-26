---
title: exp (SM4-ASM)
description: 2exponent au niveau du composant.
ms.assetid: 12EB865A-BF71-4B4B-854F-9DA056B18AE0
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b24c74394a5e8ac7a6c945e2c9b63e6f242daa1
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999076"
---
# <a name="exp-sm4---asm"></a><span data-ttu-id="3a5d3-103">exp (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="3a5d3-103">exp (sm4 - asm)</span></span>

<span data-ttu-id="3a5d3-104">2exponent au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="3a5d3-104">Component-wise 2exponent.</span></span>



| <span data-ttu-id="3a5d3-105">exp \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="3a5d3-105">exp\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="3a5d3-106">Élément</span><span class="sxs-lookup"><span data-stu-id="3a5d3-106">Item</span></span>                                                            | <span data-ttu-id="3a5d3-107">Description</span><span class="sxs-lookup"><span data-stu-id="3a5d3-107">Description</span></span>                                                                |
|-----------------------------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="3a5d3-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="3a5d3-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="3a5d3-109">\[dans \] le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="3a5d3-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="3a5d3-110">*dest* = 2 *src0*</span><span class="sxs-lookup"><span data-stu-id="3a5d3-110">*dest* = 2 *src0*</span></span><br/> |
| <span data-ttu-id="3a5d3-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="3a5d3-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="3a5d3-112">\[dans \] l’exposant.</span><span class="sxs-lookup"><span data-stu-id="3a5d3-112">\[in\] The exponent.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="3a5d3-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="3a5d3-113">Remarks</span></span>

<span data-ttu-id="3a5d3-114">Cette instruction suit la théorie des limites.</span><span class="sxs-lookup"><span data-stu-id="3a5d3-114">This instruction follows limit theory.</span></span> <span data-ttu-id="3a5d3-115">L’erreur relative maximale est 2-21.</span><span class="sxs-lookup"><span data-stu-id="3a5d3-115">The maximum relative error is 2-21.</span></span>

<span data-ttu-id="3a5d3-116">Le tableau suivant présente les résultats obtenus lors de l’exécution de l’instruction avec différentes classes de nombres, en supposant qu’aucun dépassement de capacité ou négatif ne se produit.</span><span class="sxs-lookup"><span data-stu-id="3a5d3-116">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="3a5d3-117">Dans ce tableau, F signifie nombre fini-réel.</span><span class="sxs-lookup"><span data-stu-id="3a5d3-117">In this table F means finite-real number.</span></span>



| <span data-ttu-id="3a5d3-118">**src**</span><span class="sxs-lookup"><span data-stu-id="3a5d3-118">**src**</span></span>  | <span data-ttu-id="3a5d3-119">**-INF**</span><span class="sxs-lookup"><span data-stu-id="3a5d3-119">**-inf**</span></span> | <span data-ttu-id="3a5d3-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="3a5d3-120">**-F**</span></span> | <span data-ttu-id="3a5d3-121">**-dénorme**</span><span class="sxs-lookup"><span data-stu-id="3a5d3-121">**-denorm**</span></span> | <span data-ttu-id="3a5d3-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="3a5d3-122">**-0**</span></span> | <span data-ttu-id="3a5d3-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="3a5d3-123">**+0**</span></span> | <span data-ttu-id="3a5d3-124">**+ dénorme**</span><span class="sxs-lookup"><span data-stu-id="3a5d3-124">**+denorm**</span></span> | <span data-ttu-id="3a5d3-125">**+ F**</span><span class="sxs-lookup"><span data-stu-id="3a5d3-125">**+F**</span></span> | <span data-ttu-id="3a5d3-126">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="3a5d3-126">**+inf**</span></span> | <span data-ttu-id="3a5d3-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="3a5d3-127">**NaN**</span></span> |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="3a5d3-128">**dest**</span><span class="sxs-lookup"><span data-stu-id="3a5d3-128">**dest**</span></span> | <span data-ttu-id="3a5d3-129">0</span><span class="sxs-lookup"><span data-stu-id="3a5d3-129">0</span></span>        | <span data-ttu-id="3a5d3-130">+ F</span><span class="sxs-lookup"><span data-stu-id="3a5d3-130">+F</span></span>     | <span data-ttu-id="3a5d3-131">1</span><span class="sxs-lookup"><span data-stu-id="3a5d3-131">1</span></span>           | <span data-ttu-id="3a5d3-132">1</span><span class="sxs-lookup"><span data-stu-id="3a5d3-132">1</span></span>      | <span data-ttu-id="3a5d3-133">1</span><span class="sxs-lookup"><span data-stu-id="3a5d3-133">1</span></span>      | <span data-ttu-id="3a5d3-134">1</span><span class="sxs-lookup"><span data-stu-id="3a5d3-134">1</span></span>           | <span data-ttu-id="3a5d3-135">+ F</span><span class="sxs-lookup"><span data-stu-id="3a5d3-135">+F</span></span>     | <span data-ttu-id="3a5d3-136">+inf</span><span class="sxs-lookup"><span data-stu-id="3a5d3-136">+inf</span></span>     | <span data-ttu-id="3a5d3-137">NaN</span><span class="sxs-lookup"><span data-stu-id="3a5d3-137">NaN</span></span>     |



 

<span data-ttu-id="3a5d3-138">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="3a5d3-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="3a5d3-139">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="3a5d3-139">Vertex Shader</span></span> | <span data-ttu-id="3a5d3-140">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="3a5d3-140">Geometry Shader</span></span> | <span data-ttu-id="3a5d3-141">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="3a5d3-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="3a5d3-142">x</span><span class="sxs-lookup"><span data-stu-id="3a5d3-142">x</span></span>             | <span data-ttu-id="3a5d3-143">x</span><span class="sxs-lookup"><span data-stu-id="3a5d3-143">x</span></span>               | <span data-ttu-id="3a5d3-144">x</span><span class="sxs-lookup"><span data-stu-id="3a5d3-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3a5d3-145">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="3a5d3-145">Minimum Shader Model</span></span>

<span data-ttu-id="3a5d3-146">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="3a5d3-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3a5d3-147">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="3a5d3-147">Shader Model</span></span>                                              | <span data-ttu-id="3a5d3-148">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a5d3-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="3a5d3-149">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="3a5d3-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="3a5d3-150">oui</span><span class="sxs-lookup"><span data-stu-id="3a5d3-150">yes</span></span>       |
| [<span data-ttu-id="3a5d3-151">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="3a5d3-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="3a5d3-152">oui</span><span class="sxs-lookup"><span data-stu-id="3a5d3-152">yes</span></span>       |
| [<span data-ttu-id="3a5d3-153">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="3a5d3-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="3a5d3-154">oui</span><span class="sxs-lookup"><span data-stu-id="3a5d3-154">yes</span></span>       |
| [<span data-ttu-id="3a5d3-155">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3a5d3-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="3a5d3-156">non</span><span class="sxs-lookup"><span data-stu-id="3a5d3-156">no</span></span>        |
| [<span data-ttu-id="3a5d3-157">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3a5d3-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="3a5d3-158">non</span><span class="sxs-lookup"><span data-stu-id="3a5d3-158">no</span></span>        |
| [<span data-ttu-id="3a5d3-159">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3a5d3-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="3a5d3-160">non</span><span class="sxs-lookup"><span data-stu-id="3a5d3-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="3a5d3-161">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3a5d3-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a5d3-162">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3a5d3-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





