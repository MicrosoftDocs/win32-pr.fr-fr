---
title: round_ne (SM4-ASM)
description: Arrondi à virgule flottante à l’entier float. | round_ne (SM4-ASM)
ms.assetid: 2D1A0786-F7DB-4D69-9F56-82ECD1EE7ABA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1c6f5e332453318dc0ad1a7806c3506343ff3b6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974198"
---
# <a name="round_ne-sm4---asm"></a><span data-ttu-id="d58f1-104">arrondir ne \_ (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="d58f1-104">round\_ne (sm4 - asm)</span></span>

<span data-ttu-id="d58f1-105">Arrondi à virgule flottante à l’entier float.</span><span class="sxs-lookup"><span data-stu-id="d58f1-105">Floating-point round to integral float.</span></span>



| <span data-ttu-id="d58f1-106">Round \_ ne \[ \_ rat \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="d58f1-106">round\_ne\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------------|



 



| <span data-ttu-id="d58f1-107">Élément</span><span class="sxs-lookup"><span data-stu-id="d58f1-107">Item</span></span>                                                            | <span data-ttu-id="d58f1-108">Description</span><span class="sxs-lookup"><span data-stu-id="d58f1-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="d58f1-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="d58f1-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="d58f1-110">\[dans \] l’adresse des résultats de l’opération.</span><span class="sxs-lookup"><span data-stu-id="d58f1-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="d58f1-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="d58f1-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="d58f1-112">\[dans \] les composants de l’opération.</span><span class="sxs-lookup"><span data-stu-id="d58f1-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="d58f1-113">Notes</span><span class="sxs-lookup"><span data-stu-id="d58f1-113">Remarks</span></span>

<span data-ttu-id="d58f1-114">Cette instruction effectue un arrondi de valeurs à virgule flottante au niveau du composant dans *src0*, en écrivant des valeurs à virgule flottante intégrales dans *dest*.</span><span class="sxs-lookup"><span data-stu-id="d58f1-114">This instruction performs a component-wise floating-point round of the values in *src0*, writing integral floating-point values to *dest*.</span></span> <span data-ttu-id="d58f1-115">**arrondit \_** le chiffre le plus proche pair.</span><span class="sxs-lookup"><span data-stu-id="d58f1-115">**round\_ne** rounds towards nearest even.</span></span>

<span data-ttu-id="d58f1-116">Le tableau suivant présente les résultats obtenus lors de l’exécution de l’instruction avec différentes classes de nombres.</span><span class="sxs-lookup"><span data-stu-id="d58f1-116">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>

<span data-ttu-id="d58f1-117">F signifie nombre fini-réel.</span><span class="sxs-lookup"><span data-stu-id="d58f1-117">F means finite-real number.</span></span>



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="d58f1-118">**src**</span><span class="sxs-lookup"><span data-stu-id="d58f1-118">**src**</span></span>  | <span data-ttu-id="d58f1-119">**-INF**</span><span class="sxs-lookup"><span data-stu-id="d58f1-119">**-inf**</span></span> | <span data-ttu-id="d58f1-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="d58f1-120">**-F**</span></span> | <span data-ttu-id="d58f1-121">**-dénorme**</span><span class="sxs-lookup"><span data-stu-id="d58f1-121">**-denorm**</span></span> | <span data-ttu-id="d58f1-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="d58f1-122">**-0**</span></span> | <span data-ttu-id="d58f1-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="d58f1-123">**+0**</span></span> | <span data-ttu-id="d58f1-124">**+ dénorme**</span><span class="sxs-lookup"><span data-stu-id="d58f1-124">**+denorm**</span></span> | <span data-ttu-id="d58f1-125">**+ F**</span><span class="sxs-lookup"><span data-stu-id="d58f1-125">**+F**</span></span> | <span data-ttu-id="d58f1-126">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="d58f1-126">**+inf**</span></span> | <span data-ttu-id="d58f1-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="d58f1-127">**NaN**</span></span> |
| <span data-ttu-id="d58f1-128">**dest**</span><span class="sxs-lookup"><span data-stu-id="d58f1-128">**dest**</span></span> | <span data-ttu-id="d58f1-129">-inf</span><span class="sxs-lookup"><span data-stu-id="d58f1-129">-inf</span></span>     | <span data-ttu-id="d58f1-130">-F</span><span class="sxs-lookup"><span data-stu-id="d58f1-130">-F</span></span>     | <span data-ttu-id="d58f1-131">-0</span><span class="sxs-lookup"><span data-stu-id="d58f1-131">-0</span></span>          | <span data-ttu-id="d58f1-132">-0</span><span class="sxs-lookup"><span data-stu-id="d58f1-132">-0</span></span>     | <span data-ttu-id="d58f1-133">+0</span><span class="sxs-lookup"><span data-stu-id="d58f1-133">+0</span></span>     | <span data-ttu-id="d58f1-134">+0</span><span class="sxs-lookup"><span data-stu-id="d58f1-134">+0</span></span>          | <span data-ttu-id="d58f1-135">+ F</span><span class="sxs-lookup"><span data-stu-id="d58f1-135">+F</span></span>     | <span data-ttu-id="d58f1-136">+inf</span><span class="sxs-lookup"><span data-stu-id="d58f1-136">+inf</span></span>     | <span data-ttu-id="d58f1-137">NaN</span><span class="sxs-lookup"><span data-stu-id="d58f1-137">NaN</span></span>     |



 

<span data-ttu-id="d58f1-138">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="d58f1-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d58f1-139">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="d58f1-139">Vertex Shader</span></span> | <span data-ttu-id="d58f1-140">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="d58f1-140">Geometry Shader</span></span> | <span data-ttu-id="d58f1-141">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="d58f1-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="d58f1-142">x</span><span class="sxs-lookup"><span data-stu-id="d58f1-142">x</span></span>             | <span data-ttu-id="d58f1-143">x</span><span class="sxs-lookup"><span data-stu-id="d58f1-143">x</span></span>               | <span data-ttu-id="d58f1-144">x</span><span class="sxs-lookup"><span data-stu-id="d58f1-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d58f1-145">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="d58f1-145">Minimum Shader Model</span></span>

<span data-ttu-id="d58f1-146">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="d58f1-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d58f1-147">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="d58f1-147">Shader Model</span></span>                                              | <span data-ttu-id="d58f1-148">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="d58f1-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d58f1-149">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="d58f1-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d58f1-150">Oui</span><span class="sxs-lookup"><span data-stu-id="d58f1-150">yes</span></span>       |
| [<span data-ttu-id="d58f1-151">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="d58f1-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d58f1-152">Oui</span><span class="sxs-lookup"><span data-stu-id="d58f1-152">yes</span></span>       |
| [<span data-ttu-id="d58f1-153">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="d58f1-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d58f1-154">Oui</span><span class="sxs-lookup"><span data-stu-id="d58f1-154">yes</span></span>       |
| [<span data-ttu-id="d58f1-155">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d58f1-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d58f1-156">non</span><span class="sxs-lookup"><span data-stu-id="d58f1-156">no</span></span>        |
| [<span data-ttu-id="d58f1-157">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d58f1-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d58f1-158">non</span><span class="sxs-lookup"><span data-stu-id="d58f1-158">no</span></span>        |
| [<span data-ttu-id="d58f1-159">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d58f1-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d58f1-160">non</span><span class="sxs-lookup"><span data-stu-id="d58f1-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d58f1-161">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d58f1-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d58f1-162">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d58f1-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





