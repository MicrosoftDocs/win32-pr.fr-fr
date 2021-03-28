---
title: ld_structured (SM5-ASM)
description: Lecture à accès aléatoire des composants 32 bits 1-4 à partir d’une mémoire tampon structurée.
ms.assetid: ED572B76-FF6C-405E-9110-4B12AD5E5AE6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00a34bafdcfbe0658723dd83d62507e255ff4bfa
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381191"
---
# <a name="ld_structured-sm5---asm"></a><span data-ttu-id="92410-103">LD \_ structuré (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="92410-103">ld\_structured (sm5 - asm)</span></span>

<span data-ttu-id="92410-104">Lecture à accès aléatoire des composants 32 bits 1-4 à partir d’une mémoire tampon structurée.</span><span class="sxs-lookup"><span data-stu-id="92410-104">Random-access read of 1-4 32bit components from a structured buffer.</span></span>



| <span data-ttu-id="92410-105">: LD \_ dst0 \[ . Mask \] , srcAddress \[ . Select, \_ composant, \] srcByteOffset \[ . Select \_ Component \] , src0 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="92410-105">: ld\_structured dst0\[.mask\], srcAddress\[.select\_component\], srcByteOffset\[.select\_component\], src0\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="92410-106">Élément</span><span class="sxs-lookup"><span data-stu-id="92410-106">Item</span></span>                                                                                                                       | <span data-ttu-id="92410-107">Description</span><span class="sxs-lookup"><span data-stu-id="92410-107">Description</span></span>                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92410-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="92410-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                            | <span data-ttu-id="92410-109">\[dans \] l’adresse des résultats de l’opération.</span><span class="sxs-lookup"><span data-stu-id="92410-109">\[in\] The address of the results of the operation.</span></span><br/>                                                                                             |
| <span data-ttu-id="92410-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="92410-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>             | <span data-ttu-id="92410-111">\[dans \] spécifie l’index de la structure à lire.</span><span class="sxs-lookup"><span data-stu-id="92410-111">\[in\] Specifies the index of the structure to read.</span></span><br/>                                                                                            |
| <span data-ttu-id="92410-112"><span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcByteOffset*</span><span class="sxs-lookup"><span data-stu-id="92410-112"><span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcByteOffset*</span></span><br/> | <span data-ttu-id="92410-113">\[dans \] spécifie l’offset d’octet dans la structure à partir duquel commencer la lecture.</span><span class="sxs-lookup"><span data-stu-id="92410-113">\[in\] Specifies the byte offset in the structure to start reading from.</span></span> <br/>                                                                       |
| <span data-ttu-id="92410-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="92410-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                            | <span data-ttu-id="92410-115">Mémoire tampon à partir de laquelle effectuer la lecture.</span><span class="sxs-lookup"><span data-stu-id="92410-115">The buffer to read from.</span></span> <span data-ttu-id="92410-116">Ce paramètre doit être un SRV (t \# ), UAV (u \# ).</span><span class="sxs-lookup"><span data-stu-id="92410-116">This parameter must be a SRV (t\#), UAV (u\#).</span></span> <span data-ttu-id="92410-117">Dans le nuanceur de calcul, il peut également s’agir d’une mémoire partagée de groupe de threads (g \# ).</span><span class="sxs-lookup"><span data-stu-id="92410-117">In the compute shader it can also be thread group shared memory (g\#).</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="92410-118">Notes</span><span class="sxs-lookup"><span data-stu-id="92410-118">Remarks</span></span>

<span data-ttu-id="92410-119">Les données lues à partir de la structure sont équivalentes au pseudocode suivant : où nous avons le décalage, l’adresse, le pointeur vers le contenu de la mémoire tampon, la Stride de la source et les données stockées de façon linéaire.</span><span class="sxs-lookup"><span data-stu-id="92410-119">The data read from the structure is equivalent to the following pseudocode: where we have the offset, address, pointer to the buffer contents, stride of the source, and the data stored linearly.</span></span>

``` syntax
                    BYTE *BufferContents;         // from SRV or UAV
                    UINT BufferStride;            // from base resource
                    UINT srcAddress, srcByteOffset;   // from source registers
                    BYTE *ReadLocation;           // value to calculate
                    ReadLocation = BufferContents 
                                + BufferStride * srcByteOffset
                                + srcOffset;

                    UINT32 Temp[4];  // used to make code shorter

                    // apply the source resource swizzle on source data
                    Temp = read_and_swizzle(ReadLocation, srcSwizzle);

                    // write the components to the output based on mask
                    ApplyWriteMask(dstRegister, dstWriteMask, Temp);
```

<span data-ttu-id="92410-120">Ce pseudocode montre comment fonctionne l’opération, mais les données réelles n’ont pas besoin d’être stockées de façon linéaire.</span><span class="sxs-lookup"><span data-stu-id="92410-120">This pseudocode shows how the operation functions, but the actual data does not have to be stored linearly.</span></span> <span data-ttu-id="92410-121">Si les données ne sont pas stockées de façon linéaire, l’opération réelle de l’instruction doit correspondre au comportement de l’opération ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="92410-121">If the data is not stored linearly, the actual operation of the instruction needs to match the behavior of the above operation.</span></span>

<span data-ttu-id="92410-122">L’adressage hors limites sur u \# /t \# d’un composant 32 bits donné retourne 0 pour ce composant, sauf si *srcByteOffset*, plus Swizzle est ce qui entraîne l’accès à Unlimited à vous \# /t \# , la valeur retournée pour tous les composants n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="92410-122">Out of bounds addressing on u\#/t\# of any given 32-bit component returns 0 for that component, except if *srcByteOffset*, plus swizzle is what causes out of bounds access to u\#/t\#, the returned value for all component(s) is undefined.</span></span>

<span data-ttu-id="92410-123">En dehors des limites, l’adressage sur g \# (les limites de ce g particulier \# , par opposition à toute la mémoire partagée) pour un composant 32 bits donné retourne un résultat non défini.</span><span class="sxs-lookup"><span data-stu-id="92410-123">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) for any given 32-bit component returns an undefined result.</span></span>

<span data-ttu-id="92410-124">*srcByteOffset* est un argument distinct de *srcAddress* , car il s’agit généralement d’un littéral.</span><span class="sxs-lookup"><span data-stu-id="92410-124">*srcByteOffset* is a separate argument from *srcAddress* because it is commonly a literal.</span></span> <span data-ttu-id="92410-125">Cette séparation des paramètres n’a pas été effectuée pour les atomices sur la mémoire structurée.</span><span class="sxs-lookup"><span data-stu-id="92410-125">This parameter separation has not been done for atomics on structured memory.</span></span>

<span data-ttu-id="92410-126">CS \_ 4 \_ 0 et CS \_ 4 \_ 1 prennent en charge cette instruction pour UAV, SRV et TGSM.</span><span class="sxs-lookup"><span data-stu-id="92410-126">cs\_4\_0 and cs\_4\_1 support this instruction for UAV, SRV, and TGSM.</span></span>

<span data-ttu-id="92410-127">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="92410-127">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="92410-128">Sommet</span><span class="sxs-lookup"><span data-stu-id="92410-128">Vertex</span></span> | <span data-ttu-id="92410-129">Forme</span><span class="sxs-lookup"><span data-stu-id="92410-129">Hull</span></span> | <span data-ttu-id="92410-130">Domain</span><span class="sxs-lookup"><span data-stu-id="92410-130">Domain</span></span> | <span data-ttu-id="92410-131">Géométrie</span><span class="sxs-lookup"><span data-stu-id="92410-131">Geometry</span></span> | <span data-ttu-id="92410-132">Pixel</span><span class="sxs-lookup"><span data-stu-id="92410-132">Pixel</span></span> | <span data-ttu-id="92410-133">Compute</span><span class="sxs-lookup"><span data-stu-id="92410-133">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="92410-134">X</span><span class="sxs-lookup"><span data-stu-id="92410-134">X</span></span>      | <span data-ttu-id="92410-135">X</span><span class="sxs-lookup"><span data-stu-id="92410-135">X</span></span>    | <span data-ttu-id="92410-136">X</span><span class="sxs-lookup"><span data-stu-id="92410-136">X</span></span>      | <span data-ttu-id="92410-137">X</span><span class="sxs-lookup"><span data-stu-id="92410-137">X</span></span>        | <span data-ttu-id="92410-138">X</span><span class="sxs-lookup"><span data-stu-id="92410-138">X</span></span>     | <span data-ttu-id="92410-139">X</span><span class="sxs-lookup"><span data-stu-id="92410-139">X</span></span>       |



 

<span data-ttu-id="92410-140">Étant donné que les UAVs sont disponibles à toutes les étapes de nuanceur pour Direct3D 11,1, cette instruction s’applique à toutes les étapes de nuanceur pour UAVs pour le runtime Direct3D 11,1, disponible à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="92410-140">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for UAVs for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="92410-141">Sommet</span><span class="sxs-lookup"><span data-stu-id="92410-141">Vertex</span></span> | <span data-ttu-id="92410-142">Forme</span><span class="sxs-lookup"><span data-stu-id="92410-142">Hull</span></span> | <span data-ttu-id="92410-143">Domain</span><span class="sxs-lookup"><span data-stu-id="92410-143">Domain</span></span> | <span data-ttu-id="92410-144">Géométrie</span><span class="sxs-lookup"><span data-stu-id="92410-144">Geometry</span></span> | <span data-ttu-id="92410-145">Pixel</span><span class="sxs-lookup"><span data-stu-id="92410-145">Pixel</span></span> | <span data-ttu-id="92410-146">Compute</span><span class="sxs-lookup"><span data-stu-id="92410-146">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="92410-147">X</span><span class="sxs-lookup"><span data-stu-id="92410-147">X</span></span>      | <span data-ttu-id="92410-148">X</span><span class="sxs-lookup"><span data-stu-id="92410-148">X</span></span>    | <span data-ttu-id="92410-149">X</span><span class="sxs-lookup"><span data-stu-id="92410-149">X</span></span>      | <span data-ttu-id="92410-150">X</span><span class="sxs-lookup"><span data-stu-id="92410-150">X</span></span>        | <span data-ttu-id="92410-151">X</span><span class="sxs-lookup"><span data-stu-id="92410-151">X</span></span>     | <span data-ttu-id="92410-152">X</span><span class="sxs-lookup"><span data-stu-id="92410-152">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="92410-153">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="92410-153">Minimum Shader Model</span></span>

<span data-ttu-id="92410-154">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="92410-154">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="92410-155">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="92410-155">Shader Model</span></span>                                              | <span data-ttu-id="92410-156">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="92410-156">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="92410-157">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="92410-157">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="92410-158">Oui</span><span class="sxs-lookup"><span data-stu-id="92410-158">yes</span></span>       |
| [<span data-ttu-id="92410-159">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="92410-159">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="92410-160">non</span><span class="sxs-lookup"><span data-stu-id="92410-160">no</span></span>        |
| [<span data-ttu-id="92410-161">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="92410-161">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="92410-162">non</span><span class="sxs-lookup"><span data-stu-id="92410-162">no</span></span>        |
| [<span data-ttu-id="92410-163">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="92410-163">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="92410-164">non</span><span class="sxs-lookup"><span data-stu-id="92410-164">no</span></span>        |
| [<span data-ttu-id="92410-165">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="92410-165">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="92410-166">non</span><span class="sxs-lookup"><span data-stu-id="92410-166">no</span></span>        |
| [<span data-ttu-id="92410-167">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="92410-167">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="92410-168">non</span><span class="sxs-lookup"><span data-stu-id="92410-168">no</span></span>        |



 

<span data-ttu-id="92410-169">CS \_ 4 \_ 0 et CS \_ 4 \_ 1 prennent en charge cette instruction pour UAV, SRV et TGSM.</span><span class="sxs-lookup"><span data-stu-id="92410-169">cs\_4\_0 and cs\_4\_1 support this instruction for UAV, SRV and TGSM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="92410-170">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="92410-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92410-171">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="92410-171">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





