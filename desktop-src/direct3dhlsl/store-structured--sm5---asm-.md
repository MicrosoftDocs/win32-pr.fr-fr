---
title: store_structured (SM5-ASM)
description: Écriture à accès aléatoire des composants 1-4 32 bits dans une vue de l’accès non ordonné de la mémoire tampon structurée (UAV).
ms.assetid: 8080B2CA-5BDA-4F01-8B2B-B85BDD58C5AF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5890d30fac57923365f0bdea89fcce55f7922c7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104030574"
---
# <a name="store_structured-sm5---asm"></a><span data-ttu-id="3b745-103">stockage \_ structuré (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="3b745-103">store\_structured (sm5 - asm)</span></span>

<span data-ttu-id="3b745-104">Écriture à accès aléatoire des composants 1-4 32 bits dans une vue de l’accès non ordonné de la mémoire tampon structurée (UAV).</span><span class="sxs-lookup"><span data-stu-id="3b745-104">Random-access write of 1-4 32-bit components into a structured buffer unordered access view (UAV).</span></span>



| <span data-ttu-id="3b745-105">stocker le \_ \[ masque dst0. Write structuré \_ \] , dstAddress \[ . Select \_ Component \] , dstByteOffset \[ . Select \_ Component \] , src0 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="3b745-105">store\_structured dst0\[.write\_mask\], dstAddress\[.select\_component\], dstByteOffset\[.select\_component\], src0\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="3b745-106">Élément</span><span class="sxs-lookup"><span data-stu-id="3b745-106">Item</span></span>                                                                                                                       | <span data-ttu-id="3b745-107">Description</span><span class="sxs-lookup"><span data-stu-id="3b745-107">Description</span></span>                                                    |
|----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="3b745-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="3b745-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                            | <span data-ttu-id="3b745-109">\[dans \] l’adresse des résultats de l’opération.</span><span class="sxs-lookup"><span data-stu-id="3b745-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="3b745-110"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="3b745-110"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/>             | <span data-ttu-id="3b745-111">\[dans \] l’adresse à laquelle écrire.</span><span class="sxs-lookup"><span data-stu-id="3b745-111">\[in\] The address at which to write.</span></span><br/>               |
| <span data-ttu-id="3b745-112"><span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*dstByteOffset*</span><span class="sxs-lookup"><span data-stu-id="3b745-112"><span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*dstByteOffset*</span></span><br/> | <span data-ttu-id="3b745-113">\[dans \] l’index de la structure à écrire.</span><span class="sxs-lookup"><span data-stu-id="3b745-113">\[in\] The index of the structure to write.</span></span><br/>         |
| <span data-ttu-id="3b745-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="3b745-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                            | <span data-ttu-id="3b745-115">\[dans \] les composants à écrire.</span><span class="sxs-lookup"><span data-stu-id="3b745-115">\[in\] The components to write.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="3b745-116">Notes</span><span class="sxs-lookup"><span data-stu-id="3b745-116">Remarks</span></span>

<span data-ttu-id="3b745-117">Cette instruction exécute \* les composants 32 bits 1-4 du composant écrits à partir de *src0* vers *dst0* à l’adresse dans *dstAddress* et *dstByteOffset*.</span><span class="sxs-lookup"><span data-stu-id="3b745-117">This instruction performs 1-4 component \*32bit components written from *src0* to *dst0* at the address in *dstAddress* and *dstByteOffset*.</span></span> <span data-ttu-id="3b745-118">Aucune conversion de format.</span><span class="sxs-lookup"><span data-stu-id="3b745-118">No format conversion.</span></span>

