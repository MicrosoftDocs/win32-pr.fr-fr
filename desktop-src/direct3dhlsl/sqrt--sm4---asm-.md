---
title: sqrt (SM4-ASM)
description: Racine carrée au niveau du composant.
ms.assetid: B860D656-7F01-484F-909F-A5C9A61C52C3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 628601e0a3a78784a5fd1a089ef7608a0cf9ca05
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996606"
---
# <a name="sqrt-sm4---asm"></a><span data-ttu-id="5c537-103">sqrt (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="5c537-103">sqrt (sm4 - asm)</span></span>

<span data-ttu-id="5c537-104">Racine carrée au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="5c537-104">Component-wise square root.</span></span>



| <span data-ttu-id="5c537-105">sqrt \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="5c537-105">sqrt\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="5c537-106">Élément</span><span class="sxs-lookup"><span data-stu-id="5c537-106">Item</span></span>                                                            | <span data-ttu-id="5c537-107">Description</span><span class="sxs-lookup"><span data-stu-id="5c537-107">Description</span></span>                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="5c537-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="5c537-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="5c537-109">\[dans \] le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="5c537-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="5c537-110">*dest* = sqrt (*src0*)</span><span class="sxs-lookup"><span data-stu-id="5c537-110">*dest* = sqrt(*src0*)</span></span><br/> |
| <span data-ttu-id="5c537-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="5c537-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="5c537-112">\[dans \] les composants pour lesquels prendre la racine carrée.</span><span class="sxs-lookup"><span data-stu-id="5c537-112">\[in\] The components for which to take the square root.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="5c537-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="5c537-113">Remarks</span></span>

<span data-ttu-id="5c537-114">La précision est 1 ULP.</span><span class="sxs-lookup"><span data-stu-id="5c537-114">Precision is 1 ulp.</span></span>

<span data-ttu-id="5c537-115">Le tableau suivant présente les résultats obtenus lors de l’exécution de l’instruction avec différentes classes de nombres, en supposant qu’aucun dépassement de capacité ou négatif ne se produit.</span><span class="sxs-lookup"><span data-stu-id="5c537-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="5c537-116">F signifie nombre fini-réel.</span><span class="sxs-lookup"><span data-stu-id="5c537-116">F means finite-real number.</span></span>



|          | <span data-ttu-id="5c537-117">**-INF**</span><span class="sxs-lookup"><span data-stu-id="5c537-117">**-inf**</span></span> | <span data-ttu-id="5c537-118">**-F**</span><span class="sxs-lookup"><span data-stu-id="5c537-118">**-F**</span></span> | <span data-ttu-id="5c537-119">**-dénorme**</span><span class="sxs-lookup"><span data-stu-id="5c537-119">**-denorm**</span></span> | <span data-ttu-id="5c537-120">**-0**</span><span class="sxs-lookup"><span data-stu-id="5c537-120">**-0**</span></span> | <span data-ttu-id="5c537-121">**+0**</span><span class="sxs-lookup"><span data-stu-id="5c537-121">**+0**</span></span> | <span data-ttu-id="5c537-122">**+ dénorme**</span><span class="sxs-lookup"><span data-stu-id="5c537-122">**+denorm**</span></span> | <span data-ttu-id="5c537-123">**+ F**</span><span class="sxs-lookup"><span data-stu-id="5c537-123">**+F**</span></span> | <span data-ttu-id="5c537-124">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="5c537-124">**+inf**</span></span> | <span data-ttu-id="5c537-125">**NaN**</span><span class="sxs-lookup"><span data-stu-id="5c537-125">**NaN**</span></span> |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="5c537-126">**dest**</span><span class="sxs-lookup"><span data-stu-id="5c537-126">**dest**</span></span> | <span data-ttu-id="5c537-127">NaN</span><span class="sxs-lookup"><span data-stu-id="5c537-127">NaN</span></span>      | <span data-ttu-id="5c537-128">NaN</span><span class="sxs-lookup"><span data-stu-id="5c537-128">NaN</span></span>    | <span data-ttu-id="5c537-129">-0</span><span class="sxs-lookup"><span data-stu-id="5c537-129">-0</span></span>          | <span data-ttu-id="5c537-130">-0</span><span class="sxs-lookup"><span data-stu-id="5c537-130">-0</span></span>     | <span data-ttu-id="5c537-131">+0</span><span class="sxs-lookup"><span data-stu-id="5c537-131">+0</span></span>     | <span data-ttu-id="5c537-132">+0</span><span class="sxs-lookup"><span data-stu-id="5c537-132">+0</span></span>          | <span data-ttu-id="5c537-133">+ F</span><span class="sxs-lookup"><span data-stu-id="5c537-133">+F</span></span>     | <span data-ttu-id="5c537-134">+inf</span><span class="sxs-lookup"><span data-stu-id="5c537-134">+inf</span></span>     | <span data-ttu-id="5c537-135">NaN</span><span class="sxs-lookup"><span data-stu-id="5c537-135">NaN</span></span>     |



 

<span data-ttu-id="5c537-136">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="5c537-136">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="5c537-137">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="5c537-137">Vertex Shader</span></span> | <span data-ttu-id="5c537-138">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="5c537-138">Geometry Shader</span></span> | <span data-ttu-id="5c537-139">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="5c537-139">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="5c537-140">x</span><span class="sxs-lookup"><span data-stu-id="5c537-140">x</span></span>             | <span data-ttu-id="5c537-141">x</span><span class="sxs-lookup"><span data-stu-id="5c537-141">x</span></span>               | <span data-ttu-id="5c537-142">x</span><span class="sxs-lookup"><span data-stu-id="5c537-142">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5c537-143">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="5c537-143">Minimum Shader Model</span></span>

<span data-ttu-id="5c537-144">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="5c537-144">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5c537-145">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="5c537-145">Shader Model</span></span>                                              | <span data-ttu-id="5c537-146">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c537-146">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5c537-147">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="5c537-147">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="5c537-148">oui</span><span class="sxs-lookup"><span data-stu-id="5c537-148">yes</span></span>       |
| [<span data-ttu-id="5c537-149">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="5c537-149">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="5c537-150">oui</span><span class="sxs-lookup"><span data-stu-id="5c537-150">yes</span></span>       |
| [<span data-ttu-id="5c537-151">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="5c537-151">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5c537-152">oui</span><span class="sxs-lookup"><span data-stu-id="5c537-152">yes</span></span>       |
| [<span data-ttu-id="5c537-153">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5c537-153">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5c537-154">non</span><span class="sxs-lookup"><span data-stu-id="5c537-154">no</span></span>        |
| [<span data-ttu-id="5c537-155">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5c537-155">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5c537-156">non</span><span class="sxs-lookup"><span data-stu-id="5c537-156">no</span></span>        |
| [<span data-ttu-id="5c537-157">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5c537-157">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5c537-158">non</span><span class="sxs-lookup"><span data-stu-id="5c537-158">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5c537-159">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5c537-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c537-160">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5c537-160">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





