---
title: FRC (SM4-ASM)
description: Composant, extraire un composant fractionnaire.
ms.assetid: 17C88BCE-7F2F-446C-9BB4-860098B5E42A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f59b747f38fb970b92b5e48610873efe781d63d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993916"
---
# <a name="frc-sm4---asm"></a><span data-ttu-id="4e0c3-103">FRC (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="4e0c3-103">frc (sm4 - asm)</span></span>

<span data-ttu-id="4e0c3-104">Composant, extraire un composant fractionnaire.</span><span class="sxs-lookup"><span data-stu-id="4e0c3-104">Component-wise, extract fractional component.</span></span>



| <span data-ttu-id="4e0c3-105">FRC \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="4e0c3-105">frc\[\_sat\] dest\[.mask\], \[-\] src0\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="4e0c3-106">Élément</span><span class="sxs-lookup"><span data-stu-id="4e0c3-106">Item</span></span>                                                            | <span data-ttu-id="4e0c3-107">Description</span><span class="sxs-lookup"><span data-stu-id="4e0c3-107">Description</span></span>                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e0c3-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="4e0c3-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="4e0c3-109">\[dans \] l’adresse du résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="4e0c3-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="4e0c3-110">*dest*  =  . *src0*  -  [arrondi \_](round-ni--sm4---asm-.md)(*src0*)</span><span class="sxs-lookup"><span data-stu-id="4e0c3-110">*dest* = *src0* - [round\_ni](round-ni--sm4---asm-.md)(*src0*)</span></span><br/> |
| <span data-ttu-id="4e0c3-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="4e0c3-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="4e0c3-112">\[dans \] le composant de l’opération.</span><span class="sxs-lookup"><span data-stu-id="4e0c3-112">\[in\] The component in the operation.</span></span><br/>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="4e0c3-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="4e0c3-113">Remarks</span></span>

<span data-ttu-id="4e0c3-114">Le tableau suivant présente les résultats obtenus lors de l’exécution de l’instruction avec différentes classes de nombres.</span><span class="sxs-lookup"><span data-stu-id="4e0c3-114">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>



| <span data-ttu-id="4e0c3-115">**src**</span><span class="sxs-lookup"><span data-stu-id="4e0c3-115">**src**</span></span>  | <span data-ttu-id="4e0c3-116">**-INF**</span><span class="sxs-lookup"><span data-stu-id="4e0c3-116">**-inf**</span></span> | <span data-ttu-id="4e0c3-117">**-F**</span><span class="sxs-lookup"><span data-stu-id="4e0c3-117">**-F**</span></span>     | <span data-ttu-id="4e0c3-118">**-dénorme**</span><span class="sxs-lookup"><span data-stu-id="4e0c3-118">**-denorm**</span></span> | <span data-ttu-id="4e0c3-119">**-0**</span><span class="sxs-lookup"><span data-stu-id="4e0c3-119">**-0**</span></span> | <span data-ttu-id="4e0c3-120">**+0**</span><span class="sxs-lookup"><span data-stu-id="4e0c3-120">**+0**</span></span> | <span data-ttu-id="4e0c3-121">**+ dénorme**</span><span class="sxs-lookup"><span data-stu-id="4e0c3-121">**+denorm**</span></span> | <span data-ttu-id="4e0c3-122">**+ F**</span><span class="sxs-lookup"><span data-stu-id="4e0c3-122">**+F**</span></span>     | <span data-ttu-id="4e0c3-123">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="4e0c3-123">**+inf**</span></span> | <span data-ttu-id="4e0c3-124">**NaN**</span><span class="sxs-lookup"><span data-stu-id="4e0c3-124">**NaN**</span></span> |
|----------|----------|------------|-------------|--------|--------|-------------|------------|----------|---------|
| <span data-ttu-id="4e0c3-125">**dest**</span><span class="sxs-lookup"><span data-stu-id="4e0c3-125">**dest**</span></span> | <span data-ttu-id="4e0c3-126">NaN</span><span class="sxs-lookup"><span data-stu-id="4e0c3-126">NaN</span></span>      | <span data-ttu-id="4e0c3-127">\[+ 0 à 1)</span><span class="sxs-lookup"><span data-stu-id="4e0c3-127">\[+0 to 1)</span></span> | <span data-ttu-id="4e0c3-128">+0</span><span class="sxs-lookup"><span data-stu-id="4e0c3-128">+0</span></span>          | <span data-ttu-id="4e0c3-129">+0</span><span class="sxs-lookup"><span data-stu-id="4e0c3-129">+0</span></span>     | <span data-ttu-id="4e0c3-130">+0</span><span class="sxs-lookup"><span data-stu-id="4e0c3-130">+0</span></span>     | <span data-ttu-id="4e0c3-131">+0</span><span class="sxs-lookup"><span data-stu-id="4e0c3-131">+0</span></span>          | <span data-ttu-id="4e0c3-132">\[+ 0 à 1)</span><span class="sxs-lookup"><span data-stu-id="4e0c3-132">\[+0 to 1)</span></span> | <span data-ttu-id="4e0c3-133">NaN</span><span class="sxs-lookup"><span data-stu-id="4e0c3-133">NaN</span></span>      | <span data-ttu-id="4e0c3-134">NaN</span><span class="sxs-lookup"><span data-stu-id="4e0c3-134">NaN</span></span>     |



 

