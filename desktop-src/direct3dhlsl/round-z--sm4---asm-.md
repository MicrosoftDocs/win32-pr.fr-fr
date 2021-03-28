---
title: round_z (SM4-ASM)
description: Arrondi à virgule flottante à l’entier float. | round_z (SM4-ASM)
ms.assetid: 97C0E0F2-2571-4A94-BB04-B0CDBA0B5C0C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ed79a60bf122163b49411a3b3197ccdacba1311
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869722"
---
# <a name="round_z-sm4---asm"></a><span data-ttu-id="16f8e-104">Round \_ z (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="16f8e-104">round\_z (sm4 - asm)</span></span>

<span data-ttu-id="16f8e-105">Arrondi à virgule flottante à l’entier float.</span><span class="sxs-lookup"><span data-stu-id="16f8e-105">Floating-point round to integral float.</span></span>



| <span data-ttu-id="16f8e-106">arrondi \_ z \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="16f8e-106">round\_z\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-----------------------------------------------------------------|



 



| <span data-ttu-id="16f8e-107">Élément</span><span class="sxs-lookup"><span data-stu-id="16f8e-107">Item</span></span>                                                            | <span data-ttu-id="16f8e-108">Description</span><span class="sxs-lookup"><span data-stu-id="16f8e-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="16f8e-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="16f8e-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="16f8e-110">\[dans \] l’adresse des résultats de l’opération.</span><span class="sxs-lookup"><span data-stu-id="16f8e-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="16f8e-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="16f8e-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="16f8e-112">\[dans \] les composants de l’opération.</span><span class="sxs-lookup"><span data-stu-id="16f8e-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="16f8e-113">Notes</span><span class="sxs-lookup"><span data-stu-id="16f8e-113">Remarks</span></span>

<span data-ttu-id="16f8e-114">Cette instruction effectue un arrondi de valeurs à virgule flottante au niveau du composant dans *src0*, en écrivant des valeurs à virgule flottante intégrales dans *dest*.</span><span class="sxs-lookup"><span data-stu-id="16f8e-114">This instruction performs a component-wise floating-point round of the values in *src0*, writing integral floating-point values to *dest*.</span></span>

<span data-ttu-id="16f8e-115">**round \_ z** arrondit à zéro.</span><span class="sxs-lookup"><span data-stu-id="16f8e-115">**round\_z** rounds towards zero.</span></span>

