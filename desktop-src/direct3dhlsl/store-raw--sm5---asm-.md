---
title: store_raw (SM5-ASM)
description: Écriture à accès aléatoire des composants 32 bits 1-4 dans la mémoire de type.
ms.assetid: D166116A-CF4E-4020-9F6A-F9CEEFCDAB21
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c44b4d22a576853fb8b7d2c43fcb6a2d7fc9a448
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381217"
---
# <a name="store_raw-sm5---asm"></a><span data-ttu-id="d554b-103">stocker \_ brut (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="d554b-103">store\_raw (sm5 - asm)</span></span>

<span data-ttu-id="d554b-104">Écriture à accès aléatoire des composants 32 bits 1-4 dans la mémoire de type.</span><span class="sxs-lookup"><span data-stu-id="d554b-104">Random-access write of 1-4 32bit components into typeless memory.</span></span>



| <span data-ttu-id="d554b-105">stocker le \_ \[ masque dst0. Write brut \_ \] , dstByteOffset \[ . Select \_ Component \] , src0 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="d554b-105">store\_raw dst0\[.write\_mask\], dstByteOffset\[.select\_component\], src0\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------------|



 



| <span data-ttu-id="d554b-106">Élément</span><span class="sxs-lookup"><span data-stu-id="d554b-106">Item</span></span>                                                                                                                       | <span data-ttu-id="d554b-107">Description</span><span class="sxs-lookup"><span data-stu-id="d554b-107">Description</span></span>                                |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span data-ttu-id="d554b-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="d554b-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                            | <span data-ttu-id="d554b-109">\[dans \] l’adresse mémoire.</span><span class="sxs-lookup"><span data-stu-id="d554b-109">\[in\] The memory address.</span></span><br/>      |
| <span data-ttu-id="d554b-110"><span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*dstByteOffset*</span><span class="sxs-lookup"><span data-stu-id="d554b-110"><span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*dstByteOffset*</span></span><br/> | <span data-ttu-id="d554b-111">\[dans \] le décalage.</span><span class="sxs-lookup"><span data-stu-id="d554b-111">\[in\] The offset.</span></span><br/>              |
| <span data-ttu-id="d554b-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="d554b-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                            | <span data-ttu-id="d554b-113">\[dans \] les composants à écrire.</span><span class="sxs-lookup"><span data-stu-id="d554b-113">\[in\] The components to write.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d554b-114">Notes</span><span class="sxs-lookup"><span data-stu-id="d554b-114">Remarks</span></span>

<span data-ttu-id="d554b-115">Cette instruction exécute 1-4 \* composants 32 bits écrits à partir de *src0* vers *dst0* à l’offset dans *dstByteOffset*.</span><span class="sxs-lookup"><span data-stu-id="d554b-115">This instruction performs 1-4 component \*32-bit components written from *src0* to *dst0* at the offset in *dstByteOffset*.</span></span> <span data-ttu-id="d554b-116">Il n’y a aucune conversion de format.</span><span class="sxs-lookup"><span data-stu-id="d554b-116">There is no format conversion.</span></span>

