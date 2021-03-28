---
title: exemple (SM4-ASM)
description: Échantillonne des données à partir de l’élément/texture spécifié à l’aide de l’adresse spécifiée et du mode de filtrage identifié par l’échantillonneur donné. | exemple (SM4-ASM)
ms.assetid: 9055D3EE-FD4A-418C-A743-D12E8BDF69FF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 397aba4a165f13721e73f87da82cff3e8918e33b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103953689"
---
# <a name="sample-sm4---asm"></a><span data-ttu-id="433a8-104">exemple (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="433a8-104">sample (sm4 - asm)</span></span>

<span data-ttu-id="433a8-105">Échantillonne des données à partir de l’élément/texture spécifié à l’aide de l’adresse spécifiée et du mode de filtrage identifié par l’échantillonneur donné.</span><span class="sxs-lookup"><span data-stu-id="433a8-105">Samples data from the specified Element/texture using the specified address and the filtering mode identified by the given sampler.</span></span>



| <span data-ttu-id="433a8-106">exemple \[ \_ aoffimmi (u, v, w) \] dest \[ . Mask \] , srcAddress \[ . Swizzle \] , srcResource \[ . Swizzle \] , srcSampler</span><span class="sxs-lookup"><span data-stu-id="433a8-106">sample\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler</span></span> |
|--------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="433a8-107">Élément</span><span class="sxs-lookup"><span data-stu-id="433a8-107">Item</span></span>                                                                                                               | <span data-ttu-id="433a8-108">Description</span><span class="sxs-lookup"><span data-stu-id="433a8-108">Description</span></span>                                                                                        |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="433a8-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="433a8-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="433a8-110">\[dans \] l’adresse du résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="433a8-110">\[in\] The address of the result of the operation.</span></span><br/>                                      |
| <span data-ttu-id="433a8-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="433a8-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="433a8-112">\[dans \] un ensemble de coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="433a8-112">\[in\] A set of texture coordinates.</span></span> <span data-ttu-id="433a8-113">Pour plus d’informations, consultez la section **Notes** .</span><span class="sxs-lookup"><span data-stu-id="433a8-113">For more information, see the **Remarks** section.</span></span><br/> |
| <span data-ttu-id="433a8-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="433a8-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="433a8-115">\[dans \] un registre de texture.</span><span class="sxs-lookup"><span data-stu-id="433a8-115">\[in\] A texture register.</span></span> <span data-ttu-id="433a8-116">Pour plus d’informations, consultez la section **Notes** .</span><span class="sxs-lookup"><span data-stu-id="433a8-116">For more information, see the **Remarks** section.</span></span><br/>           |
| <span data-ttu-id="433a8-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="433a8-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="433a8-118">\[dans \] un registre d’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="433a8-118">\[in\] A sampler register.</span></span> <span data-ttu-id="433a8-119">Pour plus d’informations, consultez la section **Notes** .</span><span class="sxs-lookup"><span data-stu-id="433a8-119">For more information, see the **Remarks** section.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="433a8-120">Notes</span><span class="sxs-lookup"><span data-stu-id="433a8-120">Remarks</span></span>

<span data-ttu-id="433a8-121">Les données sources peuvent provenir de n’importe quel type de ressource, autre que des mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="433a8-121">The source data may come from any Resource Type, other than Buffers.</span></span>