<span data-ttu-id="4e0c3-135">F signifie nombre fini-réel.</span><span class="sxs-lookup"><span data-stu-id="4e0c3-135">F means finite-real number.</span></span>

<span data-ttu-id="4e0c3-136">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="4e0c3-136">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="4e0c3-137">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="4e0c3-137">Vertex Shader</span></span> | <span data-ttu-id="4e0c3-138">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="4e0c3-138">Geometry Shader</span></span> | <span data-ttu-id="4e0c3-139">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="4e0c3-139">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="4e0c3-140">x</span><span class="sxs-lookup"><span data-stu-id="4e0c3-140">x</span></span>             | <span data-ttu-id="4e0c3-141">x</span><span class="sxs-lookup"><span data-stu-id="4e0c3-141">x</span></span>               | <span data-ttu-id="4e0c3-142">x</span><span class="sxs-lookup"><span data-stu-id="4e0c3-142">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4e0c3-143">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="4e0c3-143">Minimum Shader Model</span></span>

<span data-ttu-id="4e0c3-144">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="4e0c3-144">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4e0c3-145">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="4e0c3-145">Shader Model</span></span>                                              | <span data-ttu-id="4e0c3-146">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e0c3-146">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4e0c3-147">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="4e0c3-147">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4e0c3-148">oui</span><span class="sxs-lookup"><span data-stu-id="4e0c3-148">yes</span></span>       |
| [<span data-ttu-id="4e0c3-149">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="4e0c3-149">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4e0c3-150">oui</span><span class="sxs-lookup"><span data-stu-id="4e0c3-150">yes</span></span>       |
| [<span data-ttu-id="4e0c3-151">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="4e0c3-151">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4e0c3-152">oui</span><span class="sxs-lookup"><span data-stu-id="4e0c3-152">yes</span></span>       |
| [<span data-ttu-id="4e0c3-153">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4e0c3-153">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4e0c3-154">non</span><span class="sxs-lookup"><span data-stu-id="4e0c3-154">no</span></span>        |
| [<span data-ttu-id="4e0c3-155">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4e0c3-155">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4e0c3-156">non</span><span class="sxs-lookup"><span data-stu-id="4e0c3-156">no</span></span>        |
| [<span data-ttu-id="4e0c3-157">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4e0c3-157">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4e0c3-158">non</span><span class="sxs-lookup"><span data-stu-id="4e0c3-158">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4e0c3-159">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4e0c3-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e0c3-160">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4e0c3-160">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