<span data-ttu-id="16f8e-116">Le tableau suivant présente les résultats obtenus lors de l’exécution de l’instruction avec différentes classes de nombres.</span><span class="sxs-lookup"><span data-stu-id="16f8e-116">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="16f8e-117">**src**</span><span class="sxs-lookup"><span data-stu-id="16f8e-117">**src**</span></span>  | <span data-ttu-id="16f8e-118">**-INF**</span><span class="sxs-lookup"><span data-stu-id="16f8e-118">**-inf**</span></span> | <span data-ttu-id="16f8e-119">**-F**</span><span class="sxs-lookup"><span data-stu-id="16f8e-119">**-F**</span></span> | <span data-ttu-id="16f8e-120">**-dénorme**</span><span class="sxs-lookup"><span data-stu-id="16f8e-120">**-denorm**</span></span> | <span data-ttu-id="16f8e-121">**-0**</span><span class="sxs-lookup"><span data-stu-id="16f8e-121">**-0**</span></span> | <span data-ttu-id="16f8e-122">**+0**</span><span class="sxs-lookup"><span data-stu-id="16f8e-122">**+0**</span></span> | <span data-ttu-id="16f8e-123">**+ dénorme**</span><span class="sxs-lookup"><span data-stu-id="16f8e-123">**+denorm**</span></span> | <span data-ttu-id="16f8e-124">**+ F**</span><span class="sxs-lookup"><span data-stu-id="16f8e-124">**+F**</span></span> | <span data-ttu-id="16f8e-125">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="16f8e-125">**+inf**</span></span> | <span data-ttu-id="16f8e-126">**NaN**</span><span class="sxs-lookup"><span data-stu-id="16f8e-126">**NaN**</span></span> |
| <span data-ttu-id="16f8e-127">**dest**</span><span class="sxs-lookup"><span data-stu-id="16f8e-127">**dest**</span></span> | <span data-ttu-id="16f8e-128">-inf</span><span class="sxs-lookup"><span data-stu-id="16f8e-128">-inf</span></span>     | <span data-ttu-id="16f8e-129">-F</span><span class="sxs-lookup"><span data-stu-id="16f8e-129">-F</span></span>     | <span data-ttu-id="16f8e-130">-0</span><span class="sxs-lookup"><span data-stu-id="16f8e-130">-0</span></span>          | <span data-ttu-id="16f8e-131">-0</span><span class="sxs-lookup"><span data-stu-id="16f8e-131">-0</span></span>     | <span data-ttu-id="16f8e-132">+0</span><span class="sxs-lookup"><span data-stu-id="16f8e-132">+0</span></span>     | <span data-ttu-id="16f8e-133">+0</span><span class="sxs-lookup"><span data-stu-id="16f8e-133">+0</span></span>          | <span data-ttu-id="16f8e-134">+ F</span><span class="sxs-lookup"><span data-stu-id="16f8e-134">+F</span></span>     | <span data-ttu-id="16f8e-135">+inf</span><span class="sxs-lookup"><span data-stu-id="16f8e-135">+inf</span></span>     | <span data-ttu-id="16f8e-136">NaN</span><span class="sxs-lookup"><span data-stu-id="16f8e-136">NaN</span></span>     |



 

<span data-ttu-id="16f8e-137">F signifie nombre fini-réel.</span><span class="sxs-lookup"><span data-stu-id="16f8e-137">F means finite-real number.</span></span>

<span data-ttu-id="16f8e-138">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="16f8e-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="16f8e-139">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="16f8e-139">Vertex Shader</span></span> | <span data-ttu-id="16f8e-140">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="16f8e-140">Geometry Shader</span></span> | <span data-ttu-id="16f8e-141">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="16f8e-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="16f8e-142">x</span><span class="sxs-lookup"><span data-stu-id="16f8e-142">x</span></span>             | <span data-ttu-id="16f8e-143">x</span><span class="sxs-lookup"><span data-stu-id="16f8e-143">x</span></span>               | <span data-ttu-id="16f8e-144">x</span><span class="sxs-lookup"><span data-stu-id="16f8e-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="16f8e-145">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="16f8e-145">Minimum Shader Model</span></span>

<span data-ttu-id="16f8e-146">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="16f8e-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="16f8e-147">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="16f8e-147">Shader Model</span></span>                                              | <span data-ttu-id="16f8e-148">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="16f8e-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="16f8e-149">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="16f8e-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="16f8e-150">Oui</span><span class="sxs-lookup"><span data-stu-id="16f8e-150">yes</span></span>       |
| [<span data-ttu-id="16f8e-151">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="16f8e-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="16f8e-152">Oui</span><span class="sxs-lookup"><span data-stu-id="16f8e-152">yes</span></span>       |
| [<span data-ttu-id="16f8e-153">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="16f8e-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="16f8e-154">Oui</span><span class="sxs-lookup"><span data-stu-id="16f8e-154">yes</span></span>       |
| [<span data-ttu-id="16f8e-155">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="16f8e-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="16f8e-156">non</span><span class="sxs-lookup"><span data-stu-id="16f8e-156">no</span></span>        |
| [<span data-ttu-id="16f8e-157">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="16f8e-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="16f8e-158">non</span><span class="sxs-lookup"><span data-stu-id="16f8e-158">no</span></span>        |
| [<span data-ttu-id="16f8e-159">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="16f8e-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="16f8e-160">non</span><span class="sxs-lookup"><span data-stu-id="16f8e-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="16f8e-161">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="16f8e-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16f8e-162">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="16f8e-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





