---
title: ld_raw (SM5-ASM)
description: Lecture à accès aléatoire des composants 32 bits 1-4 à partir d’une mémoire tampon brute.
ms.assetid: F7DBA80D-4DD5-4271-B571-24FB6188ABFE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd4a9480ef60098b394e0eff2b06043fd9a32e45
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104971571"
---
# <a name="ld_raw-sm5---asm"></a><span data-ttu-id="403b9-103">LD \_ bruts (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="403b9-103">ld\_raw (sm5 - asm)</span></span>

<span data-ttu-id="403b9-104">Lecture à accès aléatoire des composants 32 bits 1-4 à partir d’une mémoire tampon brute.</span><span class="sxs-lookup"><span data-stu-id="403b9-104">Random-access read of 1-4 32bit components from a raw buffer.</span></span>



| <span data-ttu-id="403b9-105">LD \_ dst0 \[ . Mask \] , srcByteOffset \[ . Select brut, \_ \] src0 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="403b9-105">ld\_raw dst0\[.mask\], srcByteOffset\[.select\_component\], src0\[.swizzle\]</span></span> |
|------------------------------------------------------------------------------|



 



| <span data-ttu-id="403b9-106">Élément</span><span class="sxs-lookup"><span data-stu-id="403b9-106">Item</span></span>                                                                                                                       | <span data-ttu-id="403b9-107">Description</span><span class="sxs-lookup"><span data-stu-id="403b9-107">Description</span></span>                                                   |
|----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="403b9-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="403b9-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                            | <span data-ttu-id="403b9-109">\[dans \] l’adresse du résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="403b9-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="403b9-110"><span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcByteOffset*</span><span class="sxs-lookup"><span data-stu-id="403b9-110"><span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcByteOffset*</span></span><br/> | <span data-ttu-id="403b9-111">\[dans \] spécifie le décalage à partir duquel effectuer la lecture.</span><span class="sxs-lookup"><span data-stu-id="403b9-111">\[in\] Specifies the offset to read from.</span></span><br/>          |
| <span data-ttu-id="403b9-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="403b9-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                            | <span data-ttu-id="403b9-113">\[dans \] le composant à lire.</span><span class="sxs-lookup"><span data-stu-id="403b9-113">\[in\] The component to read.</span></span> <br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="403b9-114">Notes</span><span class="sxs-lookup"><span data-stu-id="403b9-114">Remarks</span></span>

<span data-ttu-id="403b9-115">*src0* doit être :</span><span class="sxs-lookup"><span data-stu-id="403b9-115">*src0* must be:</span></span>