<span data-ttu-id="3b745-119">*dst0* doit être un UAV (u \# ).</span><span class="sxs-lookup"><span data-stu-id="3b745-119">*dst0* must be a UAV (u\#).</span></span> <span data-ttu-id="3b745-120">Dans le nuanceur de calcul, il peut également s’agir d’une mémoire partagée de groupe de threads (g \# ).</span><span class="sxs-lookup"><span data-stu-id="3b745-120">In the compute shader it can also be thread group shared memory (g\#).</span></span>

<span data-ttu-id="3b745-121">*dstAddress* spécifie l’index de la structure à écrire.</span><span class="sxs-lookup"><span data-stu-id="3b745-121">*dstAddress* specifies the index of the structure to write.</span></span>

<span data-ttu-id="3b745-122">L’emplacement des données écrites est équivalent au pseudo-code suivant, qui montre l’offset, l’adresse, le pointeur vers le contenu de la mémoire tampon, la Stride de la source et les données stockées de façon linéaire.</span><span class="sxs-lookup"><span data-stu-id="3b745-122">The location of the data written is equivalent to the following pseudocode which shows the offset, address, pointer to the buffer contents, stride of the source, and the data stored linearly.</span></span>

``` syntax
                    BYTE *BufferContents;             // from dst0
                    UINT BufferStride;                // from dst0
                    UINT dstAddress, dstByteOffset;   // source registers
                    BYTE *WriteLocation;              // value to calculate

                    // calculate writing location
                     WriteLocation = BufferContents 
                                + BufferStride * dstAddress 
                                + dstByteOffset;

                    // calculate the number of components to write
                    switch (dstWriteMask)
                    {
                        x:    WriteComponents = 1; break;
                        xy:   WriteComponents = 2; break;
                        xyz:  WriteComponents = 3; break;
                        xyzw: WriteComponents = 4; break;
                        default:  // only these masks are valid                              
                    }

                    // copy the data from the source register with
                    //    the swizzle applied
                    memcpy(WriteLocation, swizzle(src0, src0.swizzle), 
                             WriteComponents * sizeof(INT32));
```

<span data-ttu-id="3b745-123">Ce pseudocode montre comment fonctionne l’opération, mais les données réelles n’ont pas besoin d’être stockées de façon linéaire.</span><span class="sxs-lookup"><span data-stu-id="3b745-123">This pseudocode shows how the operation functions, but the actual data does not have to be stored linearly.</span></span> <span data-ttu-id="3b745-124">Si les données ne sont pas stockées de façon linéaire, l’opération réelle de l’instruction doit correspondre au comportement de l’opération ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="3b745-124">If the data is not stored linearly, the actual operation of the instruction needs to match the behavior of the above operation.</span></span>

<span data-ttu-id="3b745-125">*dst0* peut uniquement avoir un masque d’écriture qui est l’un des suivants :. x,. XY,. xyz,. XYZW.</span><span class="sxs-lookup"><span data-stu-id="3b745-125">*dst0* can only have a write mask that is one of the following: .x, .xy, .xyz, .xyzw.</span></span> <span data-ttu-id="3b745-126">Le masque d’écriture détermine le nombre de composants 32 bits à écrire sans intervalles.</span><span class="sxs-lookup"><span data-stu-id="3b745-126">The write mask determines the number of 32-bit components to write without gaps.</span></span>

<span data-ttu-id="3b745-127">L’adressage hors limites sur u- \# attrait par *dstAddress* signifie que rien n’est écrit dans la mémoire hors limites.</span><span class="sxs-lookup"><span data-stu-id="3b745-127">Out of bounds addressing on u\# casued by *dstAddress* means nothing is written to the out of bounds memory.</span></span>

<span data-ttu-id="3b745-128">Si le *dstByteOffset*, y compris *dstWriteMask*, est à l’origine de l’accès hors limites \# , le contenu entier du UAV devient non défini.</span><span class="sxs-lookup"><span data-stu-id="3b745-128">If the *dstByteOffset*, including *dstWriteMask*, is what causes out of bounds access to u\#, the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="3b745-129">En dehors des limites d’adressage sur g \# (les limites de ce g particulier \# , par opposition à toute la mémoire partagée) pour un composant 32 bits donné, la totalité du contenu de la mémoire partagée devient non définie.</span><span class="sxs-lookup"><span data-stu-id="3b745-129">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) for any given 32-bit component causes the entire contents of all shared memory to become undefined.</span></span>

<span data-ttu-id="3b745-130">*dstByteOffset* est un argument distinct de *dstAddress* , car il s’agit généralement d’un littéral.</span><span class="sxs-lookup"><span data-stu-id="3b745-130">*dstByteOffset* is a separate argument from *dstAddress* because it is commonly a literal.</span></span> <span data-ttu-id="3b745-131">Cette séparation des paramètres n’a pas été effectuée pour les atomices sur la mémoire structurée.</span><span class="sxs-lookup"><span data-stu-id="3b745-131">This parameter separation has not been done for atomics on structured memory.</span></span>

<span data-ttu-id="3b745-132">CS \_ 4 \_ 0 et CS \_ 4 \_ 1 prennent en charge cette instruction pour UAV et TGSM.</span><span class="sxs-lookup"><span data-stu-id="3b745-132">cs\_4\_0 and cs\_4\_1 support this instruction for UAV and TGSM.</span></span>

<span data-ttu-id="3b745-133">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="3b745-133">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="3b745-134">Sommet</span><span class="sxs-lookup"><span data-stu-id="3b745-134">Vertex</span></span> | <span data-ttu-id="3b745-135">Forme</span><span class="sxs-lookup"><span data-stu-id="3b745-135">Hull</span></span> | <span data-ttu-id="3b745-136">Domain</span><span class="sxs-lookup"><span data-stu-id="3b745-136">Domain</span></span> | <span data-ttu-id="3b745-137">Géométrie</span><span class="sxs-lookup"><span data-stu-id="3b745-137">Geometry</span></span> | <span data-ttu-id="3b745-138">Pixel</span><span class="sxs-lookup"><span data-stu-id="3b745-138">Pixel</span></span> | <span data-ttu-id="3b745-139">Compute</span><span class="sxs-lookup"><span data-stu-id="3b745-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="3b745-140">X</span><span class="sxs-lookup"><span data-stu-id="3b745-140">X</span></span>     | <span data-ttu-id="3b745-141">X</span><span class="sxs-lookup"><span data-stu-id="3b745-141">X</span></span>       |



 

<span data-ttu-id="3b745-142">Étant donné que les UAVs sont disponibles à toutes les étapes de nuanceur pour Direct3D 11,1, cette instruction s’applique à toutes les étapes de nuanceur pour le runtime Direct3D 11,1, disponible à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3b745-142">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="3b745-143">Sommet</span><span class="sxs-lookup"><span data-stu-id="3b745-143">Vertex</span></span> | <span data-ttu-id="3b745-144">Forme</span><span class="sxs-lookup"><span data-stu-id="3b745-144">Hull</span></span> | <span data-ttu-id="3b745-145">Domain</span><span class="sxs-lookup"><span data-stu-id="3b745-145">Domain</span></span> | <span data-ttu-id="3b745-146">Géométrie</span><span class="sxs-lookup"><span data-stu-id="3b745-146">Geometry</span></span> | <span data-ttu-id="3b745-147">Pixel</span><span class="sxs-lookup"><span data-stu-id="3b745-147">Pixel</span></span> | <span data-ttu-id="3b745-148">Compute</span><span class="sxs-lookup"><span data-stu-id="3b745-148">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="3b745-149">X</span><span class="sxs-lookup"><span data-stu-id="3b745-149">X</span></span>      | <span data-ttu-id="3b745-150">X</span><span class="sxs-lookup"><span data-stu-id="3b745-150">X</span></span>    | <span data-ttu-id="3b745-151">X</span><span class="sxs-lookup"><span data-stu-id="3b745-151">X</span></span>      | <span data-ttu-id="3b745-152">X</span><span class="sxs-lookup"><span data-stu-id="3b745-152">X</span></span>        | <span data-ttu-id="3b745-153">X</span><span class="sxs-lookup"><span data-stu-id="3b745-153">X</span></span>     | <span data-ttu-id="3b745-154">X</span><span class="sxs-lookup"><span data-stu-id="3b745-154">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3b745-155">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="3b745-155">Minimum Shader Model</span></span>

<span data-ttu-id="3b745-156">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="3b745-156">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="3b745-157">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="3b745-157">Shader Model</span></span>                                              | <span data-ttu-id="3b745-158">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="3b745-158">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="3b745-159">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="3b745-159">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="3b745-160">Oui</span><span class="sxs-lookup"><span data-stu-id="3b745-160">yes</span></span>       |
| [<span data-ttu-id="3b745-161">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="3b745-161">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="3b745-162">non</span><span class="sxs-lookup"><span data-stu-id="3b745-162">no</span></span>        |
| [<span data-ttu-id="3b745-163">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="3b745-163">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="3b745-164">non</span><span class="sxs-lookup"><span data-stu-id="3b745-164">no</span></span>        |
| [<span data-ttu-id="3b745-165">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3b745-165">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="3b745-166">non</span><span class="sxs-lookup"><span data-stu-id="3b745-166">no</span></span>        |
| [<span data-ttu-id="3b745-167">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3b745-167">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="3b745-168">non</span><span class="sxs-lookup"><span data-stu-id="3b745-168">no</span></span>        |
| [<span data-ttu-id="3b745-169">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3b745-169">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="3b745-170">non</span><span class="sxs-lookup"><span data-stu-id="3b745-170">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="3b745-171">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3b745-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b745-172">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3b745-172">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





