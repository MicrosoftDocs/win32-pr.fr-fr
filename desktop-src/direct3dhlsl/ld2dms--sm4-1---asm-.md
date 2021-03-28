---
title: ld2dms (SM 4.1-ASM)
description: Lit des échantillons individuels à partir de textures à échantillons multiples à deux dimensions.
ms.assetid: 8D92BFA8-4B22-46F3-876D-8D84BB3A96E7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e9dd03b7c07f3fb25294dd0ad6aa382eb203560
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104101089"
---
# <a name="ld2dms-sm41---asm"></a><span data-ttu-id="07328-103">ld2dms (SM 4.1-ASM)</span><span class="sxs-lookup"><span data-stu-id="07328-103">ld2dms (sm4.1 - asm)</span></span>

<span data-ttu-id="07328-104">Lit des échantillons individuels à partir de textures à échantillons multiples à deux dimensions.</span><span class="sxs-lookup"><span data-stu-id="07328-104">Reads individual samples out of 2-dimensional multi-sample textures.</span></span>



| <span data-ttu-id="07328-105">ld2dms \[ \_ aoffimmi (u, v) \] dest \[ . Mask \] , srcAddress \[ . Swizzle \] , srcResource \[ . Swizzle \] , sampleIndex (opérande scalaire)</span><span class="sxs-lookup"><span data-stu-id="07328-105">ld2dms\[\_aoffimmi(u,v)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], sampleIndex (scalar operand)</span></span> |
|------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="07328-106">Élément</span><span class="sxs-lookup"><span data-stu-id="07328-106">Item</span></span>                                                                                                               | <span data-ttu-id="07328-107">Description</span><span class="sxs-lookup"><span data-stu-id="07328-107">Description</span></span>                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07328-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="07328-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="07328-109">\[dans \] l’adresse du résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="07328-109">\[in\] The address of result of the operation.</span></span> <br/>                                                                 |
| <span data-ttu-id="07328-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="07328-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="07328-111">\[dans \] les coordonnées de texture nécessaires à l’exécution de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="07328-111">\[in\] The texture coordinates needed to perform the sample.</span></span><br/>                                                    |
| <span data-ttu-id="07328-112"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="07328-112"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="07328-113">\[dans \] un registre de texture (t \# ) qui doit avoir été déclaré, identifiant la texture ou la mémoire tampon à partir de laquelle effectuer l’extraction</span><span class="sxs-lookup"><span data-stu-id="07328-113">\[in\] A texture register (t\#) which must have been declared identifying which Texture or Buffer to fetch from</span></span><br/> |
| <span data-ttu-id="07328-114"><span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*sampleIndex*</span><span class="sxs-lookup"><span data-stu-id="07328-114"><span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*sampleIndex*</span></span><br/> | <span data-ttu-id="07328-115">\[dans \] Idendifies les exemples à lire à partir de *srcResource*.</span><span class="sxs-lookup"><span data-stu-id="07328-115">\[in\] Idendifies the samples to read from *srcResource*.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="07328-116">Notes</span><span class="sxs-lookup"><span data-stu-id="07328-116">Remarks</span></span>

<span data-ttu-id="07328-117">Cette instruction est une alternative simplifiée à l' [exemple](sample--sm4---asm-.md) d’instruction.</span><span class="sxs-lookup"><span data-stu-id="07328-117">This instruction is a simplified alternative to the [sample](sample--sm4---asm-.md) instruction.</span></span> <span data-ttu-id="07328-118">Il extrait les données de la texture spécifiée sans aucun filtrage (par exemple, échantillonnage par points) à l’aide de l’entier fourni *srcAddress* et *sampleIndex*.</span><span class="sxs-lookup"><span data-stu-id="07328-118">It fetches data from the specified Texture without any filtering (e.g. point sampling) using the provided integer *srcAddress* and *sampleIndex*.</span></span>

<span data-ttu-id="07328-119">*srcAddress* fournit l’ensemble des coordonnées de texture nécessaires pour exécuter l’exemple sous la forme d’entiers non signés.</span><span class="sxs-lookup"><span data-stu-id="07328-119">*srcAddress* provides the set of texture coordinates needed to perform the sample in the form of unsigned integers.</span></span> <span data-ttu-id="07328-120">Si *srcAddress* est en dehors de la plage \[ 0... ( \# texels dans la dimension-1) \] , **ld2dms** retourne toujours 0 dans tous les composants présents dans le format de la ressource, et les valeurs par défaut (0, 0, 0, 1,0 f/0x00000001) pour les composants manquants.</span><span class="sxs-lookup"><span data-stu-id="07328-120">If *srcAddress* is out of the range\[0...(\#texels in dimension -1)\], **ld2dms** always returns 0 in all components present in the format of the resource, and defaults (0,0,0,1.0f/0x00000001) for missing components.</span></span>

<span data-ttu-id="07328-121">*sampleIndex* ne doit pas nécessairement être un littéral.</span><span class="sxs-lookup"><span data-stu-id="07328-121">*sampleIndex* does not have to be a literal.</span></span> <span data-ttu-id="07328-122">Il n’est pas nécessaire de spécifier le nombre d’échantillons multiples sur la ressource de texture et il fonctionne avec des affichages de profondeur ou de stencil.</span><span class="sxs-lookup"><span data-stu-id="07328-122">The multi-sample count does not have to be specified on the texture resource, and it works with depth or stencil views.</span></span>

<span data-ttu-id="07328-123">Une application qui souhaite obtenir un contrôle plus flexible sur le comportement de l’adresse hors limites doit utiliser l' **exemple** d’instruction à la place, car elle honore l’état de l’échantillonneur/de la mise en miroir/de la bordure/de la bordure.</span><span class="sxs-lookup"><span data-stu-id="07328-123">An application wishing any more flexible control over out-of-range address behavior should use the **sample** instruction instead, as it honors address wrap/mirror/clamp/border behavior defined as sampler state.</span></span>

<span data-ttu-id="07328-124">*srcAddress. b* (Swizzle) est ignoré pour Texture2Ds.</span><span class="sxs-lookup"><span data-stu-id="07328-124">*srcAddress.b* (post-swizzle) is ignored for Texture2Ds.</span></span> <span data-ttu-id="07328-125">Si la valeur est en dehors de la plage d’index de tableau disponibles \[ 0... ( Array size-1) \] , puis **ld2dms** retourne toujours 0 dans tous les composants présents dans le format de la ressource, et les valeurs par défaut (0, 0, 0, 1.0 f/0x00000001) pour les composants manquants.</span><span class="sxs-lookup"><span data-stu-id="07328-125">If the value is out of the range of available array indices \[0...(array size-1)\], then **ld2dms** always returns 0 in all components present in the format of the resource, and defaults (0,0,0,1.0f/0x00000001) for missing components.</span></span>

<span data-ttu-id="07328-126">Pour les tableaux Texture2D, *srcAddress. b* (après Swizzle) fournit l’index de tableau.</span><span class="sxs-lookup"><span data-stu-id="07328-126">For Texture2D Arrays, *srcAddress.b* (post-swizzle) provides the array index.</span></span> <span data-ttu-id="07328-127">Oherwise a le même comportement que Texture2D.</span><span class="sxs-lookup"><span data-stu-id="07328-127">Oherwise it has the same behavior as Texture2D.</span></span>

<span data-ttu-id="07328-128">*srcAddress. a* (Swizzle) est toujours ignoré.</span><span class="sxs-lookup"><span data-stu-id="07328-128">*srcAddress.a* (post-swizzle) is always ignored.</span></span> <span data-ttu-id="07328-129">Le compilateur HLSL ne sortira jamais quoi que ce soit.</span><span class="sxs-lookup"><span data-stu-id="07328-129">The HLSL compiler will never output anything there.</span></span>

<span data-ttu-id="07328-130">*srcResource* est un registre de texture (t \# ) qui doit avoir été déclaré (22.3.11), identifiant la texture à partir de laquelle effectuer l’extraction.</span><span class="sxs-lookup"><span data-stu-id="07328-130">*srcResource* is a texture register (t\#) which must have been declared(22.3.11), identifying which Texture to fetch from.</span></span>

<span data-ttu-id="07328-131">L’extraction de t \# qui n’a rien lié à elle retourne 0 pour tous les composants.</span><span class="sxs-lookup"><span data-stu-id="07328-131">Fetching from t\# that has nothing bound to it returns 0 for all components.</span></span>

### <a name="address-offset"></a><span data-ttu-id="07328-132">Décalage d’adresse</span><span class="sxs-lookup"><span data-stu-id="07328-132">Address Offset</span></span>

<span data-ttu-id="07328-133">Le \[ \_ suffixe aoffimmi (u, v, w) facultatif \] (décalage d’adresse par entier immédiat) indique que les coordonnées de texture du **ld2dms** doivent être décalées par un ensemble d’espaces de constantes d’espace de Texel immédiat fournis.</span><span class="sxs-lookup"><span data-stu-id="07328-133">The optional \[\_aoffimmi(u,v,w)\] suffix (address offset by immediate integer) indicates that the texture coordinates for the **ld2dms** are to be offset by a set of provided immediate texel space integer constant values.</span></span> <span data-ttu-id="07328-134">Les valeurs littérales sont un ensemble de numéros de compléments de 4 bits 2, dont la plage d’entiers est comprise entre \[ -8 et 7 \] .</span><span class="sxs-lookup"><span data-stu-id="07328-134">The literal values are a set of 4 bit 2's complement numbers, having integer range \[-8,7\].</span></span>

<span data-ttu-id="07328-135">Les décalages sont ajoutés aux coordonnées de texture, dans l’espace Texel.</span><span class="sxs-lookup"><span data-stu-id="07328-135">The offsets are added to the texture coordinates, in texel space.</span></span>

<span data-ttu-id="07328-136">Les décalages d’adresse ne sont pas appliqués le long de l’axe de tableau des tableaux Texture1D/2D.</span><span class="sxs-lookup"><span data-stu-id="07328-136">Address offsets are not applied along the array axis of Texture1D/2D Arrays.</span></span>

<span data-ttu-id="07328-137">Les composants *\_ aoffimmi v, w* sont ignorés pour Texture1Ds.</span><span class="sxs-lookup"><span data-stu-id="07328-137">The *\_aoffimmi v,w* components are ignored for Texture1Ds.</span></span>

<span data-ttu-id="07328-138">Le composant *\_ aoffimmi w* est ignoré pour Texture2Ds.</span><span class="sxs-lookup"><span data-stu-id="07328-138">The *\_aoffimmi w* component is ignored for Texture2Ds.</span></span>

<span data-ttu-id="07328-139">Étant donné que les coordonnées de texture pour les **ld2dms** sont des entiers non signés, si le décalage entraîne l’accès à l’adresse sous zéro, elle est renvoyée à une adresse de grande taille et entraîne un accès en dehors des limites, ce qui correspond à la valeur **LD** retourne 0 dans tous les composants présents dans le format de la ressource, et les valeurs par défaut (0, 0,</span><span class="sxs-lookup"><span data-stu-id="07328-139">Because the texture coordinates for **ld2dms** are unsigned integers, if the offset causes the address to go below zero, it will wrap to a large address, and result in an out of bounds access, which like **ld** returns 0 in all components present in the format of the resource, and the defaults (0,0,0,1.0f/0x00000001) for missing components.</span></span>

### <a name="sample-number"></a><span data-ttu-id="07328-140">Nombre d’échantillons</span><span class="sxs-lookup"><span data-stu-id="07328-140">Sample Number</span></span>

<span data-ttu-id="07328-141">**ld2dms** peut être utilisé sur n’importe quelle ressource.</span><span class="sxs-lookup"><span data-stu-id="07328-141">**ld2dms** is available for use on any resource.</span></span> <span data-ttu-id="07328-142">**ld2dms** fonctionne de la même façon que **LD** , sauf sur les ressources multsample 2D, en utilisant l’opérande *sampleIndex* supplémentaire (de base 0) pour identifier l’échantillon à lire à partir de la ressource.</span><span class="sxs-lookup"><span data-stu-id="07328-142">**ld2dms** operates identically to **ld** except on 2D multsample resources, by using the additional (0-based) *sampleIndex* operand to identify which sample to read from the resource.</span></span>

<span data-ttu-id="07328-143">Le résultat de la spécification d’un *sampleIndex* qui dépasse le nombre d’exemples dans la ressource n’est pas défini, mais ne peut pas retourner de données en dehors de l’espace d’adressage du contexte de périphérique.</span><span class="sxs-lookup"><span data-stu-id="07328-143">The result of specifying a *sampleIndex* that exceeds the number of samples in the resource is undefined, but cannot return data outside of the address space of the device context.</span></span>

### <a name="return-type-control"></a><span data-ttu-id="07328-144">Contrôle de type de retour</span><span class="sxs-lookup"><span data-stu-id="07328-144">Return Type Control</span></span>

<span data-ttu-id="07328-145">Le format de données retourné par **ld2dms** au registre de destination est déterminé de la même façon que pour l' **exemple** d’instruction.</span><span class="sxs-lookup"><span data-stu-id="07328-145">The data format returned by **ld2dms** to the destination register is determined in the same way as described for the **sample** instruction.</span></span> <span data-ttu-id="07328-146">Elle est basée sur le format lié au paramètre *srcResource* (t \# ).</span><span class="sxs-lookup"><span data-stu-id="07328-146">It is based on the format bound to the *srcResource* parameter (t\#).</span></span>

<span data-ttu-id="07328-147">Comme avec l' **exemple** d’instruction, les valeurs retournées pour **ld2dms** sont 4-vectors avec des valeurs par défaut spécifiques au format pour les composants qui ne sont pas présents dans le format.</span><span class="sxs-lookup"><span data-stu-id="07328-147">As with the **sample** instruction, returned values for **ld2dms** are 4-vectors with format-specific defaults for components not present in the format.</span></span> <span data-ttu-id="07328-148">Swizzle sur *srcResource* détermine comment Swizzle le résultat à 4 composants à partir de la charge de texture, après quoi. Mask sur *dest* détermine les composants de *dest* qui sont mis à jour.</span><span class="sxs-lookup"><span data-stu-id="07328-148">The swizzle on *srcResource* determines how to swizzle the 4-component result coming back from the texture load, after which .mask on *dest* determines which components in *dest* get updated.</span></span>

<span data-ttu-id="07328-149">Quand une valeur float 32 bits est lue par **ld2dms** dans un registre 32 bits, les bits ne sont pas touchés ; autrement dit, les valeurs dénormales restent dénormalisées.</span><span class="sxs-lookup"><span data-stu-id="07328-149">When a 32-bit float value is read by **ld2dms** into a 32-bit register, the bits are untouched; that is, denormal values remain denormal.</span></span> <span data-ttu-id="07328-150">Contrairement à l' **exemple** d’instruction.</span><span class="sxs-lookup"><span data-stu-id="07328-150">This is unlike the **sample** instruction.</span></span>

### <a name="miscellaneous-details"></a><span data-ttu-id="07328-151">Détails divers</span><span class="sxs-lookup"><span data-stu-id="07328-151">Miscellaneous Details</span></span>

<span data-ttu-id="07328-152">Comme aucun filtrage n’est associé à cette instruction, les concepts tels que LOD Bias ne s’appliquent pas.</span><span class="sxs-lookup"><span data-stu-id="07328-152">As there is no filtering associated with this instruction, concepts like LOD bias do not apply.</span></span> <span data-ttu-id="07328-153">En conséquence, il n’y a aucun paramètre de l' *échantillonneur \#* .</span><span class="sxs-lookup"><span data-stu-id="07328-153">Accordingly there is no *sampler s\#* parameter.</span></span>

### <a name="restrictions"></a><span data-ttu-id="07328-154">Restrictions</span><span class="sxs-lookup"><span data-stu-id="07328-154">Restrictions</span></span>

-   <span data-ttu-id="07328-155">*srcResource* doit être un \# Registre t, et non un TextureCube, Texture1D ou Texture1DArray.</span><span class="sxs-lookup"><span data-stu-id="07328-155">*srcResource* must be a t\# register, and not a TextureCube, Texture1D or Texture1DArray.</span></span> <span data-ttu-id="07328-156">*srcResource* ne peut pas être un ConstantBuffer, qui ne peut pas être lié à des \# registres t.</span><span class="sxs-lookup"><span data-stu-id="07328-156">*srcResource* cannot be a ConstantBuffer, which cannot be bound to t\# registers.</span></span>
-   <span data-ttu-id="07328-157">L’adressage relatif sur *srcResource* n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="07328-157">Relative addressing on *srcResource* is not permitted.</span></span>
-   <span data-ttu-id="07328-158">*srcAddress* et *sampleIndex* doivent être un registre Temp (r \# /x \# ), constant (CB \# ) ou Input (v \# ).</span><span class="sxs-lookup"><span data-stu-id="07328-158">*srcAddress* and *sampleIndex* must be a temp (r\#/x\#), constant (cb\#) or input (v\#) register.</span></span>
-   <span data-ttu-id="07328-159">*dest* doit être un registre Temp (r \# /x \# ) ou Output (o \* \# ).</span><span class="sxs-lookup"><span data-stu-id="07328-159">*dest* must be a temp (r\#/x\#) or output (o\*\#) register.</span></span>

<span data-ttu-id="07328-160">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="07328-160">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="07328-161">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="07328-161">Vertex Shader</span></span> | <span data-ttu-id="07328-162">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="07328-162">Geometry Shader</span></span> | <span data-ttu-id="07328-163">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="07328-163">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="07328-164">x</span><span class="sxs-lookup"><span data-stu-id="07328-164">x</span></span>             | <span data-ttu-id="07328-165">x</span><span class="sxs-lookup"><span data-stu-id="07328-165">x</span></span>               | <span data-ttu-id="07328-166">x</span><span class="sxs-lookup"><span data-stu-id="07328-166">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="07328-167">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="07328-167">Minimum Shader Model</span></span>

<span data-ttu-id="07328-168">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="07328-168">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="07328-169">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="07328-169">Shader Model</span></span>                                              | <span data-ttu-id="07328-170">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="07328-170">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="07328-171">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="07328-171">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="07328-172">Oui</span><span class="sxs-lookup"><span data-stu-id="07328-172">yes</span></span>       |
| [<span data-ttu-id="07328-173">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="07328-173">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="07328-174">Oui</span><span class="sxs-lookup"><span data-stu-id="07328-174">yes</span></span>       |
| [<span data-ttu-id="07328-175">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="07328-175">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="07328-176">non</span><span class="sxs-lookup"><span data-stu-id="07328-176">no</span></span>        |
| [<span data-ttu-id="07328-177">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="07328-177">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="07328-178">non</span><span class="sxs-lookup"><span data-stu-id="07328-178">no</span></span>        |
| [<span data-ttu-id="07328-179">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="07328-179">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="07328-180">non</span><span class="sxs-lookup"><span data-stu-id="07328-180">no</span></span>        |
| [<span data-ttu-id="07328-181">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="07328-181">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="07328-182">non</span><span class="sxs-lookup"><span data-stu-id="07328-182">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="07328-183">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="07328-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07328-184">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="07328-184">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





