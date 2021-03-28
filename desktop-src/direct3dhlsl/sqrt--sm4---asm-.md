---
title: sqrt (SM4-ASM)
description: Racine carrée au niveau du composant.
ms.assetid: B860D656-7F01-484F-909F-A5C9A61C52C3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0a12afaf5b2366dac15c953d509a6814b48a6b9
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381177"
---
# <a name="sqrt-sm4---asm"></a><span data-ttu-id="7f373-103">sqrt (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="7f373-103">sqrt (sm4 - asm)</span></span>

<span data-ttu-id="7f373-104">Racine carrée au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="7f373-104">Component-wise square root.</span></span>



| <span data-ttu-id="7f373-105">sqrt \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="7f373-105">sqrt\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="7f373-106">Élément</span><span class="sxs-lookup"><span data-stu-id="7f373-106">Item</span></span>                                                            | <span data-ttu-id="7f373-107">Description</span><span class="sxs-lookup"><span data-stu-id="7f373-107">Description</span></span>                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="7f373-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="7f373-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="7f373-109">\[dans \] le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="7f373-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="7f373-110">*dest* = sqrt (*src0*)</span><span class="sxs-lookup"><span data-stu-id="7f373-110">*dest* = sqrt(*src0*)</span></span><br/> |
| <span data-ttu-id="7f373-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="7f373-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="7f373-112">\[dans \] les composants pour lesquels prendre la racine carrée.</span><span class="sxs-lookup"><span data-stu-id="7f373-112">\[in\] The components for which to take the square root.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="7f373-113">Notes</span><span class="sxs-lookup"><span data-stu-id="7f373-113">Remarks</span></span>

<span data-ttu-id="7f373-114">La précision est 1 ULP.</span><span class="sxs-lookup"><span data-stu-id="7f373-114">Precision is 1 ulp.</span></span>

<span data-ttu-id="7f373-115">Le tableau suivant présente les résultats obtenus lors de l’exécution de l’instruction avec différentes classes de nombres, en supposant qu’aucun dépassement de capacité ou négatif ne se produit.</span><span class="sxs-lookup"><span data-stu-id="7f373-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="7f373-116">F signifie nombre fini-réel.</span><span class="sxs-lookup"><span data-stu-id="7f373-116">F means finite-real number.</span></span>



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
|          | <span data-ttu-id="7f373-117">**-INF**</span><span class="sxs-lookup"><span data-stu-id="7f373-117">**-inf**</span></span> | <span data-ttu-id="7f373-118">**-F**</span><span class="sxs-lookup"><span data-stu-id="7f373-118">**-F**</span></span> | <span data-ttu-id="7f373-119">**-dénorme**</span><span class="sxs-lookup"><span data-stu-id="7f373-119">**-denorm**</span></span> | <span data-ttu-id="7f373-120">**-0**</span><span class="sxs-lookup"><span data-stu-id="7f373-120">**-0**</span></span> | <span data-ttu-id="7f373-121">**+0**</span><span class="sxs-lookup"><span data-stu-id="7f373-121">**+0**</span></span> | <span data-ttu-id="7f373-122">**+ dénorme**</span><span class="sxs-lookup"><span data-stu-id="7f373-122">**+denorm**</span></span> | <span data-ttu-id="7f373-123">**+ F**</span><span class="sxs-lookup"><span data-stu-id="7f373-123">**+F**</span></span> | <span data-ttu-id="7f373-124">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="7f373-124">**+inf**</span></span> | <span data-ttu-id="7f373-125">**NaN**</span><span class="sxs-lookup"><span data-stu-id="7f373-125">**NaN**</span></span> |
| <span data-ttu-id="7f373-126">**dest**</span><span class="sxs-lookup"><span data-stu-id="7f373-126">**dest**</span></span> | <span data-ttu-id="7f373-127">NaN</span><span class="sxs-lookup"><span data-stu-id="7f373-127">NaN</span></span>      | <span data-ttu-id="7f373-128">NaN</span><span class="sxs-lookup"><span data-stu-id="7f373-128">NaN</span></span>    | <span data-ttu-id="7f373-129">-0</span><span class="sxs-lookup"><span data-stu-id="7f373-129">-0</span></span>          | <span data-ttu-id="7f373-130">-0</span><span class="sxs-lookup"><span data-stu-id="7f373-130">-0</span></span>     | <span data-ttu-id="7f373-131">+0</span><span class="sxs-lookup"><span data-stu-id="7f373-131">+0</span></span>     | <span data-ttu-id="7f373-132">+0</span><span class="sxs-lookup"><span data-stu-id="7f373-132">+0</span></span>          | <span data-ttu-id="7f373-133">+ F</span><span class="sxs-lookup"><span data-stu-id="7f373-133">+F</span></span>     | <span data-ttu-id="7f373-134">+inf</span><span class="sxs-lookup"><span data-stu-id="7f373-134">+inf</span></span>     | <span data-ttu-id="7f373-135">NaN</span><span class="sxs-lookup"><span data-stu-id="7f373-135">NaN</span></span>     |



 

<span data-ttu-id="7f373-136">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="7f373-136">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="7f373-137">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="7f373-137">Vertex Shader</span></span> | <span data-ttu-id="7f373-138">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="7f373-138">Geometry Shader</span></span> | <span data-ttu-id="7f373-139">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="7f373-139">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="7f373-140">x</span><span class="sxs-lookup"><span data-stu-id="7f373-140">x</span></span>             | <span data-ttu-id="7f373-141">x</span><span class="sxs-lookup"><span data-stu-id="7f373-141">x</span></span>               | <span data-ttu-id="7f373-142">x</span><span class="sxs-lookup"><span data-stu-id="7f373-142">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7f373-143">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="7f373-143">Minimum Shader Model</span></span>

<span data-ttu-id="7f373-144">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="7f373-144">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7f373-145">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="7f373-145">Shader Model</span></span>                                              | <span data-ttu-id="7f373-146">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="7f373-146">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="7f373-147">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="7f373-147">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="7f373-148">Oui</span><span class="sxs-lookup"><span data-stu-id="7f373-148">yes</span></span>       |
| [<span data-ttu-id="7f373-149">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="7f373-149">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="7f373-150">Oui</span><span class="sxs-lookup"><span data-stu-id="7f373-150">yes</span></span>       |
| [<span data-ttu-id="7f373-151">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="7f373-151">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="7f373-152">Oui</span><span class="sxs-lookup"><span data-stu-id="7f373-152">yes</span></span>       |
| [<span data-ttu-id="7f373-153">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7f373-153">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="7f373-154">non</span><span class="sxs-lookup"><span data-stu-id="7f373-154">no</span></span>        |
| [<span data-ttu-id="7f373-155">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7f373-155">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="7f373-156">non</span><span class="sxs-lookup"><span data-stu-id="7f373-156">no</span></span>        |
| [<span data-ttu-id="7f373-157">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7f373-157">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="7f373-158">non</span><span class="sxs-lookup"><span data-stu-id="7f373-158">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="7f373-159">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7f373-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f373-160">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7f373-160">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





