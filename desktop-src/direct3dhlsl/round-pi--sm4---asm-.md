---
title: round_pi (SM4-ASM)
description: Arrondi à virgule flottante à l’entier float. | round_pi (SM4-ASM)
ms.assetid: AA4E4C2E-A4B0-4892-8660-1EF57767F4C4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6016cc03f28852c938b1be62d3aaca39dae5dcfb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992044"
---
# <a name="round_pi-sm4---asm"></a><span data-ttu-id="9ca14-104">Round \_ pi (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="9ca14-104">round\_pi (sm4 - asm)</span></span>

<span data-ttu-id="9ca14-105">Arrondi à virgule flottante à l’entier float.</span><span class="sxs-lookup"><span data-stu-id="9ca14-105">Floating-point round to integral float.</span></span>



| <span data-ttu-id="9ca14-106">Round \_ pi \[ \_ SAT \] dest \[ . masque \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="9ca14-106">round\_pi\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------------|



 



| <span data-ttu-id="9ca14-107">Élément</span><span class="sxs-lookup"><span data-stu-id="9ca14-107">Item</span></span>                                                            | <span data-ttu-id="9ca14-108">Description</span><span class="sxs-lookup"><span data-stu-id="9ca14-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="9ca14-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="9ca14-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="9ca14-110">\[dans \] l’adresse des résultats de l’opération.</span><span class="sxs-lookup"><span data-stu-id="9ca14-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="9ca14-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="9ca14-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="9ca14-112">\[dans \] les composants de l’opération.</span><span class="sxs-lookup"><span data-stu-id="9ca14-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="9ca14-113">Notes</span><span class="sxs-lookup"><span data-stu-id="9ca14-113">Remarks</span></span>

<span data-ttu-id="9ca14-114">Cette instruction effectue un arrondi de valeurs à virgule flottante au niveau du composant dans *src0*, en écrivant des valeurs à virgule flottante intégrales dans *dest*.</span><span class="sxs-lookup"><span data-stu-id="9ca14-114">This instruction performs a component-wise floating-point round of the values in *src0*, writing integral floating-point values to *dest*.</span></span>

<span data-ttu-id="9ca14-115">**round \_ pi** arrondit à + Infinity, communément appelé ceil ().</span><span class="sxs-lookup"><span data-stu-id="9ca14-115">**round\_pi** rounds towards +infinity, commonly known as ceil().</span></span>

<span data-ttu-id="9ca14-116">Le tableau suivant présente les résultats obtenus lors de l’exécution de l’instruction avec différentes classes de nombres.</span><span class="sxs-lookup"><span data-stu-id="9ca14-116">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>

<span data-ttu-id="9ca14-117">F signifie nombre fini-réel.</span><span class="sxs-lookup"><span data-stu-id="9ca14-117">F means finite-real number.</span></span>



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="9ca14-118">**src**</span><span class="sxs-lookup"><span data-stu-id="9ca14-118">**src**</span></span>  | <span data-ttu-id="9ca14-119">**-INF**</span><span class="sxs-lookup"><span data-stu-id="9ca14-119">**-inf**</span></span> | <span data-ttu-id="9ca14-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="9ca14-120">**-F**</span></span> | <span data-ttu-id="9ca14-121">**-dénorme**</span><span class="sxs-lookup"><span data-stu-id="9ca14-121">**-denorm**</span></span> | <span data-ttu-id="9ca14-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="9ca14-122">**-0**</span></span> | <span data-ttu-id="9ca14-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="9ca14-123">**+0**</span></span> | <span data-ttu-id="9ca14-124">**+ dénorme**</span><span class="sxs-lookup"><span data-stu-id="9ca14-124">**+denorm**</span></span> | <span data-ttu-id="9ca14-125">**+ F**</span><span class="sxs-lookup"><span data-stu-id="9ca14-125">**+F**</span></span> | <span data-ttu-id="9ca14-126">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="9ca14-126">**+inf**</span></span> | <span data-ttu-id="9ca14-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="9ca14-127">**NaN**</span></span> |
| <span data-ttu-id="9ca14-128">**dest**</span><span class="sxs-lookup"><span data-stu-id="9ca14-128">**dest**</span></span> | <span data-ttu-id="9ca14-129">-inf</span><span class="sxs-lookup"><span data-stu-id="9ca14-129">-inf</span></span>     | <span data-ttu-id="9ca14-130">-F</span><span class="sxs-lookup"><span data-stu-id="9ca14-130">-F</span></span>     | <span data-ttu-id="9ca14-131">-0</span><span class="sxs-lookup"><span data-stu-id="9ca14-131">-0</span></span>          | <span data-ttu-id="9ca14-132">-0</span><span class="sxs-lookup"><span data-stu-id="9ca14-132">-0</span></span>     | <span data-ttu-id="9ca14-133">+0</span><span class="sxs-lookup"><span data-stu-id="9ca14-133">+0</span></span>     | <span data-ttu-id="9ca14-134">+0</span><span class="sxs-lookup"><span data-stu-id="9ca14-134">+0</span></span>          | <span data-ttu-id="9ca14-135">+ F</span><span class="sxs-lookup"><span data-stu-id="9ca14-135">+F</span></span>     | <span data-ttu-id="9ca14-136">+inf</span><span class="sxs-lookup"><span data-stu-id="9ca14-136">+inf</span></span>     | <span data-ttu-id="9ca14-137">NaN</span><span class="sxs-lookup"><span data-stu-id="9ca14-137">NaN</span></span>     |



 

<span data-ttu-id="9ca14-138">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="9ca14-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9ca14-139">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="9ca14-139">Vertex Shader</span></span> | <span data-ttu-id="9ca14-140">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="9ca14-140">Geometry Shader</span></span> | <span data-ttu-id="9ca14-141">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="9ca14-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="9ca14-142">x</span><span class="sxs-lookup"><span data-stu-id="9ca14-142">x</span></span>             | <span data-ttu-id="9ca14-143">x</span><span class="sxs-lookup"><span data-stu-id="9ca14-143">x</span></span>               | <span data-ttu-id="9ca14-144">x</span><span class="sxs-lookup"><span data-stu-id="9ca14-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9ca14-145">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="9ca14-145">Minimum Shader Model</span></span>

<span data-ttu-id="9ca14-146">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="9ca14-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9ca14-147">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="9ca14-147">Shader Model</span></span>                                              | <span data-ttu-id="9ca14-148">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="9ca14-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9ca14-149">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="9ca14-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9ca14-150">Oui</span><span class="sxs-lookup"><span data-stu-id="9ca14-150">yes</span></span>       |
| [<span data-ttu-id="9ca14-151">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="9ca14-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9ca14-152">Oui</span><span class="sxs-lookup"><span data-stu-id="9ca14-152">yes</span></span>       |
| [<span data-ttu-id="9ca14-153">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="9ca14-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9ca14-154">Oui</span><span class="sxs-lookup"><span data-stu-id="9ca14-154">yes</span></span>       |
| [<span data-ttu-id="9ca14-155">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9ca14-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9ca14-156">non</span><span class="sxs-lookup"><span data-stu-id="9ca14-156">no</span></span>        |
| [<span data-ttu-id="9ca14-157">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9ca14-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9ca14-158">non</span><span class="sxs-lookup"><span data-stu-id="9ca14-158">no</span></span>        |
| [<span data-ttu-id="9ca14-159">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9ca14-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9ca14-160">non</span><span class="sxs-lookup"><span data-stu-id="9ca14-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9ca14-161">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9ca14-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ca14-162">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9ca14-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





