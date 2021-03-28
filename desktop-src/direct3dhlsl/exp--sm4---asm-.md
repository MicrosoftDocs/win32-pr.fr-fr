---
title: exp (SM4-ASM)
description: 2exponent au niveau du composant.
ms.assetid: 12EB865A-BF71-4B4B-854F-9DA056B18AE0
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 774be1230bdb02a6179ea5662ca2237c2cefc200
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104030558"
---
# <a name="exp-sm4---asm"></a><span data-ttu-id="0e632-103">exp (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="0e632-103">exp (sm4 - asm)</span></span>

<span data-ttu-id="0e632-104">2exponent au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="0e632-104">Component-wise 2exponent.</span></span>



| <span data-ttu-id="0e632-105">exp \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="0e632-105">exp\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="0e632-106">Élément</span><span class="sxs-lookup"><span data-stu-id="0e632-106">Item</span></span>                                                            | <span data-ttu-id="0e632-107">Description</span><span class="sxs-lookup"><span data-stu-id="0e632-107">Description</span></span>                                                                |
|-----------------------------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="0e632-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="0e632-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="0e632-109">\[dans \] le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="0e632-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="0e632-110">*dest* = 2 *src0*</span><span class="sxs-lookup"><span data-stu-id="0e632-110">*dest* = 2 *src0*</span></span><br/> |
| <span data-ttu-id="0e632-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="0e632-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="0e632-112">\[dans \] l’exposant.</span><span class="sxs-lookup"><span data-stu-id="0e632-112">\[in\] The exponent.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="0e632-113">Notes</span><span class="sxs-lookup"><span data-stu-id="0e632-113">Remarks</span></span>

<span data-ttu-id="0e632-114">Cette instruction suit la théorie des limites.</span><span class="sxs-lookup"><span data-stu-id="0e632-114">This instruction follows limit theory.</span></span> <span data-ttu-id="0e632-115">L’erreur relative maximale est 2-21.</span><span class="sxs-lookup"><span data-stu-id="0e632-115">The maximum relative error is 2-21.</span></span>

<span data-ttu-id="0e632-116">Le tableau suivant présente les résultats obtenus lors de l’exécution de l’instruction avec différentes classes de nombres, en supposant qu’aucun dépassement de capacité ou négatif ne se produit.</span><span class="sxs-lookup"><span data-stu-id="0e632-116">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="0e632-117">Dans ce tableau, F signifie nombre fini-réel.</span><span class="sxs-lookup"><span data-stu-id="0e632-117">In this table F means finite-real number.</span></span>



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="0e632-118">**src**</span><span class="sxs-lookup"><span data-stu-id="0e632-118">**src**</span></span>  | <span data-ttu-id="0e632-119">**-INF**</span><span class="sxs-lookup"><span data-stu-id="0e632-119">**-inf**</span></span> | <span data-ttu-id="0e632-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="0e632-120">**-F**</span></span> | <span data-ttu-id="0e632-121">**-dénorme**</span><span class="sxs-lookup"><span data-stu-id="0e632-121">**-denorm**</span></span> | <span data-ttu-id="0e632-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="0e632-122">**-0**</span></span> | <span data-ttu-id="0e632-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="0e632-123">**+0**</span></span> | <span data-ttu-id="0e632-124">**+ dénorme**</span><span class="sxs-lookup"><span data-stu-id="0e632-124">**+denorm**</span></span> | <span data-ttu-id="0e632-125">**+ F**</span><span class="sxs-lookup"><span data-stu-id="0e632-125">**+F**</span></span> | <span data-ttu-id="0e632-126">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="0e632-126">**+inf**</span></span> | <span data-ttu-id="0e632-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="0e632-127">**NaN**</span></span> |
| <span data-ttu-id="0e632-128">**dest**</span><span class="sxs-lookup"><span data-stu-id="0e632-128">**dest**</span></span> | <span data-ttu-id="0e632-129">0</span><span class="sxs-lookup"><span data-stu-id="0e632-129">0</span></span>        | <span data-ttu-id="0e632-130">+ F</span><span class="sxs-lookup"><span data-stu-id="0e632-130">+F</span></span>     | <span data-ttu-id="0e632-131">1</span><span class="sxs-lookup"><span data-stu-id="0e632-131">1</span></span>           | <span data-ttu-id="0e632-132">1</span><span class="sxs-lookup"><span data-stu-id="0e632-132">1</span></span>      | <span data-ttu-id="0e632-133">1</span><span class="sxs-lookup"><span data-stu-id="0e632-133">1</span></span>      | <span data-ttu-id="0e632-134">1</span><span class="sxs-lookup"><span data-stu-id="0e632-134">1</span></span>           | <span data-ttu-id="0e632-135">+ F</span><span class="sxs-lookup"><span data-stu-id="0e632-135">+F</span></span>     | <span data-ttu-id="0e632-136">+inf</span><span class="sxs-lookup"><span data-stu-id="0e632-136">+inf</span></span>     | <span data-ttu-id="0e632-137">NaN</span><span class="sxs-lookup"><span data-stu-id="0e632-137">NaN</span></span>     |



 

<span data-ttu-id="0e632-138">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="0e632-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0e632-139">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="0e632-139">Vertex Shader</span></span> | <span data-ttu-id="0e632-140">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="0e632-140">Geometry Shader</span></span> | <span data-ttu-id="0e632-141">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="0e632-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="0e632-142">x</span><span class="sxs-lookup"><span data-stu-id="0e632-142">x</span></span>             | <span data-ttu-id="0e632-143">x</span><span class="sxs-lookup"><span data-stu-id="0e632-143">x</span></span>               | <span data-ttu-id="0e632-144">x</span><span class="sxs-lookup"><span data-stu-id="0e632-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0e632-145">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="0e632-145">Minimum Shader Model</span></span>

<span data-ttu-id="0e632-146">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="0e632-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0e632-147">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="0e632-147">Shader Model</span></span>                                              | <span data-ttu-id="0e632-148">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="0e632-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0e632-149">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="0e632-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0e632-150">Oui</span><span class="sxs-lookup"><span data-stu-id="0e632-150">yes</span></span>       |
| [<span data-ttu-id="0e632-151">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="0e632-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0e632-152">Oui</span><span class="sxs-lookup"><span data-stu-id="0e632-152">yes</span></span>       |
| [<span data-ttu-id="0e632-153">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="0e632-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0e632-154">Oui</span><span class="sxs-lookup"><span data-stu-id="0e632-154">yes</span></span>       |
| [<span data-ttu-id="0e632-155">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0e632-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0e632-156">non</span><span class="sxs-lookup"><span data-stu-id="0e632-156">no</span></span>        |
| [<span data-ttu-id="0e632-157">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0e632-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0e632-158">non</span><span class="sxs-lookup"><span data-stu-id="0e632-158">no</span></span>        |
| [<span data-ttu-id="0e632-159">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0e632-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0e632-160">non</span><span class="sxs-lookup"><span data-stu-id="0e632-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="0e632-161">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0e632-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e632-162">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0e632-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





