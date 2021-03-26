---
title: texld-ps_2_0 et haut
description: Échantillonner une texture au niveau d’un échantillonneur particulier, à l’aide des coordonnées de texture fournies. Cette instruction est différente de l’instruction texld-PS \_ 1 \_ 4 utilisée dans le nuanceur de pixels version 1 \_ 4.
ms.assetid: 2b0d02b4-d9dd-4388-aa86-03b27bc4fdc8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b71990e230290403bca2a5af11eeca11b093402f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104507981"
---
# <a name="texld---ps_2_0-and-up"></a><span data-ttu-id="39b57-104">texld-PS \_ 2 \_ 0 et haut</span><span class="sxs-lookup"><span data-stu-id="39b57-104">texld - ps\_2\_0 and up</span></span>

<span data-ttu-id="39b57-105">Échantillonner une texture au niveau d’un échantillonneur particulier, à l’aide des coordonnées de texture fournies.</span><span class="sxs-lookup"><span data-stu-id="39b57-105">Sample a texture at a particular sampler, using provided texture coordinates.</span></span> <span data-ttu-id="39b57-106">Cette instruction est différente de l’instruction [texld-PS \_ 1 \_ 4](texld---ps-1-4.md) utilisée dans le nuanceur de pixels version 1 \_ 4.</span><span class="sxs-lookup"><span data-stu-id="39b57-106">This instruction is different from the [texld - ps\_1\_4](texld---ps-1-4.md) instruction used in pixel shader version 1\_4.</span></span>

## <a name="syntax"></a><span data-ttu-id="39b57-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="39b57-107">Syntax</span></span>



| <span data-ttu-id="39b57-108">texld DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="39b57-108">texld dst, src0, src1</span></span> |
|-----------------------|



 

<span data-ttu-id="39b57-109">Où :</span><span class="sxs-lookup"><span data-stu-id="39b57-109">Where:</span></span>

-   <span data-ttu-id="39b57-110">l’heure d’été est un registre de destination.</span><span class="sxs-lookup"><span data-stu-id="39b57-110">dst is a destination register.</span></span>
-   <span data-ttu-id="39b57-111">src0 est un registre source qui fournit les coordonnées de texture pour l’échantillon de texture.</span><span class="sxs-lookup"><span data-stu-id="39b57-111">src0 is a source register that provides the texture coordinates for the texture sample.</span></span>
-   <span data-ttu-id="39b57-112">src1 identifie l' [échantillonneur (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# , où \# spécifie le numéro d’échantillonnage de texture à échantillonner.</span><span class="sxs-lookup"><span data-stu-id="39b57-112">src1 identifies the [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), where \# specifies which texture sampler number to sample.</span></span> <span data-ttu-id="39b57-113">L’échantillonneur lui est associé une texture et un état d’échantillonneur défini par [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span><span class="sxs-lookup"><span data-stu-id="39b57-113">The sampler has associated with it a texture and a sampler state defined by [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span></span>

### <a name="ps_2_0-and-ps_2_x"></a><span data-ttu-id="39b57-114">PS \_ 2 \_ 0 et PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="39b57-114">ps\_2\_0 and ps\_2\_x</span></span>

<span data-ttu-id="39b57-115">l’heure d’été doit être un [Registre temporaire](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) et seul le masque XYZW (masque par défaut) est autorisé.</span><span class="sxs-lookup"><span data-stu-id="39b57-115">dst must be a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) and only .xyzw mask (default mask) is allowed.</span></span>