<span data-ttu-id="d554b-117">*dst0* doit être un UAV (u \# ) ou, dans le nuanceur de calcul, il peut également s’agir d’une mémoire partagée de groupe de threads (g \# ).</span><span class="sxs-lookup"><span data-stu-id="d554b-117">*dst0* must be a UAV (u\#), or in the compute shader it can also be thread group shared memory (g\#).</span></span>

<span data-ttu-id="d554b-118">*dstByteOffset* spécifie la valeur de base de 32 bits en mémoire pour une fenêtre de 4 valeurs de 32 bits séquentielles dans lesquelles les données peuvent être écrites, en fonction du Swizzle et du masque sur les autres paramètres.</span><span class="sxs-lookup"><span data-stu-id="d554b-118">*dstByteOffset* specifies the base 32-bit value in memory for a window of 4 sequential 32-bit values in which data may be written, depending on the swizzle and mask on other parameters.</span></span>

<span data-ttu-id="d554b-119">L’emplacement des données écrites est équivalent au pseudo-code suivant, qui affiche l’adresse, le pointeur vers le contenu de la mémoire tampon et les données stockées de façon linéaire.</span><span class="sxs-lookup"><span data-stu-id="d554b-119">The location of the data written is equivalent to the following pseudocode which show the address, pointer to the buffer contents, and the data stored linearly.</span></span>

``` syntax
                    BYTE *BufferContents;          // from src0
                    UINT dstByteOffset;            // source register
                    BYTE *WriteLocation;           // value to calculate

                    // calculate writing location
                    WriteLocation = BufferContents 
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
                             WriteComponents * sizeof(UINT32));
```

<span data-ttu-id="d554b-120">Ce pseudocode montre comment fonctionne l’opération, mais les données réelles n’ont pas besoin d’être stockées de façon linéaire.</span><span class="sxs-lookup"><span data-stu-id="d554b-120">This pseudocode shows how the operation functions, but the actual data does not have to be stored linearly.</span></span> <span data-ttu-id="d554b-121">*dst0* peut uniquement avoir un masque d’écriture qui est l’un des suivants :. x,. XY,. xyz,. XYZW.</span><span class="sxs-lookup"><span data-stu-id="d554b-121">*dst0* can only have a write mask that is one of the following: .x, .xy, .xyz, .xyzw.</span></span> <span data-ttu-id="d554b-122">Le masque d’écriture détermine le nombre de composants 32 bits à écrire sans écarts.</span><span class="sxs-lookup"><span data-stu-id="d554b-122">The write mask determines the number of 32bit components to write without gaps.</span></span>

<span data-ttu-id="d554b-123">L’adressage hors limites sur u \# signifie que rien n’est écrit dans la mémoire en dehors des limites ; toute partie qui se trouve dans des limites est écrite correctement.</span><span class="sxs-lookup"><span data-stu-id="d554b-123">Out of bounds addressing on u\# means nothing is written to the out of bounds memory; any part that is in bounds is written correctly.</span></span>

<span data-ttu-id="d554b-124">En dehors des limites d’adressage sur g \# (les limites de ce g particulier \# , par opposition à toute la mémoire partagée) pour un composant 32 bits donné, la totalité du contenu de la mémoire partagée devient non définie.</span><span class="sxs-lookup"><span data-stu-id="d554b-124">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) for any given 32-bit component causes the entire contents of all shared memory to become undefined.</span></span>

<span data-ttu-id="d554b-125">CS \_ 4 \_ 0 et CS \_ 4 \_ 1 prennent en charge cette instruction pour UAV.</span><span class="sxs-lookup"><span data-stu-id="d554b-125">cs\_4\_0 and cs\_4\_1 support this instruction for UAV.</span></span>

<span data-ttu-id="d554b-126">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="d554b-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d554b-127">Sommet</span><span class="sxs-lookup"><span data-stu-id="d554b-127">Vertex</span></span> | <span data-ttu-id="d554b-128">Forme</span><span class="sxs-lookup"><span data-stu-id="d554b-128">Hull</span></span> | <span data-ttu-id="d554b-129">Domain</span><span class="sxs-lookup"><span data-stu-id="d554b-129">Domain</span></span> | <span data-ttu-id="d554b-130">Géométrie</span><span class="sxs-lookup"><span data-stu-id="d554b-130">Geometry</span></span> | <span data-ttu-id="d554b-131">Pixel</span><span class="sxs-lookup"><span data-stu-id="d554b-131">Pixel</span></span> | <span data-ttu-id="d554b-132">Compute</span><span class="sxs-lookup"><span data-stu-id="d554b-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="d554b-133">X</span><span class="sxs-lookup"><span data-stu-id="d554b-133">X</span></span>     | <span data-ttu-id="d554b-134">X</span><span class="sxs-lookup"><span data-stu-id="d554b-134">X</span></span>       |



 

<span data-ttu-id="d554b-135">Étant donné que les UAVs sont disponibles à toutes les étapes de nuanceur pour Direct3D 11,1, cette instruction s’applique à toutes les étapes de nuanceur pour le runtime Direct3D 11,1, disponible à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d554b-135">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="d554b-136">Sommet</span><span class="sxs-lookup"><span data-stu-id="d554b-136">Vertex</span></span> | <span data-ttu-id="d554b-137">Forme</span><span class="sxs-lookup"><span data-stu-id="d554b-137">Hull</span></span> | <span data-ttu-id="d554b-138">Domain</span><span class="sxs-lookup"><span data-stu-id="d554b-138">Domain</span></span> | <span data-ttu-id="d554b-139">Géométrie</span><span class="sxs-lookup"><span data-stu-id="d554b-139">Geometry</span></span> | <span data-ttu-id="d554b-140">Pixel</span><span class="sxs-lookup"><span data-stu-id="d554b-140">Pixel</span></span> | <span data-ttu-id="d554b-141">Compute</span><span class="sxs-lookup"><span data-stu-id="d554b-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="d554b-142">X</span><span class="sxs-lookup"><span data-stu-id="d554b-142">X</span></span>      | <span data-ttu-id="d554b-143">X</span><span class="sxs-lookup"><span data-stu-id="d554b-143">X</span></span>    | <span data-ttu-id="d554b-144">X</span><span class="sxs-lookup"><span data-stu-id="d554b-144">X</span></span>      | <span data-ttu-id="d554b-145">X</span><span class="sxs-lookup"><span data-stu-id="d554b-145">X</span></span>        | <span data-ttu-id="d554b-146">X</span><span class="sxs-lookup"><span data-stu-id="d554b-146">X</span></span>     | <span data-ttu-id="d554b-147">X</span><span class="sxs-lookup"><span data-stu-id="d554b-147">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d554b-148">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="d554b-148">Minimum Shader Model</span></span>

<span data-ttu-id="d554b-149">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="d554b-149">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="d554b-150">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="d554b-150">Shader Model</span></span>                                              | <span data-ttu-id="d554b-151">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="d554b-151">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d554b-152">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="d554b-152">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d554b-153">Oui</span><span class="sxs-lookup"><span data-stu-id="d554b-153">yes</span></span>       |
| [<span data-ttu-id="d554b-154">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="d554b-154">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d554b-155">non</span><span class="sxs-lookup"><span data-stu-id="d554b-155">no</span></span>        |
| [<span data-ttu-id="d554b-156">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="d554b-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d554b-157">non</span><span class="sxs-lookup"><span data-stu-id="d554b-157">no</span></span>        |
| [<span data-ttu-id="d554b-158">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d554b-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d554b-159">non</span><span class="sxs-lookup"><span data-stu-id="d554b-159">no</span></span>        |
| [<span data-ttu-id="d554b-160">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d554b-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d554b-161">non</span><span class="sxs-lookup"><span data-stu-id="d554b-161">no</span></span>        |
| [<span data-ttu-id="d554b-162">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d554b-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d554b-163">non</span><span class="sxs-lookup"><span data-stu-id="d554b-163">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d554b-164">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d554b-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d554b-165">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d554b-165">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





