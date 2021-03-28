---
title: rsq (SM4-ASM)
description: Racine carrée réciproque au niveau du composant.
ms.assetid: CDA3C2DF-2793-4CE3-87CE-4E0AA945A1BB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc274f927151938be055150d5b17287f9be0004d
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104030606"
---
# <a name="rsq-sm4---asm"></a><span data-ttu-id="3d689-103">rsq (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="3d689-103">rsq (sm4 - asm)</span></span>

<span data-ttu-id="3d689-104">Racine carrée réciproque au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="3d689-104">Component-wise reciprocal square root.</span></span>



| <span data-ttu-id="3d689-105">rsq \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="3d689-105">rsq\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="3d689-106">Élément</span><span class="sxs-lookup"><span data-stu-id="3d689-106">Item</span></span>                                                            | <span data-ttu-id="3d689-107">Description</span><span class="sxs-lookup"><span data-stu-id="3d689-107">Description</span></span>                                                                                      |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d689-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="3d689-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="3d689-109">\[dans \] contient les résultats de l’opération.</span><span class="sxs-lookup"><span data-stu-id="3d689-109">\[in\] Contains the results of the operation.</span></span><br/> <span data-ttu-id="3d689-110">*dest* = 1.0 f/sqrt (*src0*)</span><span class="sxs-lookup"><span data-stu-id="3d689-110">*dest* = 1.0f / sqrt(*src0*)</span></span><br/> |
| <span data-ttu-id="3d689-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="3d689-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="3d689-112">\[dans \] les composants de l’opération.</span><span class="sxs-lookup"><span data-stu-id="3d689-112">\[in\] The components for the operation.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="3d689-113">Notes</span><span class="sxs-lookup"><span data-stu-id="3d689-113">Remarks</span></span>

<span data-ttu-id="3d689-114">L’erreur relative maximale est 2-21.</span><span class="sxs-lookup"><span data-stu-id="3d689-114">The maximum relative error is 2-21.</span></span>

<span data-ttu-id="3d689-115">Le tableau suivant présente les résultats obtenus lors de l’exécution de l’instruction avec différentes classes de nombres, en supposant qu’aucun dépassement de capacité ou négatif ne se produit.</span><span class="sxs-lookup"><span data-stu-id="3d689-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="3d689-116">F signifie nombre fini-réel.</span><span class="sxs-lookup"><span data-stu-id="3d689-116">F means finite-real number.</span></span>



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="3d689-117">**src**</span><span class="sxs-lookup"><span data-stu-id="3d689-117">**src**</span></span>  | <span data-ttu-id="3d689-118">**-INF**</span><span class="sxs-lookup"><span data-stu-id="3d689-118">**-inf**</span></span> | <span data-ttu-id="3d689-119">**-F**</span><span class="sxs-lookup"><span data-stu-id="3d689-119">**-F**</span></span> | <span data-ttu-id="3d689-120">**-dénorme**</span><span class="sxs-lookup"><span data-stu-id="3d689-120">**-denorm**</span></span> | <span data-ttu-id="3d689-121">**-0**</span><span class="sxs-lookup"><span data-stu-id="3d689-121">**-0**</span></span> | <span data-ttu-id="3d689-122">**+0**</span><span class="sxs-lookup"><span data-stu-id="3d689-122">**+0**</span></span> | <span data-ttu-id="3d689-123">**+ dénorme**</span><span class="sxs-lookup"><span data-stu-id="3d689-123">**+denorm**</span></span> | <span data-ttu-id="3d689-124">**+ F**</span><span class="sxs-lookup"><span data-stu-id="3d689-124">**+F**</span></span> | <span data-ttu-id="3d689-125">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="3d689-125">**+inf**</span></span> | <span data-ttu-id="3d689-126">**NaN**</span><span class="sxs-lookup"><span data-stu-id="3d689-126">**NaN**</span></span> |
| <span data-ttu-id="3d689-127">**dest**</span><span class="sxs-lookup"><span data-stu-id="3d689-127">**dest**</span></span> | <span data-ttu-id="3d689-128">NaN</span><span class="sxs-lookup"><span data-stu-id="3d689-128">NaN</span></span>      | <span data-ttu-id="3d689-129">NaN</span><span class="sxs-lookup"><span data-stu-id="3d689-129">NaN</span></span>    | <span data-ttu-id="3d689-130">-inf</span><span class="sxs-lookup"><span data-stu-id="3d689-130">-inf</span></span>        | <span data-ttu-id="3d689-131">-inf</span><span class="sxs-lookup"><span data-stu-id="3d689-131">-inf</span></span>   | <span data-ttu-id="3d689-132">+inf</span><span class="sxs-lookup"><span data-stu-id="3d689-132">+inf</span></span>   | <span data-ttu-id="3d689-133">+inf</span><span class="sxs-lookup"><span data-stu-id="3d689-133">+inf</span></span>        | <span data-ttu-id="3d689-134">+ F</span><span class="sxs-lookup"><span data-stu-id="3d689-134">+F</span></span>     | <span data-ttu-id="3d689-135">+0</span><span class="sxs-lookup"><span data-stu-id="3d689-135">+0</span></span>       | <span data-ttu-id="3d689-136">NaN</span><span class="sxs-lookup"><span data-stu-id="3d689-136">NaN</span></span>     |



 

<span data-ttu-id="3d689-137">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="3d689-137">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="3d689-138">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="3d689-138">Vertex Shader</span></span> | <span data-ttu-id="3d689-139">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="3d689-139">Geometry Shader</span></span> | <span data-ttu-id="3d689-140">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="3d689-140">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="3d689-141">x</span><span class="sxs-lookup"><span data-stu-id="3d689-141">x</span></span>             | <span data-ttu-id="3d689-142">x</span><span class="sxs-lookup"><span data-stu-id="3d689-142">x</span></span>               | <span data-ttu-id="3d689-143">x</span><span class="sxs-lookup"><span data-stu-id="3d689-143">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3d689-144">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="3d689-144">Minimum Shader Model</span></span>

<span data-ttu-id="3d689-145">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="3d689-145">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3d689-146">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="3d689-146">Shader Model</span></span>                                              | <span data-ttu-id="3d689-147">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="3d689-147">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="3d689-148">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="3d689-148">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="3d689-149">Oui</span><span class="sxs-lookup"><span data-stu-id="3d689-149">yes</span></span>       |
| [<span data-ttu-id="3d689-150">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="3d689-150">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="3d689-151">Oui</span><span class="sxs-lookup"><span data-stu-id="3d689-151">yes</span></span>       |
| [<span data-ttu-id="3d689-152">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="3d689-152">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="3d689-153">Oui</span><span class="sxs-lookup"><span data-stu-id="3d689-153">yes</span></span>       |
| [<span data-ttu-id="3d689-154">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3d689-154">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="3d689-155">non</span><span class="sxs-lookup"><span data-stu-id="3d689-155">no</span></span>        |
| [<span data-ttu-id="3d689-156">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3d689-156">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="3d689-157">non</span><span class="sxs-lookup"><span data-stu-id="3d689-157">no</span></span>        |
| [<span data-ttu-id="3d689-158">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3d689-158">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="3d689-159">non</span><span class="sxs-lookup"><span data-stu-id="3d689-159">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="3d689-160">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3d689-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d689-161">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3d689-161">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





