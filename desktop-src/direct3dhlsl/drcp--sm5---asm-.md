---
title: DRCP (SM5-ASM)
description: Calcule une réciproque à double précision au niveau du composant.
ms.assetid: 499A14D6-36DB-4860-94D1-887D931E60D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 770159f5007b08f5482ba8b58634b44e7f3e6ef0
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998336"
---
# <a name="drcp-sm5---asm"></a><span data-ttu-id="265c7-103">DRCP (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="265c7-103">drcp (sm5 - asm)</span></span>

<span data-ttu-id="265c7-104">Calcule une réciproque à double précision au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="265c7-104">Computes a component-wise double-precision reciprocal.</span></span>



| <span data-ttu-id="265c7-105">RCP \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="265c7-105">rcp\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="265c7-106">Élément</span><span class="sxs-lookup"><span data-stu-id="265c7-106">Item</span></span>                                                            | <span data-ttu-id="265c7-107">Description</span><span class="sxs-lookup"><span data-stu-id="265c7-107">Description</span></span>                                                                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="265c7-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="265c7-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="265c7-109">\[dans \] l’adresse des résultats</span><span class="sxs-lookup"><span data-stu-id="265c7-109">\[in\] The address of the results</span></span><br/> <span data-ttu-id="265c7-110">*dest*  =  . **1,0**  /  *src0*.</span><span class="sxs-lookup"><span data-stu-id="265c7-110">*dest* = **1.0** / *src0*.</span></span> <span data-ttu-id="265c7-111">La valeur de résultat doit être précise à 1,0 ULP</span><span class="sxs-lookup"><span data-stu-id="265c7-111">The result value must be accurate to 1.0 ULP</span></span><br/> |
| <span data-ttu-id="265c7-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="265c7-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="265c7-113">\[dans \] le nombre à prendre la réciproque de.</span><span class="sxs-lookup"><span data-stu-id="265c7-113">\[in\] The number to take the reciprocal of.</span></span><br/>                                                                         |



 

## <a name="remarks"></a><span data-ttu-id="265c7-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="265c7-114">Remarks</span></span>

<span data-ttu-id="265c7-115">L’instruction DRCP est émise par le compilateur HLSL uniquement lorsqu’il est appelé explicitement par le biais de l’intrinsèque RCP (), quand un double est utilisé comme argument.</span><span class="sxs-lookup"><span data-stu-id="265c7-115">The DRCP instruction is emitted by the HLSL compiler only when explicitly called via the rcp() intrinsic, when a double is used as the argument.</span></span> <span data-ttu-id="265c7-116">La précision de cette instruction doit être de 1,0 ULP.</span><span class="sxs-lookup"><span data-stu-id="265c7-116">The accuracy of this instruction is required to be 1.0 ULP.</span></span>

<span data-ttu-id="265c7-117">Les nuanceurs qui utilisent cette instruction sont marqués d’un indicateur de nuanceur qui entraîne l’échec de la liaison de ces derniers, sauf si toutes les conditions suivantes sont remplies.</span><span class="sxs-lookup"><span data-stu-id="265c7-117">Shaders that use this instruction will be marked with a shader flag that will cause them to fail to bind unless all the following conditions are met.</span></span>

-   <span data-ttu-id="265c7-118">Le système prend en charge DirectX 11,1.</span><span class="sxs-lookup"><span data-stu-id="265c7-118">The system supports DirectX 11.1.</span></span>
-   <span data-ttu-id="265c7-119">Le système comprend un pilote WDDM 1,2.</span><span class="sxs-lookup"><span data-stu-id="265c7-119">The system includes a WDDM 1.2 driver.</span></span>
-   <span data-ttu-id="265c7-120">Le pilote fournit une prise en charge pour cette instruction via les **\_ options d3d11 des données de la fonctionnalité d3d11 \_ \_ \_ . ExtendedDoublesShaderInstructions** défini sur **true**.</span><span class="sxs-lookup"><span data-stu-id="265c7-120">The driver reports support for this instruction via **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS.ExtendedDoublesShaderInstructions** set to **TRUE**.</span></span>

<span data-ttu-id="265c7-121">Le tableau suivant présente les résultats obtenus lors de l’exécution de l’instruction avec différentes classes de nombres, en supposant qu’aucun dépassement de capacité ou négatif ne se produit.</span><span class="sxs-lookup"><span data-stu-id="265c7-121">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="265c7-122">Dans ce tableau, F signifie nombre fini-réel.</span><span class="sxs-lookup"><span data-stu-id="265c7-122">In this table F means finite-real number.</span></span>