<span data-ttu-id="39b57-116">src0 doit être un [Registre de coordonnées de texture](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t \# ) ou un [Registre temporaire](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ), sans modificateur ni Swizzle.</span><span class="sxs-lookup"><span data-stu-id="39b57-116">src0 must be either a [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t\#) or a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#), with no modifier or swizzle.</span></span>

<span data-ttu-id="39b57-117">src1 doit être un [échantillonneur (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) , sans \# modificateur ni Swizzle.</span><span class="sxs-lookup"><span data-stu-id="39b57-117">src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), with no modifier or swizzle.</span></span>

<span data-ttu-id="39b57-118">Si le \_ \_ bit d’extrémité D3DD3DPSHADERCAPS2 0 NODEPENDENTREADLIMIT n’est pas défini (dans D3DPSHADERCAPS2 \_ 0), une instruction de texture donnée ([texld](texld---ps-1-4.md), [texldp](texldp---ps.md), [texldb-PS](texldb---ps.md), [texldd](texldd---ps.md) ) peut dépendre, au plus, du troisième ordre.</span><span class="sxs-lookup"><span data-stu-id="39b57-118">If the D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT cap bit is not set (in D3DPSHADERCAPS2\_0), a given texture instruction ([texld](texld---ps-1-4.md), [texldp](texldp---ps.md), [texldb - ps](texldb---ps.md), [texldd](texldd---ps.md) ) may be dependent upon, at most, third order.</span></span> <span data-ttu-id="39b57-119">Une instruction de texture dépendante de premier ordre est une instruction de texture dans laquelle :</span><span class="sxs-lookup"><span data-stu-id="39b57-119">A first-order dependent texture instruction is a texture instruction in which either:</span></span>

-   <span data-ttu-id="39b57-120">src0 est un [Registre temporaire](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).</span><span class="sxs-lookup"><span data-stu-id="39b57-120">src0 is a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#).</span></span>
-   <span data-ttu-id="39b57-121">l’heure d’été a été écrite précédemment, en cours de réécriture.</span><span class="sxs-lookup"><span data-stu-id="39b57-121">dst was previously written, now being written again.</span></span>

<span data-ttu-id="39b57-122">Une instruction de texture dépendante d’une seconde commande est définie comme une instruction de texture qui lit ou écrit dans un [Registre temporaire](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) dont le contenu, avant d’exécuter l’instruction de texture, dépend (peut-être indirectement) du résultat d’une instruction de texture dépendante de premier ordre.</span><span class="sxs-lookup"><span data-stu-id="39b57-122">A second-order dependent texture instruction is defined as a texture instruction that reads or writes to a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) whose contents, before executing the texture instruction, depend (perhaps indirectly) on the outcome of a first-order dependent texture instruction.</span></span> <span data-ttu-id="39b57-123">Une instruction de texture dépendante (n)<sup>th</sup>dérive d’une instruction de texture (n-1)<sup>th</sup>-Order.</span><span class="sxs-lookup"><span data-stu-id="39b57-123">An (n)<sup>th</sup>-order dependent texture instruction derives from an (n - 1)<sup>th</sup>-order texture instruction.</span></span>

### <a name="ps_3_0"></a><span data-ttu-id="39b57-124">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="39b57-124">ps\_3\_0</span></span>

<span data-ttu-id="39b57-125">src1 doit être un [échantillonneur (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) , sans \# modificateur.</span><span class="sxs-lookup"><span data-stu-id="39b57-125">src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), with no modifier.</span></span> <span data-ttu-id="39b57-126">Swizzle est autorisé sur src0 ou src1.</span><span class="sxs-lookup"><span data-stu-id="39b57-126">Swizzle is allowed on src0 or src1.</span></span> <span data-ttu-id="39b57-127">Swizzle est appliqué à la texture coordintates avant la recherche de texture.</span><span class="sxs-lookup"><span data-stu-id="39b57-127">The swizzle is applied to the texture coordintates before texture lookup.</span></span>

## <a name="remarks"></a><span data-ttu-id="39b57-128">Notes</span><span class="sxs-lookup"><span data-stu-id="39b57-128">Remarks</span></span>

<span data-ttu-id="39b57-129">Cette instruction est prise en charge dans les versions suivantes :</span><span class="sxs-lookup"><span data-stu-id="39b57-129">This instruction is supported in the following versions:</span></span>



| <span data-ttu-id="39b57-130">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="39b57-130">Pixel shader versions</span></span> | <span data-ttu-id="39b57-131">1\_1</span><span class="sxs-lookup"><span data-stu-id="39b57-131">1\_1</span></span> | <span data-ttu-id="39b57-132">1\_2</span><span class="sxs-lookup"><span data-stu-id="39b57-132">1\_2</span></span> | <span data-ttu-id="39b57-133">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="39b57-133">1\_3</span></span> | <span data-ttu-id="39b57-134">1\_4</span><span class="sxs-lookup"><span data-stu-id="39b57-134">1\_4</span></span> | <span data-ttu-id="39b57-135">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="39b57-135">2\_0</span></span> | <span data-ttu-id="39b57-136">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="39b57-136">2\_x</span></span> | <span data-ttu-id="39b57-137">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="39b57-137">2\_sw</span></span> | <span data-ttu-id="39b57-138">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="39b57-138">3\_0</span></span> | <span data-ttu-id="39b57-139">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="39b57-139">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="39b57-140">texld</span><span class="sxs-lookup"><span data-stu-id="39b57-140">texld</span></span>                 |      |      |      |      | <span data-ttu-id="39b57-141">x</span><span class="sxs-lookup"><span data-stu-id="39b57-141">x</span></span>    | <span data-ttu-id="39b57-142">x</span><span class="sxs-lookup"><span data-stu-id="39b57-142">x</span></span>    | <span data-ttu-id="39b57-143">x</span><span class="sxs-lookup"><span data-stu-id="39b57-143">x</span></span>     | <span data-ttu-id="39b57-144">x</span><span class="sxs-lookup"><span data-stu-id="39b57-144">x</span></span>    | <span data-ttu-id="39b57-145">x</span><span class="sxs-lookup"><span data-stu-id="39b57-145">x</span></span>     |



 

<span data-ttu-id="39b57-146">Le nombre de coordonnées nécessaires à l’exécution de l’exemple de texture par src0 dépend de la manière dont src1 a été déclaré, plus le composant. w.</span><span class="sxs-lookup"><span data-stu-id="39b57-146">The number of coordinates required for src0 to perform the texture sample depends on how src1 was declared, plus the .w component.</span></span> <span data-ttu-id="39b57-147">Les types d’échantillonneur sont déclarés avec le [ \_ samplerType DCL (SM2, SM3-PS ASM)](dcl-samplertype---ps.md).</span><span class="sxs-lookup"><span data-stu-id="39b57-147">Sampler types are declared with [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md).</span></span> <span data-ttu-id="39b57-148">Si src1 est déclaré en tant qu’échantillonneur 2D, src0 doit contenir des coordonnées. XY ; Si src1 est déclaré comme un échantillonneur de cube ou un échantillonneur de volume, src0 doit contenir des coordonnées. xyz.</span><span class="sxs-lookup"><span data-stu-id="39b57-148">If src1 is declared as a 2D sampler, then src0 must contain .xy coordinates; if src1 is declared as either a cube sampler or a volume sampler, then src0 must contain .xyz coordinates.</span></span> <span data-ttu-id="39b57-149">L’échantillonnage d’une texture avec moins de dimensions que celles présentes dans la coordonnée de texture est autorisé, car le ou les composants de coordonnée de texture supplémentaires sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="39b57-149">Sampling a texture with fewer dimensions than are present in the texture coordinate is allowed since the extra texture coordinate component(s) are ignored.</span></span>

<span data-ttu-id="39b57-150">Si la texture source contient moins de quatre composants, les valeurs par défaut sont placées dans les composants manquants.</span><span class="sxs-lookup"><span data-stu-id="39b57-150">If the source texture contains fewer than four components, defaults are placed in the missing components.</span></span> <span data-ttu-id="39b57-151">Les valeurs par défaut dépendent du format de texture, comme indiqué dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="39b57-151">Defaults depend on the texture format as shown in the following table:</span></span>



| <span data-ttu-id="39b57-152">Format de texture</span><span class="sxs-lookup"><span data-stu-id="39b57-152">Texture Format</span></span>                                                                                          | <span data-ttu-id="39b57-153">Valeurs par défaut</span><span class="sxs-lookup"><span data-stu-id="39b57-153">Default Values</span></span>       |
|---------------------------------------------------------------------------------------------------------|----------------------|
| <span data-ttu-id="39b57-154">D3DFMT \_ R5G6B5, D3DFMT \_ R8G8B8, D3DFMT \_ L8, D3DFMT \_ L16, D3DFMT \_ R3G3B2, D3DFMT \_ CxV8U8, D3DFMT \_ L6V5U5</span><span class="sxs-lookup"><span data-stu-id="39b57-154">D3DFMT\_R5G6B5, D3DFMT\_R8G8B8, D3DFMT\_L8, D3DFMT\_L16, D3DFMT\_R3G3B2, D3DFMT\_CxV8U8, D3DFMT\_L6V5U5</span></span> | <span data-ttu-id="39b57-155">A = 1,0</span><span class="sxs-lookup"><span data-stu-id="39b57-155">A = 1.0</span></span>              |
| <span data-ttu-id="39b57-156">D3DFMT \_ V8U8, D3DFMT \_ V16U16, D3DFMT \_ G16R16, D3DFMT \_ G16R16F, D3DFMT \_ G32R32F</span><span class="sxs-lookup"><span data-stu-id="39b57-156">D3DFMT\_V8U8, D3DFMT\_V16U16, D3DFMT\_G16R16, D3DFMT\_G16R16F, D3DFMT\_G32R32F</span></span>                          | <span data-ttu-id="39b57-157">B = A = 1,0</span><span class="sxs-lookup"><span data-stu-id="39b57-157">B = A = 1.0</span></span>          |
| <span data-ttu-id="39b57-158">D3DFMT \_ a8</span><span class="sxs-lookup"><span data-stu-id="39b57-158">D3DFMT\_A8</span></span>                                                                                              | <span data-ttu-id="39b57-159">R = G = B = 0,0</span><span class="sxs-lookup"><span data-stu-id="39b57-159">R = G = B = 0.0</span></span>      |
| <span data-ttu-id="39b57-160">D3DFMT \_ R16F, D3DFMT \_ R32F</span><span class="sxs-lookup"><span data-stu-id="39b57-160">D3DFMT\_R16F, D3DFMT\_R32F</span></span>                                                                              | <span data-ttu-id="39b57-161">G = B = A = 1,0</span><span class="sxs-lookup"><span data-stu-id="39b57-161">G = B = A = 1.0</span></span>      |
| <span data-ttu-id="39b57-162">Tous les formats de profondeur/gabarit</span><span class="sxs-lookup"><span data-stu-id="39b57-162">All depth/stencil formats</span></span>                                                                               | <span data-ttu-id="39b57-163">R = B = 0,0, A = 1,0</span><span class="sxs-lookup"><span data-stu-id="39b57-163">R = B = 0.0, A = 1.0</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="39b57-164">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="39b57-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39b57-165">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="39b57-165">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 