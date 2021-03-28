---
title: LD (SM4-ASM)
description: Extrait des données de la mémoire tampon ou de la texture spécifiée sans aucun filtrage (par exemple, échantillonnage par points) à l’aide de l’adresse entière fournie. Les données sources peuvent provenir de n’importe quel type de ressource, autre que TextureCube.
ms.assetid: DEE9A55F-EDFE-478E-8169-5BF9C43E98AF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaacc3d76d49cc2b3043d39036f0ff652d7b8794
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313684"
---
# <a name="ld-sm4---asm"></a><span data-ttu-id="e5f78-104">LD (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="e5f78-104">ld (sm4 - asm)</span></span>

<span data-ttu-id="e5f78-105">Extrait des données de la mémoire tampon ou de la texture spécifiée sans aucun filtrage (par exemple, échantillonnage par points) à l’aide de l’adresse entière fournie.</span><span class="sxs-lookup"><span data-stu-id="e5f78-105">Fetches data from the specified buffer or texture without any filtering (e.g. point sampling) using the provided integer address.</span></span> <span data-ttu-id="e5f78-106">Les données sources peuvent provenir de n’importe quel type de ressource, autre que TextureCube.</span><span class="sxs-lookup"><span data-stu-id="e5f78-106">The source data may come from any resource type, other than TextureCube.</span></span>



| <span data-ttu-id="e5f78-107">LD \[ \_ aoffimmi (u, v, w) \] dest \[ . Mask \] , srcAddress \[ . Swizzle \] , srcResource \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="e5f78-107">ld\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------------|



 



