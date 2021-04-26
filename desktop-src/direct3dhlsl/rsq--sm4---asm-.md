---
title: rsq (SM4-ASM)
description: Racine carrée réciproque au niveau du composant.
ms.assetid: CDA3C2DF-2793-4CE3-87CE-4E0AA945A1BB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1528e9f187ff7d4fb6074d42a1c574686f3b22f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998166"
---
# <a name="rsq-sm4---asm"></a><span data-ttu-id="1dc34-103">rsq (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="1dc34-103">rsq (sm4 - asm)</span></span>

<span data-ttu-id="1dc34-104">Racine carrée réciproque au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="1dc34-104">Component-wise reciprocal square root.</span></span>



| <span data-ttu-id="1dc34-105">rsq \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="1dc34-105">rsq\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="1dc34-106">Élément</span><span class="sxs-lookup"><span data-stu-id="1dc34-106">Item</span></span>                                                            | <span data-ttu-id="1dc34-107">Description</span><span class="sxs-lookup"><span data-stu-id="1dc34-107">Description</span></span>                                                                                      |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1dc34-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="1dc34-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="1dc34-109">\[dans \] contient les résultats de l’opération.</span><span class="sxs-lookup"><span data-stu-id="1dc34-109">\[in\] Contains the results of the operation.</span></span><br/> <span data-ttu-id="1dc34-110">*dest* = 1.0 f/sqrt (*src0*)</span><span class="sxs-lookup"><span data-stu-id="1dc34-110">*dest* = 1.0f / sqrt(*src0*)</span></span><br/> |
| <span data-ttu-id="1dc34-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="1dc34-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="1dc34-112">\[dans \] les composants de l’opération.</span><span class="sxs-lookup"><span data-stu-id="1dc34-112">\[in\] The components for the operation.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="1dc34-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="1dc34-113">Remarks</span></span>

<span data-ttu-id="1dc34-114">L’erreur relative maximale est 2-21.</span><span class="sxs-lookup"><span data-stu-id="1dc34-114">The maximum relative error is 2-21.</span></span>

<span data-ttu-id="1dc34-115">Le tableau suivant présente les résultats obtenus lors de l’exécution de l’instruction avec différentes classes de nombres, en supposant qu’aucun dépassement de capacité ou négatif ne se produit.</span><span class="sxs-lookup"><span data-stu-id="1dc34-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="1dc34-116">F signifie nombre fini-réel.</span><span class="sxs-lookup"><span data-stu-id="1dc34-116">F means finite-real number.</span></span>



| <span data-ttu-id="1dc34-117">**src**</span><span class="sxs-lookup"><span data-stu-id="1dc34-117">**src**</span></span>  | <span data-ttu-id="1dc34-118">**-INF**</span><span class="sxs-lookup"><span data-stu-id="1dc34-118">**-inf**</span></span> | <span data-ttu-id="1dc34-119">**-F**</span><span class="sxs-lookup"><span data-stu-id="1dc34-119">**-F**</span></span> | <span data-ttu-id="1dc34-120">**-dénorme**</span><span class="sxs-lookup"><span data-stu-id="1dc34-120">**-denorm**</span></span> | <span data-ttu-id="1dc34-121">**-0**</span><span class="sxs-lookup"><span data-stu-id="1dc34-121">**-0**</span></span> | <span data-ttu-id="1dc34-122">**+0**</span><span class="sxs-lookup"><span data-stu-id="1dc34-122">**+0**</span></span> | <span data-ttu-id="1dc34-123">**+ dénorme**</span><span class="sxs-lookup"><span data-stu-id="1dc34-123">**+denorm**</span></span> | <span data-ttu-id="1dc34-124">**+ F**</span><span class="sxs-lookup"><span data-stu-id="1dc34-124">**+F**</span></span> | <span data-ttu-id="1dc34-125">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="1dc34-125">**+inf**</span></span> | <span data-ttu-id="1dc34-126">**NaN**</span><span class="sxs-lookup"><span data-stu-id="1dc34-126">**NaN**</span></span> |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="1dc34-127">**dest**</span><span class="sxs-lookup"><span data-stu-id="1dc34-127">**dest**</span></span> | <span data-ttu-id="1dc34-128">NaN</span><span class="sxs-lookup"><span data-stu-id="1dc34-128">NaN</span></span>      | <span data-ttu-id="1dc34-129">NaN</span><span class="sxs-lookup"><span data-stu-id="1dc34-129">NaN</span></span>    | <span data-ttu-id="1dc34-130">-inf</span><span class="sxs-lookup"><span data-stu-id="1dc34-130">-inf</span></span>        | <span data-ttu-id="1dc34-131">-inf</span><span class="sxs-lookup"><span data-stu-id="1dc34-131">-inf</span></span>   | <span data-ttu-id="1dc34-132">+inf</span><span class="sxs-lookup"><span data-stu-id="1dc34-132">+inf</span></span>   | <span data-ttu-id="1dc34-133">+inf</span><span class="sxs-lookup"><span data-stu-id="1dc34-133">+inf</span></span>        | <span data-ttu-id="1dc34-134">+ F</span><span class="sxs-lookup"><span data-stu-id="1dc34-134">+F</span></span>     | <span data-ttu-id="1dc34-135">+0</span><span class="sxs-lookup"><span data-stu-id="1dc34-135">+0</span></span>       | <span data-ttu-id="1dc34-136">NaN</span><span class="sxs-lookup"><span data-stu-id="1dc34-136">NaN</span></span>     |



 

<span data-ttu-id="1dc34-137">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="1dc34-137">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1dc34-138">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="1dc34-138">Vertex Shader</span></span> | <span data-ttu-id="1dc34-139">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="1dc34-139">Geometry Shader</span></span> | <span data-ttu-id="1dc34-140">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="1dc34-140">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="1dc34-141">x</span><span class="sxs-lookup"><span data-stu-id="1dc34-141">x</span></span>             | <span data-ttu-id="1dc34-142">x</span><span class="sxs-lookup"><span data-stu-id="1dc34-142">x</span></span>               | <span data-ttu-id="1dc34-143">x</span><span class="sxs-lookup"><span data-stu-id="1dc34-143">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1dc34-144">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="1dc34-144">Minimum Shader Model</span></span>

<span data-ttu-id="1dc34-145">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="1dc34-145">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1dc34-146">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="1dc34-146">Shader Model</span></span>                                              | <span data-ttu-id="1dc34-147">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="1dc34-147">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1dc34-148">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="1dc34-148">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1dc34-149">oui</span><span class="sxs-lookup"><span data-stu-id="1dc34-149">yes</span></span>       |
| [<span data-ttu-id="1dc34-150">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="1dc34-150">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1dc34-151">oui</span><span class="sxs-lookup"><span data-stu-id="1dc34-151">yes</span></span>       |
| [<span data-ttu-id="1dc34-152">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="1dc34-152">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1dc34-153">oui</span><span class="sxs-lookup"><span data-stu-id="1dc34-153">yes</span></span>       |
| [<span data-ttu-id="1dc34-154">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1dc34-154">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1dc34-155">non</span><span class="sxs-lookup"><span data-stu-id="1dc34-155">no</span></span>        |
| [<span data-ttu-id="1dc34-156">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1dc34-156">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1dc34-157">non</span><span class="sxs-lookup"><span data-stu-id="1dc34-157">no</span></span>        |
| [<span data-ttu-id="1dc34-158">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1dc34-158">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1dc34-159">non</span><span class="sxs-lookup"><span data-stu-id="1dc34-159">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1dc34-160">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1dc34-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1dc34-161">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1dc34-161">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