<span data-ttu-id="433a8-122">*srcAddress* fournit l’ensemble des coordonnées de texture nécessaires pour exécuter l’exemple, sous la forme de valeurs à virgule flottante référençant l’espace normalisé dans la texture.</span><span class="sxs-lookup"><span data-stu-id="433a8-122">*srcAddress* provides the set of texture coordinates needed to perform the sample, as floating point values referencing normalized space in the texture.</span></span> <span data-ttu-id="433a8-123">Les modes de renvoi à la ligne de l’adresse (Wrap/Mirror/collier/bordure, etc.) sont appliqués pour les coordonnées de texture en dehors de \[ 0... 1 \] plage, tirées de l’état de l’échantillonneur (s \# ) et appliquées après l’application d’un décalage d’adresse à des coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="433a8-123">Address wrapping modes (wrap/mirror/clamp/border etc.) are applied for texture coordinates outside \[0...1\] range, taken from the sampler state (s\#), and applied after any address offset is applied to texture coordinates.</span></span>

<span data-ttu-id="433a8-124">*srcResource* est un registre de texture (t \# ).</span><span class="sxs-lookup"><span data-stu-id="433a8-124">*srcResource* is a texture register (t\#).</span></span> <span data-ttu-id="433a8-125">Il s’agit simplement d’un espace réservé pour une texture, y compris le type de données de retour de la ressource échantillonnée.</span><span class="sxs-lookup"><span data-stu-id="433a8-125">This is simply a placeholder for a texture, including the return data type of the resource being sampled.</span></span> <span data-ttu-id="433a8-126">Toutes ces informations sont déclarées dans le préambule du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="433a8-126">All of this information is declared in the Shader preamble.</span></span> <span data-ttu-id="433a8-127">La ressource réelle à échantillonner est liée au nuanceur en externe à l’emplacement \# (pour t \# ).</span><span class="sxs-lookup"><span data-stu-id="433a8-127">The actual resource to be sampled is bound to the Shader externally at slot \# (for t\#).</span></span>

<span data-ttu-id="433a8-128">*srcSampler* est un ou plusieurs registres d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="433a8-128">*srcSampler* is a sampler register (s).</span></span> <span data-ttu-id="433a8-129">Il s’agit simplement d’un espace réservé pour une collection de contrôles de filtrage tels que point et Linear, mappage MIP et les contrôles d’habillage d’adresse.</span><span class="sxs-lookup"><span data-stu-id="433a8-129">This is simply a placeholder for a collection of filtering controls such as point vs. linear, mipmapping and address wrapping controls.</span></span>

<span data-ttu-id="433a8-130">L’ensemble d’informations nécessaires au matériel pour effectuer l’échantillonnage est divisé en deux parties orthogonales.</span><span class="sxs-lookup"><span data-stu-id="433a8-130">The set of information required for the hardware to perform sampling is split into two orthogonal pieces.</span></span> <span data-ttu-id="433a8-131">Tout d’abord, le registre de texture fournit des informations sur le type de données sources, notamment des informations indiquant si la texture contient des données sRVB.</span><span class="sxs-lookup"><span data-stu-id="433a8-131">First, the texture register provides source data type information including, for example, information about whether the texture contains SRGB data.</span></span> <span data-ttu-id="433a8-132">Elle fait également référence à la mémoire réelle échantillonnée.</span><span class="sxs-lookup"><span data-stu-id="433a8-132">It also references the actual memory being sampled.</span></span> <span data-ttu-id="433a8-133">Deuxièmement, le registre de l’échantillonneur définit le mode de filtrage à appliquer.</span><span class="sxs-lookup"><span data-stu-id="433a8-133">Second, the sampler register defines the filtering mode to apply.</span></span>

### <a name="array-resources"></a><span data-ttu-id="433a8-134">Ressources de groupe</span><span class="sxs-lookup"><span data-stu-id="433a8-134">Array Resources</span></span>

<span data-ttu-id="433a8-135">Pour les tableaux Texture1D, le composant *srcAddress* g (pos-Swizzle) sélectionne la tranche de tableau à partir de laquelle effectuer l’extraction.</span><span class="sxs-lookup"><span data-stu-id="433a8-135">For Texture1D Arrays, the *srcAddress* g component (POS-swizzle) selects which Array Slice to fetch from.</span></span> <span data-ttu-id="433a8-136">Elle est toujours traitée comme une valeur float mise à l’échelle, plutôt que l’espace normalisé pour les coordonnées de texture standard, et un arrondi vers le plus proche est appliqué à la valeur, suivi d’une bride à la plage BufferArray disponible.</span><span class="sxs-lookup"><span data-stu-id="433a8-136">This is always treated as a scaled float value, rather than the normalized space for standard texture coordinates, and a round-to-nearest even is applied on the value, followed by a clamp to the available BufferArray range.</span></span>

<span data-ttu-id="433a8-137">Pour les tableaux Texture2D, le composant *srcAddress* b (pos-Swizzle) sélectionne la tranche de tableau à partir de laquelle effectuer l’extraction, sinon en utilisant la même sémantique que celle décrite pour les groupes Texture1D.</span><span class="sxs-lookup"><span data-stu-id="433a8-137">For Texture2D Arrays, the *srcAddress* b component (POS-swizzle) selects which Array Slice to fetch from, otherwise using the same semantics described for Texture1D Arrays .</span></span>

### <a name="address-offset"></a><span data-ttu-id="433a8-138">Décalage d’adresse</span><span class="sxs-lookup"><span data-stu-id="433a8-138">Address Offset</span></span>

<span data-ttu-id="433a8-139">Le \[ \_ suffixe aoffimmi (u, v, w) facultatif \] (décalage d’adresse par entier immédiat) indique que les coordonnées de la texture de l’échantillon doivent être décalées par un jeu d’espaces de texture de l’espace de Texel immédiat fournis.</span><span class="sxs-lookup"><span data-stu-id="433a8-139">The optional \[\_aoffimmi(u,v,w)\] suffix (address offset by immediate integer) indicates that the texture coordinates for the sample are to be offset by a set of provided immediate texel space integer constant values.</span></span> <span data-ttu-id="433a8-140">Les valeurs littérales sont un ensemble de numéros de compléments de 4 bits 2, dont la plage d’entiers est comprise entre \[ -8 et 7 \] .</span><span class="sxs-lookup"><span data-stu-id="433a8-140">The literal values are a set of 4 bit 2's complement numbers, having integer range \[-8,7\].</span></span> <span data-ttu-id="433a8-141">Ce modificateur est défini pour toutes les ressources, y compris les tableaux Texture1D/2D et Texture3D, mais il n’est pas défini pour TextureCube.</span><span class="sxs-lookup"><span data-stu-id="433a8-141">This modifier is defined for all Resources, including Texture1D/2D Arrays and Texture3D, but it is undefined for TextureCube.</span></span>

<span data-ttu-id="433a8-142">Le matériel peut tirer parti d’une connaissance immédiate selon laquelle un parcours sur une certaine empreinte des texels à propos d’un emplacement commun est effectué par un ensemble d’instructions d’exemple.</span><span class="sxs-lookup"><span data-stu-id="433a8-142">Hardware can take advantage of immediate knowledge that a traversal over some footprint of texels about a common location is being performed by a set of sample instructions.</span></span> <span data-ttu-id="433a8-143">Cela peut être transmis à l’aide \_ de aoffimmi (u, v, w).</span><span class="sxs-lookup"><span data-stu-id="433a8-143">This can be conveyed using \_aoffimmi(u,v,w).</span></span>

<span data-ttu-id="433a8-144">Les décalages sont ajoutés aux coordonnées de texture, dans l’espace Texel, par rapport à chaque miplevel accédé.</span><span class="sxs-lookup"><span data-stu-id="433a8-144">The offsets are added to the texture coordinates, in texel space, relative to each miplevel being accessed.</span></span> <span data-ttu-id="433a8-145">Ainsi, même si les coordonnées de texture sont fournies en tant que valeurs float normalisées, le décalage applique un décalage d’entier d’espace Texel.</span><span class="sxs-lookup"><span data-stu-id="433a8-145">So even though texture coordinates are provided as normalized float values, the offset applies a texel-space integer offset.</span></span>

<span data-ttu-id="433a8-146">Les décalages d’adresse ne sont pas appliqués le long de l’axe de tableau des tableaux Texture1D/2D.</span><span class="sxs-lookup"><span data-stu-id="433a8-146">Address offsets are not applied along the array axis of Texture1D/2D Arrays.</span></span>

<span data-ttu-id="433a8-147">\_aoffimmi v, w Components sont ignorés pour Texture1Ds.</span><span class="sxs-lookup"><span data-stu-id="433a8-147">\_aoffimmi v,w components are ignored for Texture1Ds.</span></span>

<span data-ttu-id="433a8-148">\_le composant aoffimmi w est ignoré pour Texture2Ds.</span><span class="sxs-lookup"><span data-stu-id="433a8-148">\_aoffimmi w component is ignored for Texture2Ds.</span></span>

<span data-ttu-id="433a8-149">Les modes de renvoi à la ligne de l’adresse (Wrap/Mirror/collier/bordure, etc.) du ou des États de l’échantillonneur \# sont appliqués après l’application d’un décalage d’adresse à des coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="433a8-149">Address wrapping modes (wrap/mirror/clamp/border etc.) from the sampler state (s\#) are applied after any address offset is applied to texture coordinates.</span></span>

### <a name="return-type-control"></a><span data-ttu-id="433a8-150">Contrôle de type de retour</span><span class="sxs-lookup"><span data-stu-id="433a8-150">Return Type Control</span></span>

<span data-ttu-id="433a8-151">Le format de données retourné par l’exemple au registre de destination est déterminé par le format de ressource ( \_ format dxgi \* ) lié au paramètre *srcResource* (t \# ).</span><span class="sxs-lookup"><span data-stu-id="433a8-151">The data format returned by the sample to the destination register is determined by the resource format (DXGI\_FORMAT\*) bound to the *srcResource* parameter (t\#).</span></span> <span data-ttu-id="433a8-152">Par exemple, si le t spécifié \# a été lié à une ressource au format \_ dxgi \_ A8B8G8R8 \_ UNORM \_ sRVB, l’opération d’échantillonnage convertira les texels échantillonnés de gamma 2,0 à 1,0, appliquera le filtrage et le résultat sera écrit dans le registre de destination en tant que valeurs à virgule flottante dans la plage \[ 0.. 1 \] .</span><span class="sxs-lookup"><span data-stu-id="433a8-152">For example, if the specified t\# was bound with a resource with format DXGI\_FORMAT\_A8B8G8R8\_UNORM\_SRGB, then the sampling operation will convert sampled texels from gamma 2.0 to 1.0, apply filtering, and the result will written to the destination register as floating point values in the range \[0..1\].</span></span>

<span data-ttu-id="433a8-153">Les valeurs retournées sont 4-vectors (avec des valeurs par défaut spécifiques au format pour les composants qui ne sont pas présents au format).</span><span class="sxs-lookup"><span data-stu-id="433a8-153">Returned values are 4-vectors (with format-specific defaults for components not present in the format).</span></span> <span data-ttu-id="433a8-154">Swizzle sur *srcResource* détermine comment Swizzle le résultat à 4 composants à partir de l’échantillon de texture/filtre, après quoi. Mask sur *dest* détermine les composants de *dest* qui sont mis à jour.</span><span class="sxs-lookup"><span data-stu-id="433a8-154">The swizzle on *srcResource* determines how to swizzle the 4-component result coming back from the texture sample/filter, after which .mask on *dest* determines which components in *dest* get updated.</span></span>

<span data-ttu-id="433a8-155">Quand **Sample** lit une valeur float 32 bits dans un registre 32 bits, avec l’échantillonnage de point (aucun filtrage), il peut ou non vider les valeurs dénormalisées, mais les autres valeurs ne sont pas modifiées.</span><span class="sxs-lookup"><span data-stu-id="433a8-155">When **sample** reads a 32-bit float value into a 32-bit register, with point sampling (no filtering), it may or may not flush denormal values, but otherwise numbers are unmodified.</span></span> <span data-ttu-id="433a8-156">Si l’incertitude avec les valeurs de dénormalisation par échantillonnage des points est un problème pour une application, utilisez l’instruction [LD](ld--sm4---asm-.md) , qui garantit que les valeurs float 32 bits sont lues sans modification.</span><span class="sxs-lookup"><span data-stu-id="433a8-156">If the uncertainty with point sampling denormal values is an issue for an application,use the [ld](ld--sm4---asm-.md) instruction, which guarantees that 32-bit float values are read unmodified.</span></span>

### <a name="lod-calculation"></a><span data-ttu-id="433a8-157">Calcul LOD</span><span class="sxs-lookup"><span data-stu-id="433a8-157">LOD Calculation</span></span>

<span data-ttu-id="433a8-158">Pour plus d’informations sur la façon dont les dérivés sont calculés dans le processus de détermination de LOD pour le filtrage, consultez [Deriv \_ RTX](deriv-rtx--sm4---asm-.md) et [Deriv \_ propriété](deriv-rty--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="433a8-158">For details on how derivatives are calculated in the process of determining LOD for filtering, see [deriv\_rtx](deriv-rtx--sm4---asm-.md) and [deriv\_rty](deriv-rty--sm4---asm-.md).</span></span> <span data-ttu-id="433a8-159">L' **exemple** d’instruction calcule implicitement les dérivés sur les coordonnées de texture à l’aide de la même définition que celle utilisée par les instructions du nuanceur **Deriv** .</span><span class="sxs-lookup"><span data-stu-id="433a8-159">The **sample** instruction implicitly computes derivatives on the texture coordinates using the same definition that the **deriv** Shader instructions use.</span></span> <span data-ttu-id="433a8-160">Cela ne s’applique pas à l' [exemple \_ l](sample-l--sm4---asm-.md) ou à des exemples d’instructions [ \_ d](sample-d--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="433a8-160">This does not apply to [sample\_l](sample-l--sm4---asm-.md) or [sample\_d](sample-d--sm4---asm-.md) instructions.</span></span> <span data-ttu-id="433a8-161">Pour ces instructions, LOD ou les dérivés sont fournis directement par l’application.</span><span class="sxs-lookup"><span data-stu-id="433a8-161">For those instructions, LOD or derivatives are provided directly by the application.</span></span>

<span data-ttu-id="433a8-162">Pour l' **exemple** d’instruction, les implémentations peuvent choisir de partager le même calcul de LOD sur les 4 pixels d’un tampon 2x2 (mais pas de plus grande zone) ou d’effectuer des calculs de LOD par pixel.</span><span class="sxs-lookup"><span data-stu-id="433a8-162">For the **sample** instruction, implementations can choose to share the same LOD calculation across all 4 pixels in a 2x2 stamp (but no larger area), or perform per-pixel LOD calculations.</span></span>

### <a name="miscellaneous-details"></a><span data-ttu-id="433a8-163">Détails divers</span><span class="sxs-lookup"><span data-stu-id="433a8-163">Miscellaneous Details</span></span>

<span data-ttu-id="433a8-164">Pour la mémoire tampon & Texture1D, les composants *srcAddress* . GBA (pos-Swizzle) sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="433a8-164">For Buffer & Texture1D, *srcAddress* .gba components (POS-swizzle) are ignored.</span></span> <span data-ttu-id="433a8-165">Pour les tableaux Texture1D, les composants *srcAddress* . BA (pos-Swizzle) sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="433a8-165">For Texture1D Arrays, *srcAddress* .ba components (POS-swizzle) are ignored.</span></span> <span data-ttu-id="433a8-166">Pour Texture2Ds, *srcAddress* . a Component (pos-Swizzle) est ignoré.</span><span class="sxs-lookup"><span data-stu-id="433a8-166">For Texture2Ds, *srcAddress* .a component (POS-swizzle) is ignored.</span></span>

<span data-ttu-id="433a8-167">L’extraction à partir d’un emplacement d’entrée auquel rien n’est lié retourne 0 pour tous les composants.</span><span class="sxs-lookup"><span data-stu-id="433a8-167">Fetching from an input slot that has nothing bound to it returns 0 for all components.</span></span>

### <a name="restrictions"></a><span data-ttu-id="433a8-168">Restrictions</span><span class="sxs-lookup"><span data-stu-id="433a8-168">Restrictions</span></span>

-   <span data-ttu-id="433a8-169">*srcResource* doit être un \# Registre t.</span><span class="sxs-lookup"><span data-stu-id="433a8-169">*srcResource* must be a t\# register.</span></span> <span data-ttu-id="433a8-170">*srcResource* ne peut pas être un ConstantBuffer, qui ne peut pas être lié à des \# registres t.</span><span class="sxs-lookup"><span data-stu-id="433a8-170">*srcResource* cannot be a ConstantBuffer, which cannot be bound to t\# registers.</span></span>
-   <span data-ttu-id="433a8-171">*srcSampler* doit être un \# Registre s.</span><span class="sxs-lookup"><span data-stu-id="433a8-171">*srcSampler* must be an s\# register.</span></span>
-   <span data-ttu-id="433a8-172">L’adressage relatif sur *srcResource* ou *srcSampler* n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="433a8-172">Relative addressing on *srcResource* or *srcSampler* is not permitted.</span></span>
-   <span data-ttu-id="433a8-173">*srcAddress* doit être un registre Temp (r \# /X \# ), constantBuffer (CB \# ), Input (v \# ) ou une ou plusieurs valeurs immédiates.</span><span class="sxs-lookup"><span data-stu-id="433a8-173">*srcAddress* must be a temp (r\#/x\#), constantBuffer (cb\#), input (v\#) register or immediate value(s).</span></span>
-   <span data-ttu-id="433a8-174">*dest* doit être un registre Temp (r \# /x \# ) ou Output (o \* \# ).</span><span class="sxs-lookup"><span data-stu-id="433a8-174">*dest* must be a temp (r\#/x\#) or output (o\*\#) register.</span></span>
-   <span data-ttu-id="433a8-175">\_aoffimmi (u, v, w) n’est pas autorisé pour TextureCubes.</span><span class="sxs-lookup"><span data-stu-id="433a8-175">\_aoffimmi(u,v,w) is not permitted for TextureCubes.</span></span>

<span data-ttu-id="433a8-176">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="433a8-176">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="433a8-177">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="433a8-177">Vertex Shader</span></span> | <span data-ttu-id="433a8-178">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="433a8-178">Geometry Shader</span></span> | <span data-ttu-id="433a8-179">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="433a8-179">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="433a8-180">x</span><span class="sxs-lookup"><span data-stu-id="433a8-180">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="433a8-181">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="433a8-181">Minimum Shader Model</span></span>

<span data-ttu-id="433a8-182">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="433a8-182">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="433a8-183">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="433a8-183">Shader Model</span></span>                                              | <span data-ttu-id="433a8-184">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="433a8-184">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="433a8-185">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="433a8-185">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="433a8-186">Oui</span><span class="sxs-lookup"><span data-stu-id="433a8-186">yes</span></span>       |
| [<span data-ttu-id="433a8-187">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="433a8-187">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="433a8-188">Oui</span><span class="sxs-lookup"><span data-stu-id="433a8-188">yes</span></span>       |
| [<span data-ttu-id="433a8-189">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="433a8-189">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="433a8-190">Oui</span><span class="sxs-lookup"><span data-stu-id="433a8-190">yes</span></span>       |
| [<span data-ttu-id="433a8-191">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="433a8-191">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="433a8-192">non</span><span class="sxs-lookup"><span data-stu-id="433a8-192">no</span></span>        |
| [<span data-ttu-id="433a8-193">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="433a8-193">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="433a8-194">non</span><span class="sxs-lookup"><span data-stu-id="433a8-194">no</span></span>        |
| [<span data-ttu-id="433a8-195">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="433a8-195">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="433a8-196">non</span><span class="sxs-lookup"><span data-stu-id="433a8-196">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="433a8-197">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="433a8-197">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="433a8-198">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="433a8-198">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