-   <span data-ttu-id="403b9-116">Étape de nuanceur : SRV (t \# ) LD St</span><span class="sxs-lookup"><span data-stu-id="403b9-116">Any shader stage: SRV (t\#)ld st</span></span>
-   <span data-ttu-id="403b9-117">Nuanceur de calcul ou nuanceur de pixels : UAV (u \# )</span><span class="sxs-lookup"><span data-stu-id="403b9-117">Compute shader or pixel shader: UAV (u\#)</span></span>
-   <span data-ttu-id="403b9-118">Nuanceur de calcul : mémoire partagée de groupe de threads (g \# )</span><span class="sxs-lookup"><span data-stu-id="403b9-118">Compute shader: thread group shared memory (g\#)</span></span>

<span data-ttu-id="403b9-119">*srcByteOffset* spécifie la valeur de base de 32 bits en mémoire pour une fenêtre de 4 valeurs 32 bits séquentielles dans lesquelles les données peuvent être lues, en fonction du Swizzle et du masque sur les autres paramètres.</span><span class="sxs-lookup"><span data-stu-id="403b9-119">*srcByteOffset* specifies the base 32-bit value in memory for a window of 4 sequential 32-bit values in which data may be read, depending on the swizzle and mask on other parameters.</span></span>

<span data-ttu-id="403b9-120">Les données lues à partir de la mémoire tampon brute sont équivalentes au pseudocode suivant : où nous avons le décalage, l’adresse, le pointeur vers le contenu de la mémoire tampon, la Stride de la source et les données stockées de façon linéaire.</span><span class="sxs-lookup"><span data-stu-id="403b9-120">The data read from the raw buffer is equivalent to the following pseudocode: where we have the offset, address, pointer to the buffer contents, stride of the source, and the data stored linearly.</span></span>

``` syntax
                    BYTE *BufferContents;         // from src0
                    UINT srcByteOffset;           // from srcRegister
                    BYTE *ReadLocation;           // value to calculate
                    ReadLocation = BufferContents 
                                + srcByteOffset;

                    UINT32 Temp[4];  // used to make code shorter

                    // apply the source resource swizzle on source data
                    Temp = read_and_swizzle(ReadLocation, srcSwizzle);

                    // write the components to the output based on mask
                    ApplyWriteMask(dstRegister, dstWriteMask, Temp);
```

<span data-ttu-id="403b9-121">L’adressage hors limites sur u \# /t \# d’un composant 32 bits donné retourne 0 pour ce composant.</span><span class="sxs-lookup"><span data-stu-id="403b9-121">Out of bounds addressing on u\#/t\# of any given 32-bit component returns 0 for that component.</span></span>

<span data-ttu-id="403b9-122">En dehors des limites, l’adressage sur g \# (les limites de ce g particulier \# , par opposition à toute la mémoire partagée) pour un composant 32 bits donné retourne un résultat non défini.</span><span class="sxs-lookup"><span data-stu-id="403b9-122">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) for any given 32-bit component returns an undefined result.</span></span>

<span data-ttu-id="403b9-123">CS \_ 4 \_ 0 et CS \_ 4 \_ 1 prennent en charge cette instruction pour UAV et SRV.</span><span class="sxs-lookup"><span data-stu-id="403b9-123">cs\_4\_0 and cs\_4\_1 support this instruction for UAV and SRV.</span></span>

<span data-ttu-id="403b9-124">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="403b9-124">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="403b9-125">Sommet</span><span class="sxs-lookup"><span data-stu-id="403b9-125">Vertex</span></span> | <span data-ttu-id="403b9-126">Forme</span><span class="sxs-lookup"><span data-stu-id="403b9-126">Hull</span></span> | <span data-ttu-id="403b9-127">Domain</span><span class="sxs-lookup"><span data-stu-id="403b9-127">Domain</span></span> | <span data-ttu-id="403b9-128">Géométrie</span><span class="sxs-lookup"><span data-stu-id="403b9-128">Geometry</span></span> | <span data-ttu-id="403b9-129">Pixel</span><span class="sxs-lookup"><span data-stu-id="403b9-129">Pixel</span></span> | <span data-ttu-id="403b9-130">Compute</span><span class="sxs-lookup"><span data-stu-id="403b9-130">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="403b9-131">X</span><span class="sxs-lookup"><span data-stu-id="403b9-131">X</span></span>      | <span data-ttu-id="403b9-132">X</span><span class="sxs-lookup"><span data-stu-id="403b9-132">X</span></span>    | <span data-ttu-id="403b9-133">X</span><span class="sxs-lookup"><span data-stu-id="403b9-133">X</span></span>      | <span data-ttu-id="403b9-134">X</span><span class="sxs-lookup"><span data-stu-id="403b9-134">X</span></span>        | <span data-ttu-id="403b9-135">X</span><span class="sxs-lookup"><span data-stu-id="403b9-135">X</span></span>     | <span data-ttu-id="403b9-136">X</span><span class="sxs-lookup"><span data-stu-id="403b9-136">X</span></span>       |



 

<span data-ttu-id="403b9-137">Étant donné que les UAVs sont disponibles à toutes les étapes de nuanceur pour Direct3D 11,1, cette instruction s’applique à toutes les étapes de nuanceur pour UAVs pour le runtime Direct3D 11,1, disponible à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="403b9-137">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for UAVs for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="403b9-138">Sommet</span><span class="sxs-lookup"><span data-stu-id="403b9-138">Vertex</span></span> | <span data-ttu-id="403b9-139">Forme</span><span class="sxs-lookup"><span data-stu-id="403b9-139">Hull</span></span> | <span data-ttu-id="403b9-140">Domain</span><span class="sxs-lookup"><span data-stu-id="403b9-140">Domain</span></span> | <span data-ttu-id="403b9-141">Géométrie</span><span class="sxs-lookup"><span data-stu-id="403b9-141">Geometry</span></span> | <span data-ttu-id="403b9-142">Pixel</span><span class="sxs-lookup"><span data-stu-id="403b9-142">Pixel</span></span> | <span data-ttu-id="403b9-143">Compute</span><span class="sxs-lookup"><span data-stu-id="403b9-143">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="403b9-144">X</span><span class="sxs-lookup"><span data-stu-id="403b9-144">X</span></span>      | <span data-ttu-id="403b9-145">X</span><span class="sxs-lookup"><span data-stu-id="403b9-145">X</span></span>    | <span data-ttu-id="403b9-146">X</span><span class="sxs-lookup"><span data-stu-id="403b9-146">X</span></span>      | <span data-ttu-id="403b9-147">X</span><span class="sxs-lookup"><span data-stu-id="403b9-147">X</span></span>        | <span data-ttu-id="403b9-148">X</span><span class="sxs-lookup"><span data-stu-id="403b9-148">X</span></span>     | <span data-ttu-id="403b9-149">X</span><span class="sxs-lookup"><span data-stu-id="403b9-149">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="403b9-150">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="403b9-150">Minimum Shader Model</span></span>

<span data-ttu-id="403b9-151">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="403b9-151">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="403b9-152">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="403b9-152">Shader Model</span></span>                                              | <span data-ttu-id="403b9-153">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="403b9-153">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="403b9-154">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="403b9-154">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="403b9-155">Oui</span><span class="sxs-lookup"><span data-stu-id="403b9-155">yes</span></span>       |
| [<span data-ttu-id="403b9-156">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="403b9-156">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="403b9-157">non</span><span class="sxs-lookup"><span data-stu-id="403b9-157">no</span></span>        |
| [<span data-ttu-id="403b9-158">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="403b9-158">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="403b9-159">non</span><span class="sxs-lookup"><span data-stu-id="403b9-159">no</span></span>        |
| [<span data-ttu-id="403b9-160">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="403b9-160">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="403b9-161">non</span><span class="sxs-lookup"><span data-stu-id="403b9-161">no</span></span>        |
| [<span data-ttu-id="403b9-162">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="403b9-162">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="403b9-163">non</span><span class="sxs-lookup"><span data-stu-id="403b9-163">no</span></span>        |
| [<span data-ttu-id="403b9-164">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="403b9-164">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="403b9-165">non</span><span class="sxs-lookup"><span data-stu-id="403b9-165">no</span></span>        |



 

<span data-ttu-id="403b9-166">CS \_ 4 \_ 0 et CS \_ 4 \_ 1 prennent en charge cette instruction pour UAV et SRV.</span><span class="sxs-lookup"><span data-stu-id="403b9-166">cs\_4\_0 and cs\_4\_1 support this instruction for UAV and SRV.</span></span>

## <a name="related-topics"></a><span data-ttu-id="403b9-167">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="403b9-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="403b9-168">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="403b9-168">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





