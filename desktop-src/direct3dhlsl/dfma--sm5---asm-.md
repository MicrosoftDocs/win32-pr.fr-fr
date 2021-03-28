---
title: DFMA (SM5-ASM)
description: Effectue un ajout de multiplication par fusion.
ms.assetid: 5BE96CDB-1756-4EBE-B4CC-69EFF098A4F1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2e6cafc71dbc7d57655524b1b87c9c5b9ba20f3
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313657"
---
# <a name="dfma-sm5---asm"></a><span data-ttu-id="443fe-103">DFMA (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="443fe-103">dfma (sm5 - asm)</span></span>

<span data-ttu-id="443fe-104">Effectue un ajout de multiplication par fusion.</span><span class="sxs-lookup"><span data-stu-id="443fe-104">Performs a fused-multiply add.</span></span>



| <span data-ttu-id="443fe-105">DFMA \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src2 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="443fe-105">dfma\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],\[-\]src2\[\_abs\]\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="443fe-106">Élément</span><span class="sxs-lookup"><span data-stu-id="443fe-106">Item</span></span>                                                            | <span data-ttu-id="443fe-107">Description</span><span class="sxs-lookup"><span data-stu-id="443fe-107">Description</span></span>                                                                                                                                               |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="443fe-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="443fe-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="443fe-109">\[dans \] l’adresse du résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="443fe-109">\[in\] The address of the result of the operation.</span></span> <span data-ttu-id="443fe-110">La valeur de résultat doit être précise à 0,5 ULP.</span><span class="sxs-lookup"><span data-stu-id="443fe-110">The result value must be accurate to 0.5 ULP.</span></span><br/> <span data-ttu-id="443fe-111">*dest*  =  . *src0* \* *src1*  +  *src2*</span><span class="sxs-lookup"><span data-stu-id="443fe-111">*dest* = *src0* \* *src1* + *src2*</span></span><br/> |
| <span data-ttu-id="443fe-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="443fe-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="443fe-113">\[dans \] les composants à multiplier avec *src1*.</span><span class="sxs-lookup"><span data-stu-id="443fe-113">\[in\] The components to multiply with *src1*.</span></span><br/>                                                                                                 |
| <span data-ttu-id="443fe-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="443fe-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="443fe-115">\[dans \] les composants à multiplier avec *src0*.</span><span class="sxs-lookup"><span data-stu-id="443fe-115">\[in\] The components to multiply with *src0*.</span></span><br/>                                                                                                 |
| <span data-ttu-id="443fe-116"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="443fe-116"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="443fe-117">\[dans \] les composants à ajouter à *src0* \* *src1*.</span><span class="sxs-lookup"><span data-stu-id="443fe-117">\[in\] The components to add to *src0* \* *src1*.</span></span><br/>                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="443fe-118">Notes</span><span class="sxs-lookup"><span data-stu-id="443fe-118">Remarks</span></span>

<span data-ttu-id="443fe-119">Les nuanceurs qui utilisent cette instruction sont marqués d’un indicateur de nuanceur qui entraîne l’échec de la liaison de ces derniers, sauf si toutes les conditions suivantes sont remplies.</span><span class="sxs-lookup"><span data-stu-id="443fe-119">Shaders that use this instruction will be marked with a shader flag that will cause them to fail to bind unless all the following conditions are met.</span></span>

-   <span data-ttu-id="443fe-120">Le système prend en charge DirectX 11,1.</span><span class="sxs-lookup"><span data-stu-id="443fe-120">The system supports DirectX 11.1.</span></span>
-   <span data-ttu-id="443fe-121">Le système comprend un pilote WDDM 1,2.</span><span class="sxs-lookup"><span data-stu-id="443fe-121">The system includes a WDDM 1.2 driver.</span></span>
-   <span data-ttu-id="443fe-122">Le pilote fournit une prise en charge pour cette instruction via les **\_ options d3d11 des données de la fonctionnalité d3d11 \_ \_ \_ . ExtendedDoublesShaderInstructions** défini sur **true**.</span><span class="sxs-lookup"><span data-stu-id="443fe-122">The driver reports support for this instruction via **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS.ExtendedDoublesShaderInstructions** set to **TRUE**.</span></span>

<span data-ttu-id="443fe-123">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="443fe-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="443fe-124">Sommet</span><span class="sxs-lookup"><span data-stu-id="443fe-124">Vertex</span></span> | <span data-ttu-id="443fe-125">Forme</span><span class="sxs-lookup"><span data-stu-id="443fe-125">Hull</span></span> | <span data-ttu-id="443fe-126">Domain</span><span class="sxs-lookup"><span data-stu-id="443fe-126">Domain</span></span> | <span data-ttu-id="443fe-127">Géométrie</span><span class="sxs-lookup"><span data-stu-id="443fe-127">Geometry</span></span> | <span data-ttu-id="443fe-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="443fe-128">Pixel</span></span> | <span data-ttu-id="443fe-129">Compute</span><span class="sxs-lookup"><span data-stu-id="443fe-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="443fe-130">X</span><span class="sxs-lookup"><span data-stu-id="443fe-130">X</span></span>      | <span data-ttu-id="443fe-131">X</span><span class="sxs-lookup"><span data-stu-id="443fe-131">X</span></span>    | <span data-ttu-id="443fe-132">X</span><span class="sxs-lookup"><span data-stu-id="443fe-132">X</span></span>      | <span data-ttu-id="443fe-133">X</span><span class="sxs-lookup"><span data-stu-id="443fe-133">X</span></span>        | <span data-ttu-id="443fe-134">X</span><span class="sxs-lookup"><span data-stu-id="443fe-134">X</span></span>     | <span data-ttu-id="443fe-135">X</span><span class="sxs-lookup"><span data-stu-id="443fe-135">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="443fe-136">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="443fe-136">Minimum Shader Model</span></span>

<span data-ttu-id="443fe-137">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="443fe-137">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="443fe-138">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="443fe-138">Shader Model</span></span>                                              | <span data-ttu-id="443fe-139">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="443fe-139">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="443fe-140">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="443fe-140">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="443fe-141">Oui</span><span class="sxs-lookup"><span data-stu-id="443fe-141">yes</span></span>       |
| [<span data-ttu-id="443fe-142">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="443fe-142">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="443fe-143">non</span><span class="sxs-lookup"><span data-stu-id="443fe-143">no</span></span>        |
| [<span data-ttu-id="443fe-144">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="443fe-144">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="443fe-145">non</span><span class="sxs-lookup"><span data-stu-id="443fe-145">no</span></span>        |
| [<span data-ttu-id="443fe-146">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="443fe-146">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="443fe-147">non</span><span class="sxs-lookup"><span data-stu-id="443fe-147">no</span></span>        |
| [<span data-ttu-id="443fe-148">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="443fe-148">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="443fe-149">non</span><span class="sxs-lookup"><span data-stu-id="443fe-149">no</span></span>        |
| [<span data-ttu-id="443fe-150">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="443fe-150">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="443fe-151">non</span><span class="sxs-lookup"><span data-stu-id="443fe-151">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="443fe-152">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="443fe-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="443fe-153">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="443fe-153">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





