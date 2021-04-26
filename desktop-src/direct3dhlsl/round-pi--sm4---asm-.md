---
title: round_pi (SM4-ASM)
description: Arrondi à virgule flottante à l’entier float. | round_pi (SM4-ASM)
ms.assetid: AA4E4C2E-A4B0-4892-8660-1EF57767F4C4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b61282078b3639681eed756e2899d06744f0369e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997106"
---
# <a name="round_pi-sm4---asm"></a><span data-ttu-id="c91cd-104">Round \_ pi (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="c91cd-104">round\_pi (sm4 - asm)</span></span>

<span data-ttu-id="c91cd-105">Arrondi à virgule flottante à l’entier float.</span><span class="sxs-lookup"><span data-stu-id="c91cd-105">Floating-point round to integral float.</span></span>



| <span data-ttu-id="c91cd-106">Round \_ pi \[ \_ SAT \] dest \[ . masque \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="c91cd-106">round\_pi\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------------|



 



| <span data-ttu-id="c91cd-107">Élément</span><span class="sxs-lookup"><span data-stu-id="c91cd-107">Item</span></span>                                                            | <span data-ttu-id="c91cd-108">Description</span><span class="sxs-lookup"><span data-stu-id="c91cd-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="c91cd-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="c91cd-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="c91cd-110">\[dans \] l’adresse des résultats de l’opération.</span><span class="sxs-lookup"><span data-stu-id="c91cd-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="c91cd-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="c91cd-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="c91cd-112">\[dans \] les composants de l’opération.</span><span class="sxs-lookup"><span data-stu-id="c91cd-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="c91cd-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="c91cd-113">Remarks</span></span>

<span data-ttu-id="c91cd-114">Cette instruction effectue un arrondi de valeurs à virgule flottante au niveau du composant dans *src0*, en écrivant des valeurs à virgule flottante intégrales dans *dest*.</span><span class="sxs-lookup"><span data-stu-id="c91cd-114">This instruction performs a component-wise floating-point round of the values in *src0*, writing integral floating-point values to *dest*.</span></span>

<span data-ttu-id="c91cd-115">**round \_ pi** arrondit à + Infinity, communément appelé ceil ().</span><span class="sxs-lookup"><span data-stu-id="c91cd-115">**round\_pi** rounds towards +infinity, commonly known as ceil().</span></span>

<span data-ttu-id="c91cd-116">Le tableau suivant présente les résultats obtenus lors de l’exécution de l’instruction avec différentes classes de nombres.</span><span class="sxs-lookup"><span data-stu-id="c91cd-116">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>

<span data-ttu-id="c91cd-117">F signifie nombre fini-réel.</span><span class="sxs-lookup"><span data-stu-id="c91cd-117">F means finite-real number.</span></span>



| <span data-ttu-id="c91cd-118">**src**</span><span class="sxs-lookup"><span data-stu-id="c91cd-118">**src**</span></span>  | <span data-ttu-id="c91cd-119">**-INF**</span><span class="sxs-lookup"><span data-stu-id="c91cd-119">**-inf**</span></span> | <span data-ttu-id="c91cd-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="c91cd-120">**-F**</span></span> | <span data-ttu-id="c91cd-121">**-dénorme**</span><span class="sxs-lookup"><span data-stu-id="c91cd-121">**-denorm**</span></span> | <span data-ttu-id="c91cd-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="c91cd-122">**-0**</span></span> | <span data-ttu-id="c91cd-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="c91cd-123">**+0**</span></span> | <span data-ttu-id="c91cd-124">**+ dénorme**</span><span class="sxs-lookup"><span data-stu-id="c91cd-124">**+denorm**</span></span> | <span data-ttu-id="c91cd-125">**+ F**</span><span class="sxs-lookup"><span data-stu-id="c91cd-125">**+F**</span></span> | <span data-ttu-id="c91cd-126">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="c91cd-126">**+inf**</span></span> | <span data-ttu-id="c91cd-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="c91cd-127">**NaN**</span></span> |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="c91cd-128">**dest**</span><span class="sxs-lookup"><span data-stu-id="c91cd-128">**dest**</span></span> | <span data-ttu-id="c91cd-129">-inf</span><span class="sxs-lookup"><span data-stu-id="c91cd-129">-inf</span></span>     | <span data-ttu-id="c91cd-130">-F</span><span class="sxs-lookup"><span data-stu-id="c91cd-130">-F</span></span>     | <span data-ttu-id="c91cd-131">-0</span><span class="sxs-lookup"><span data-stu-id="c91cd-131">-0</span></span>          | <span data-ttu-id="c91cd-132">-0</span><span class="sxs-lookup"><span data-stu-id="c91cd-132">-0</span></span>     | <span data-ttu-id="c91cd-133">+0</span><span class="sxs-lookup"><span data-stu-id="c91cd-133">+0</span></span>     | <span data-ttu-id="c91cd-134">+0</span><span class="sxs-lookup"><span data-stu-id="c91cd-134">+0</span></span>          | <span data-ttu-id="c91cd-135">+ F</span><span class="sxs-lookup"><span data-stu-id="c91cd-135">+F</span></span>     | <span data-ttu-id="c91cd-136">+inf</span><span class="sxs-lookup"><span data-stu-id="c91cd-136">+inf</span></span>     | <span data-ttu-id="c91cd-137">NaN</span><span class="sxs-lookup"><span data-stu-id="c91cd-137">NaN</span></span>     |



 

<span data-ttu-id="c91cd-138">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="c91cd-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c91cd-139">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="c91cd-139">Vertex Shader</span></span> | <span data-ttu-id="c91cd-140">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="c91cd-140">Geometry Shader</span></span> | <span data-ttu-id="c91cd-141">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="c91cd-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="c91cd-142">x</span><span class="sxs-lookup"><span data-stu-id="c91cd-142">x</span></span>             | <span data-ttu-id="c91cd-143">x</span><span class="sxs-lookup"><span data-stu-id="c91cd-143">x</span></span>               | <span data-ttu-id="c91cd-144">x</span><span class="sxs-lookup"><span data-stu-id="c91cd-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c91cd-145">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="c91cd-145">Minimum Shader Model</span></span>

<span data-ttu-id="c91cd-146">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="c91cd-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c91cd-147">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="c91cd-147">Shader Model</span></span>                                              | <span data-ttu-id="c91cd-148">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="c91cd-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c91cd-149">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="c91cd-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c91cd-150">oui</span><span class="sxs-lookup"><span data-stu-id="c91cd-150">yes</span></span>       |
| [<span data-ttu-id="c91cd-151">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="c91cd-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c91cd-152">oui</span><span class="sxs-lookup"><span data-stu-id="c91cd-152">yes</span></span>       |
| [<span data-ttu-id="c91cd-153">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="c91cd-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c91cd-154">oui</span><span class="sxs-lookup"><span data-stu-id="c91cd-154">yes</span></span>       |
| [<span data-ttu-id="c91cd-155">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c91cd-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c91cd-156">non</span><span class="sxs-lookup"><span data-stu-id="c91cd-156">no</span></span>        |
| [<span data-ttu-id="c91cd-157">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c91cd-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c91cd-158">non</span><span class="sxs-lookup"><span data-stu-id="c91cd-158">no</span></span>        |
| [<span data-ttu-id="c91cd-159">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c91cd-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c91cd-160">non</span><span class="sxs-lookup"><span data-stu-id="c91cd-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c91cd-161">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c91cd-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c91cd-162">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c91cd-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