| <span data-ttu-id="265c7-123">**sources**-></span><span class="sxs-lookup"><span data-stu-id="265c7-123">**src**-></span></span>  | <span data-ttu-id="265c7-124">**-INF**</span><span class="sxs-lookup"><span data-stu-id="265c7-124">**-inf**</span></span> | <span data-ttu-id="265c7-125">**-F**</span><span class="sxs-lookup"><span data-stu-id="265c7-125">**-F**</span></span> | <span data-ttu-id="265c7-126">**-0**</span><span class="sxs-lookup"><span data-stu-id="265c7-126">**-0**</span></span> | <span data-ttu-id="265c7-127">**+0**</span><span class="sxs-lookup"><span data-stu-id="265c7-127">**+0**</span></span> | <span data-ttu-id="265c7-128">**+ F**</span><span class="sxs-lookup"><span data-stu-id="265c7-128">**+F**</span></span> | <span data-ttu-id="265c7-129">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="265c7-129">**+inf**</span></span> | <span data-ttu-id="265c7-130">**NaN**</span><span class="sxs-lookup"><span data-stu-id="265c7-130">**NaN**</span></span> |
|---------------|----------|--------|--------|--------|--------|----------|---------|
| <span data-ttu-id="265c7-131">**dest**-></span><span class="sxs-lookup"><span data-stu-id="265c7-131">**dest**-></span></span> | <span data-ttu-id="265c7-132">-0</span><span class="sxs-lookup"><span data-stu-id="265c7-132">-0</span></span>       | <span data-ttu-id="265c7-133">-F</span><span class="sxs-lookup"><span data-stu-id="265c7-133">-F</span></span>     | <span data-ttu-id="265c7-134">-inf</span><span class="sxs-lookup"><span data-stu-id="265c7-134">-inf</span></span>   | <span data-ttu-id="265c7-135">+inf</span><span class="sxs-lookup"><span data-stu-id="265c7-135">+inf</span></span>   | <span data-ttu-id="265c7-136">+ F</span><span class="sxs-lookup"><span data-stu-id="265c7-136">+F</span></span>     | <span data-ttu-id="265c7-137">+0</span><span class="sxs-lookup"><span data-stu-id="265c7-137">+0</span></span>       | <span data-ttu-id="265c7-138">NaN</span><span class="sxs-lookup"><span data-stu-id="265c7-138">NaN</span></span>     |



 

<span data-ttu-id="265c7-139">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="265c7-139">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="265c7-140">Sommet</span><span class="sxs-lookup"><span data-stu-id="265c7-140">Vertex</span></span> | <span data-ttu-id="265c7-141">Forme</span><span class="sxs-lookup"><span data-stu-id="265c7-141">Hull</span></span> | <span data-ttu-id="265c7-142">Domain</span><span class="sxs-lookup"><span data-stu-id="265c7-142">Domain</span></span> | <span data-ttu-id="265c7-143">Géométrie</span><span class="sxs-lookup"><span data-stu-id="265c7-143">Geometry</span></span> | <span data-ttu-id="265c7-144">Pixel</span><span class="sxs-lookup"><span data-stu-id="265c7-144">Pixel</span></span> | <span data-ttu-id="265c7-145">Calcul</span><span class="sxs-lookup"><span data-stu-id="265c7-145">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="265c7-146">X</span><span class="sxs-lookup"><span data-stu-id="265c7-146">X</span></span>      | <span data-ttu-id="265c7-147">X</span><span class="sxs-lookup"><span data-stu-id="265c7-147">X</span></span>    | <span data-ttu-id="265c7-148">X</span><span class="sxs-lookup"><span data-stu-id="265c7-148">X</span></span>      | <span data-ttu-id="265c7-149">X</span><span class="sxs-lookup"><span data-stu-id="265c7-149">X</span></span>        | <span data-ttu-id="265c7-150">X</span><span class="sxs-lookup"><span data-stu-id="265c7-150">X</span></span>     | <span data-ttu-id="265c7-151">X</span><span class="sxs-lookup"><span data-stu-id="265c7-151">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="265c7-152">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="265c7-152">Minimum Shader Model</span></span>

<span data-ttu-id="265c7-153">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="265c7-153">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="265c7-154">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="265c7-154">Shader Model</span></span>                                              | <span data-ttu-id="265c7-155">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="265c7-155">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="265c7-156">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="265c7-156">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="265c7-157">oui</span><span class="sxs-lookup"><span data-stu-id="265c7-157">yes</span></span>       |
| [<span data-ttu-id="265c7-158">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="265c7-158">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="265c7-159">non</span><span class="sxs-lookup"><span data-stu-id="265c7-159">no</span></span>        |
| [<span data-ttu-id="265c7-160">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="265c7-160">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="265c7-161">non</span><span class="sxs-lookup"><span data-stu-id="265c7-161">no</span></span>        |
| [<span data-ttu-id="265c7-162">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="265c7-162">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="265c7-163">non</span><span class="sxs-lookup"><span data-stu-id="265c7-163">no</span></span>        |
| [<span data-ttu-id="265c7-164">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="265c7-164">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="265c7-165">non</span><span class="sxs-lookup"><span data-stu-id="265c7-165">no</span></span>        |
| [<span data-ttu-id="265c7-166">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="265c7-166">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="265c7-167">non</span><span class="sxs-lookup"><span data-stu-id="265c7-167">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="265c7-168">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="265c7-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="265c7-169">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="265c7-169">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