| <span data-ttu-id="e5f78-108">Élément</span><span class="sxs-lookup"><span data-stu-id="e5f78-108">Item</span></span>                                                                                                               | <span data-ttu-id="e5f78-109">Description</span><span class="sxs-lookup"><span data-stu-id="e5f78-109">Description</span></span>                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5f78-110"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="e5f78-110"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="e5f78-111">\[dans \] l’adresse du résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="e5f78-111">\[in\] The address of the result of the operation.</span></span><br/>                                                               |
| <span data-ttu-id="e5f78-112"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="e5f78-112"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="e5f78-113">\[dans \] les coordonnées de texture nécessaires à l’exécution de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="e5f78-113">\[in\] The texture coordinates needed to perform the sample.</span></span><br/>                                                     |
| <span data-ttu-id="e5f78-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="e5f78-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="e5f78-115">\[dans \] un registre de texture (t \# ) qui doit avoir été déclaré, identifiant la texture ou la mémoire tampon à partir de laquelle effectuer l’extraction.</span><span class="sxs-lookup"><span data-stu-id="e5f78-115">\[in\] A texture register (t\#) which must have been declared identifying which Texture or Buffer to fetch from.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e5f78-116">Notes</span><span class="sxs-lookup"><span data-stu-id="e5f78-116">Remarks</span></span>

<span data-ttu-id="e5f78-117">Cette instruction est une alternative simplifiée à l' [exemple](sample--sm4---asm-.md) d’instruction.</span><span class="sxs-lookup"><span data-stu-id="e5f78-117">This instruction is a simplified alternative to the [sample](sample--sm4---asm-.md) instruction.</span></span> <span data-ttu-id="e5f78-118">Contrairement à l' **exemple**, **LD** peut également extraire des données de tampons.</span><span class="sxs-lookup"><span data-stu-id="e5f78-118">Unlike **sample**, **ld** is also capable of fetching data from buffers.</span></span> <span data-ttu-id="e5f78-119">**LD** peut également extraire des ressources à plusieurs exemples (sur le nuanceur de pixels uniquement).</span><span class="sxs-lookup"><span data-stu-id="e5f78-119">**ld** is can also fetch from multi-sample resources (on pixel shader only).</span></span>

<span data-ttu-id="e5f78-120">*srcAddress* fournit l’ensemble des coordonnées de texture nécessaires pour exécuter l’exemple sous la forme d’entiers non signés.</span><span class="sxs-lookup"><span data-stu-id="e5f78-120">*srcAddress* provides the set of texture coordinates needed to perform the sample in the form of unsigned integers.</span></span> <span data-ttu-id="e5f78-121">Si *srcAddress* est en dehors de la plage \[ 0... ( \# texels dans la dimension-1) \] , le comportement hors limites est appelé, où **LD** retourne 0 dans tous les composants non manquants du format de *srcResource*, et la valeur par défaut pour les composants manquants.</span><span class="sxs-lookup"><span data-stu-id="e5f78-121">If *srcAddress* is out of the range\[0...(\#texels in dimension -1)\], then out-of-bounds behavior is invoked, where **ld** returns 0 in all non-missing components of the format of the *srcResource*, and the default for missing components.</span></span> <span data-ttu-id="e5f78-122">Une application qui souhaite obtenir un contrôle plus flexible sur le comportement de l’adresse hors limites doit utiliser l' **exemple** d’instruction à la place, car elle honore l’état de l’échantillonneur/de la mise en miroir/de la bordure/de la bordure.</span><span class="sxs-lookup"><span data-stu-id="e5f78-122">An application wishing any more flexible control over out-of-range address behavior should use the **sample** instruction instead, as it honors address wrap/mirror/clamp/border behavior defined as sampler state.</span></span>

<span data-ttu-id="e5f78-123">*srcAddress. a* (pos-Swizzle) fournit toujours un niveau de mipmap d’entier non signé.</span><span class="sxs-lookup"><span data-stu-id="e5f78-123">*srcAddress.a* (POS-swizzle) always provides an unsigned integer mipmap level.</span></span> <span data-ttu-id="e5f78-124">Si la valeur est en dehors de la plage \[ 0... ( num miplevels a dans la ressource-1) \] ), le comportement hors limites est appelé.</span><span class="sxs-lookup"><span data-stu-id="e5f78-124">If the value is out of the range \[0...(num miplevels in resource-1)\]), then out-of-bounds behavior is invoked.</span></span> <span data-ttu-id="e5f78-125">Si la ressource est une mémoire tampon, qui ne peut pas avoir de des mipmaps, *srcAddress. a* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="e5f78-125">If the resource is a buffer, which can not have any mipmaps, then *srcAddress.a* is ignored</span></span>

<span data-ttu-id="e5f78-126">*srcAddress. Go* (pos-Swizzle) est ignoré pour les mémoires tampons et les texture1D (non-tableau).</span><span class="sxs-lookup"><span data-stu-id="e5f78-126">*srcAddress.gb* (POS-swizzle) is ignored for buffers and texture1D (non-Array).</span></span> <span data-ttu-id="e5f78-127">*srcAddress. b* (pos-Swizzle) est ignoré pour les tableaux Texture1D et texture2Ds.</span><span class="sxs-lookup"><span data-stu-id="e5f78-127">*srcAddress.b* (POS-swizzle) is ignored for texture1D arrays and texture2Ds.</span></span>

<span data-ttu-id="e5f78-128">Pour les tableaux texture1D, *srcAddress. g* (pos-Swizzle) fournit l’index de tableau sous la forme d’un entier non signé.</span><span class="sxs-lookup"><span data-stu-id="e5f78-128">For texture1D arrays, *srcAddress.g* (POS-swizzle) provides the array index as an unsigned integer.</span></span> <span data-ttu-id="e5f78-129">Si la valeur est en dehors de la plage d’index de tableau disponibles \[ 0... ( Array size-1) \] , alors le comportement hors limites est appelé.</span><span class="sxs-lookup"><span data-stu-id="e5f78-129">If the value is out of the range of available array indices \[0...(array size-1)\], then out-of-bounds behavior is invoked.</span></span>

<span data-ttu-id="e5f78-130">Pour les tableaux texture2D, *srcAddress. b* (pos-Swizzle) fournit l’index de tableau, sinon avec la même sémantique que pour texture1D.</span><span class="sxs-lookup"><span data-stu-id="e5f78-130">For texture2D arrays, *srcAddress.b* (POS-swizzle) provides the array index, otherwise with same semantics as for texture1D.</span></span>

<span data-ttu-id="e5f78-131">L’extraction de *t \#* qui n’a rien lié à elle retourne 0 pour tous les composants.</span><span class="sxs-lookup"><span data-stu-id="e5f78-131">Fetching from *t\#* that has nothing bound to it returns 0 for all components.</span></span>

### <a name="address-offset"></a><span data-ttu-id="e5f78-132">Décalage d’adresse</span><span class="sxs-lookup"><span data-stu-id="e5f78-132">Address Offset</span></span>

<span data-ttu-id="e5f78-133">Le \[ \_ suffixe aoffimmi (u, v, w) facultatif \] (décalage d’adresse par entier immédiat) indique que les coordonnées de texture pour le **LD** doivent être décalées par un jeu d’espaces de texture d’entier d’espace de texture immédiate fournis.</span><span class="sxs-lookup"><span data-stu-id="e5f78-133">The optional \[\_aoffimmi(u,v,w)\] suffix (address offset by immediate integer) indicates that the texture coordinates for the **ld** are to be offset by a set of provided immediate texel space integer constant values.</span></span> <span data-ttu-id="e5f78-134">Les valeurs littérales sont un ensemble de numéros de compléments de 4 bits 2, dont la plage d’entiers est comprise entre \[ -8 et 7 \] .</span><span class="sxs-lookup"><span data-stu-id="e5f78-134">The literal values are a set of 4 bit 2's complement numbers, having integer range \[-8,7\].</span></span> <span data-ttu-id="e5f78-135">Ce modificateur est défini uniquement pour texture1D/2D/3D, y compris les tableaux, et non pour les mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="e5f78-135">This modifier is defined only for texture1D/2D/3D, including arrays, and not for buffers.</span></span>

<span data-ttu-id="e5f78-136">Les décalages sont ajoutés aux coordonnées de texture, dans l’espace de Texel, par rapport au miplevel auquel le **LD** accède.</span><span class="sxs-lookup"><span data-stu-id="e5f78-136">The offsets are added to the texture coordinates, in texel space, relative to the miplevel being accessed by the **ld**.</span></span>

<span data-ttu-id="e5f78-137">Les décalages d’adresse ne sont pas appliqués le long de l’axe de tableau des tableaux texture1D/2D.</span><span class="sxs-lookup"><span data-stu-id="e5f78-137">Address offsets are not applied along the array axis of texture1D/2D arrays.</span></span>

<span data-ttu-id="e5f78-138">Les composants *\_ aoffimmi v, w* sont ignorés pour texture1Ds.</span><span class="sxs-lookup"><span data-stu-id="e5f78-138">The *\_aoffimmi v,w* components are ignored for texture1Ds.</span></span>

<span data-ttu-id="e5f78-139">Le composant *\_ aoffimmi w* est ignoré pour texture2Ds.</span><span class="sxs-lookup"><span data-stu-id="e5f78-139">The *\_aoffimmi w* component is ignored for texture2Ds.</span></span>

<span data-ttu-id="e5f78-140">Étant donné que les coordonnées de texture pour **LD** sont des entiers non signés, si le décalage entraîne la sortie de l’adresse sous zéro, elle est renvoyée à une adresse de grande taille et entraîne un accès hors limites.</span><span class="sxs-lookup"><span data-stu-id="e5f78-140">Because the texture coordinates for **ld** are unsigned integers, if the offset causes the address to go below zero, it will wrap to a large address, and result in an out of bounds access.</span></span>

### <a name="return-type-control"></a><span data-ttu-id="e5f78-141">Contrôle de type de retour</span><span class="sxs-lookup"><span data-stu-id="e5f78-141">Return Type Control</span></span>

<span data-ttu-id="e5f78-142">Le format de données renvoyé par **LD** au registre de destination est déterminé de la même façon que pour l' **exemple** d’instruction. elle est basée sur le format lié au paramètre *srcResource* (*t \#*).</span><span class="sxs-lookup"><span data-stu-id="e5f78-142">The data format returned by **ld** to the destination register is determined in the same way as described for the **sample** instruction; it is based on the format bound to the *srcResource* parameter (*t\#*).</span></span>

<span data-ttu-id="e5f78-143">Comme avec l' **exemple** d’instruction, les valeurs retournées pour **LD** sont 4-vectors avec des valeurs par défaut spécifiques au format pour les composants qui ne sont pas présents dans le format.</span><span class="sxs-lookup"><span data-stu-id="e5f78-143">As with the **sample** instruction, returned values for **ld** are 4-vectors with format-specific defaults for components not present in the format.</span></span> <span data-ttu-id="e5f78-144">Swizzle sur *srcResource* détermine comment Swizzle le résultat à 4 composants à partir de la charge de texture, après quoi. Mask sur *dest* détermine les composants de *dest* qui sont mis à jour.</span><span class="sxs-lookup"><span data-stu-id="e5f78-144">The swizzle on *srcResource* determines how to swizzle the 4-component result coming back from the texture load, after which .mask on *dest* determines which components in *dest* get updated.</span></span>

<span data-ttu-id="e5f78-145">Quand une valeur float 32 bits est lue par *LD* dans un registre 32 bits, les bits ne sont pas touchés ; autrement dit, les valeurs dénormales restent dénormalisées.</span><span class="sxs-lookup"><span data-stu-id="e5f78-145">When a 32-bit float value is read by *ld* into a 32-bit register, the bits are untouched; that is, denormal values remain denormal.</span></span> <span data-ttu-id="e5f78-146">Contrairement à l' **exemple** d’instruction.</span><span class="sxs-lookup"><span data-stu-id="e5f78-146">This is unlike the **sample** instruction.</span></span>

### <a name="miscellaneous-details"></a><span data-ttu-id="e5f78-147">Détails divers</span><span class="sxs-lookup"><span data-stu-id="e5f78-147">Miscellaneous Details</span></span>

<span data-ttu-id="e5f78-148">Comme aucun filtrage n’est associé à l’instruction **LD** , les concepts tels que LOD Bias ne s’appliquent pas à **LD**.</span><span class="sxs-lookup"><span data-stu-id="e5f78-148">As there is no filtering associated with the **ld** instruction, concepts like LOD bias do not apply to **ld**.</span></span> <span data-ttu-id="e5f78-149">En conséquence, il n’y *a \# aucun paramètre de* l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="e5f78-149">Accordingly there is no sampler *s\#* parameter.</span></span>

### <a name="restrictions"></a><span data-ttu-id="e5f78-150">Restrictions</span><span class="sxs-lookup"><span data-stu-id="e5f78-150">Restrictions</span></span>

-   <span data-ttu-id="e5f78-151">*srcResource* doit être un \# Registre t et non un TextureCube.</span><span class="sxs-lookup"><span data-stu-id="e5f78-151">*srcResource* must be a t\# register, and not a TextureCube.</span></span> <span data-ttu-id="e5f78-152">*srcResource* ne peut pas être un constantbuffer, qui ne peut pas être lié à des \# registres t.</span><span class="sxs-lookup"><span data-stu-id="e5f78-152">*srcResource* cannot be a constantbuffer either, which cannot be bound to t\# registers.</span></span>
-   <span data-ttu-id="e5f78-153">L’adressage relatif sur *srcResource* n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="e5f78-153">Relative addressing on *srcResource* is not permitted.</span></span>
-   <span data-ttu-id="e5f78-154">*srcAddress* doit être un registre Temp (r \# /x \# ), constant (CB \# ) ou Input (v \# ).</span><span class="sxs-lookup"><span data-stu-id="e5f78-154">*srcAddress* must be a temp (r\#/x\#), constant (cb\#) or input (v\#) register.</span></span>
-   <span data-ttu-id="e5f78-155">*dest* doit être un registre Temp (r \# /x \# ) ou Output (o \* \# ).</span><span class="sxs-lookup"><span data-stu-id="e5f78-155">*dest* must be a temp (r\#/x\#) or output (o\*\#) register.</span></span>

<span data-ttu-id="e5f78-156">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="e5f78-156">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e5f78-157">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="e5f78-157">Vertex Shader</span></span> | <span data-ttu-id="e5f78-158">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="e5f78-158">Geometry Shader</span></span> | <span data-ttu-id="e5f78-159">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="e5f78-159">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="e5f78-160">x</span><span class="sxs-lookup"><span data-stu-id="e5f78-160">x</span></span>             | <span data-ttu-id="e5f78-161">x</span><span class="sxs-lookup"><span data-stu-id="e5f78-161">x</span></span>               | <span data-ttu-id="e5f78-162">x</span><span class="sxs-lookup"><span data-stu-id="e5f78-162">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e5f78-163">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="e5f78-163">Minimum Shader Model</span></span>

<span data-ttu-id="e5f78-164">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="e5f78-164">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e5f78-165">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="e5f78-165">Shader Model</span></span>                                              | <span data-ttu-id="e5f78-166">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="e5f78-166">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e5f78-167">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="e5f78-167">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e5f78-168">Oui</span><span class="sxs-lookup"><span data-stu-id="e5f78-168">yes</span></span>       |
| [<span data-ttu-id="e5f78-169">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="e5f78-169">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e5f78-170">Oui</span><span class="sxs-lookup"><span data-stu-id="e5f78-170">yes</span></span>       |
| [<span data-ttu-id="e5f78-171">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="e5f78-171">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e5f78-172">Oui</span><span class="sxs-lookup"><span data-stu-id="e5f78-172">yes</span></span>       |
| [<span data-ttu-id="e5f78-173">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e5f78-173">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e5f78-174">non</span><span class="sxs-lookup"><span data-stu-id="e5f78-174">no</span></span>        |
| [<span data-ttu-id="e5f78-175">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e5f78-175">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e5f78-176">non</span><span class="sxs-lookup"><span data-stu-id="e5f78-176">no</span></span>        |
| [<span data-ttu-id="e5f78-177">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e5f78-177">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e5f78-178">non</span><span class="sxs-lookup"><span data-stu-id="e5f78-178">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e5f78-179">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e5f78-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5f78-180">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e5f78-180">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





