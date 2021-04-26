---
title: round_ni (SM4-ASM)
description: Arrondi à virgule flottante à l’entier float. | round_ni (SM4-ASM)
ms.assetid: 6DEF818B-AFF9-4B44-950E-320EACE1CAC4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2487715bbb2596653b1ca985a2e0390457feecbf
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998576"
---
# <a name="round_ni-sm4---asm"></a><span data-ttu-id="4d8a8-104">Round \_ (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="4d8a8-104">round\_ni (sm4 - asm)</span></span>

<span data-ttu-id="4d8a8-105">Arrondi à virgule flottante à l’entier float.</span><span class="sxs-lookup"><span data-stu-id="4d8a8-105">Floating-point round to integral float.</span></span>



| <span data-ttu-id="4d8a8-106">Round \_ / \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="4d8a8-106">round\_ni\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------------|



 



| <span data-ttu-id="4d8a8-107">Élément</span><span class="sxs-lookup"><span data-stu-id="4d8a8-107">Item</span></span>                                                            | <span data-ttu-id="4d8a8-108">Description</span><span class="sxs-lookup"><span data-stu-id="4d8a8-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="4d8a8-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="4d8a8-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="4d8a8-110">\[dans \] l’adresse des résultats de l’opération.</span><span class="sxs-lookup"><span data-stu-id="4d8a8-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="4d8a8-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="4d8a8-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="4d8a8-112">\[dans \] les composants de l’opération.</span><span class="sxs-lookup"><span data-stu-id="4d8a8-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="4d8a8-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="4d8a8-113">Remarks</span></span>

<span data-ttu-id="4d8a8-114">Cette instruction effectue un arrondi de valeurs à virgule flottante au niveau du composant dans *src0*, en écrivant des valeurs à virgule flottante intégrales dans *dest*.</span><span class="sxs-lookup"><span data-stu-id="4d8a8-114">This instruction performs a component-wise floating-point round of the values in *src0*, writing integral floating-point values to *dest*.</span></span> <span data-ttu-id="4d8a8-115">**round \_** ou arrondis à-Infinity, communément appelé Floor ().</span><span class="sxs-lookup"><span data-stu-id="4d8a8-115">**round\_ni** rounds toward -infinity, commonly known as floor().</span></span>

<span data-ttu-id="4d8a8-116">Le tableau suivant présente les résultats obtenus lors de l’exécution de l’instruction avec différentes classes de nombres.</span><span class="sxs-lookup"><span data-stu-id="4d8a8-116">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>

<span data-ttu-id="4d8a8-117">F signifie nombre fini-réel.</span><span class="sxs-lookup"><span data-stu-id="4d8a8-117">F means finite-real number.</span></span>



| <span data-ttu-id="4d8a8-118">**src**</span><span class="sxs-lookup"><span data-stu-id="4d8a8-118">**src**</span></span>  | <span data-ttu-id="4d8a8-119">**-INF**</span><span class="sxs-lookup"><span data-stu-id="4d8a8-119">**-inf**</span></span> | <span data-ttu-id="4d8a8-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="4d8a8-120">**-F**</span></span> | <span data-ttu-id="4d8a8-121">**-dénorme**</span><span class="sxs-lookup"><span data-stu-id="4d8a8-121">**-denorm**</span></span> | <span data-ttu-id="4d8a8-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="4d8a8-122">**-0**</span></span> | <span data-ttu-id="4d8a8-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="4d8a8-123">**+0**</span></span> | <span data-ttu-id="4d8a8-124">**+ dénorme**</span><span class="sxs-lookup"><span data-stu-id="4d8a8-124">**+denorm**</span></span> | <span data-ttu-id="4d8a8-125">**+ F**</span><span class="sxs-lookup"><span data-stu-id="4d8a8-125">**+F**</span></span> | <span data-ttu-id="4d8a8-126">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="4d8a8-126">**+inf**</span></span> | <span data-ttu-id="4d8a8-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="4d8a8-127">**NaN**</span></span> |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="4d8a8-128">**dest**</span><span class="sxs-lookup"><span data-stu-id="4d8a8-128">**dest**</span></span> | <span data-ttu-id="4d8a8-129">-inf</span><span class="sxs-lookup"><span data-stu-id="4d8a8-129">-inf</span></span>     | <span data-ttu-id="4d8a8-130">-F</span><span class="sxs-lookup"><span data-stu-id="4d8a8-130">-F</span></span>     | <span data-ttu-id="4d8a8-131">-0</span><span class="sxs-lookup"><span data-stu-id="4d8a8-131">-0</span></span>          | <span data-ttu-id="4d8a8-132">-0</span><span class="sxs-lookup"><span data-stu-id="4d8a8-132">-0</span></span>     | <span data-ttu-id="4d8a8-133">+0</span><span class="sxs-lookup"><span data-stu-id="4d8a8-133">+0</span></span>     | <span data-ttu-id="4d8a8-134">+0</span><span class="sxs-lookup"><span data-stu-id="4d8a8-134">+0</span></span>          | <span data-ttu-id="4d8a8-135">+ F</span><span class="sxs-lookup"><span data-stu-id="4d8a8-135">+F</span></span>     | <span data-ttu-id="4d8a8-136">+inf</span><span class="sxs-lookup"><span data-stu-id="4d8a8-136">+inf</span></span>     | <span data-ttu-id="4d8a8-137">NaN</span><span class="sxs-lookup"><span data-stu-id="4d8a8-137">NaN</span></span>     |



 

<span data-ttu-id="4d8a8-138">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="4d8a8-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="4d8a8-139">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="4d8a8-139">Vertex Shader</span></span> | <span data-ttu-id="4d8a8-140">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="4d8a8-140">Geometry Shader</span></span> | <span data-ttu-id="4d8a8-141">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="4d8a8-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="4d8a8-142">x</span><span class="sxs-lookup"><span data-stu-id="4d8a8-142">x</span></span>             | <span data-ttu-id="4d8a8-143">x</span><span class="sxs-lookup"><span data-stu-id="4d8a8-143">x</span></span>               | <span data-ttu-id="4d8a8-144">x</span><span class="sxs-lookup"><span data-stu-id="4d8a8-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4d8a8-145">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="4d8a8-145">Minimum Shader Model</span></span>

<span data-ttu-id="4d8a8-146">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="4d8a8-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4d8a8-147">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="4d8a8-147">Shader Model</span></span>                                              | <span data-ttu-id="4d8a8-148">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="4d8a8-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4d8a8-149">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="4d8a8-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4d8a8-150">oui</span><span class="sxs-lookup"><span data-stu-id="4d8a8-150">yes</span></span>       |
| [<span data-ttu-id="4d8a8-151">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="4d8a8-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4d8a8-152">oui</span><span class="sxs-lookup"><span data-stu-id="4d8a8-152">yes</span></span>       |
| [<span data-ttu-id="4d8a8-153">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="4d8a8-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4d8a8-154">oui</span><span class="sxs-lookup"><span data-stu-id="4d8a8-154">yes</span></span>       |
| [<span data-ttu-id="4d8a8-155">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4d8a8-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4d8a8-156">non</span><span class="sxs-lookup"><span data-stu-id="4d8a8-156">no</span></span>        |
| [<span data-ttu-id="4d8a8-157">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4d8a8-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4d8a8-158">non</span><span class="sxs-lookup"><span data-stu-id="4d8a8-158">no</span></span>        |
| [<span data-ttu-id="4d8a8-159">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4d8a8-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4d8a8-160">non</span><span class="sxs-lookup"><span data-stu-id="4d8a8-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4d8a8-161">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4d8a8-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d8a8-162">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4d8a8-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





