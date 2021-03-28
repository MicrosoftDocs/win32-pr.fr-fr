---
title: texldb-PS
description: Instruction de chargement de texture biaisée. Cette instruction utilise le quatrième élément (. a ou. w) pour écarter le niveau de détail de l’échantillonnage de texture juste avant l’échantillonnage.
ms.assetid: cafd72c9-b7bb-4e3f-8a8c-de26a4446864
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 912c4c61f6c1f2b6bef46c7c5b6ea17223df5eb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101784"
---
# <a name="texldb---ps"></a><span data-ttu-id="814b6-104">texldb-PS</span><span class="sxs-lookup"><span data-stu-id="814b6-104">texldb - ps</span></span>

<span data-ttu-id="814b6-105">Instruction de chargement de texture biaisée.</span><span class="sxs-lookup"><span data-stu-id="814b6-105">Biased texture load instruction.</span></span> <span data-ttu-id="814b6-106">Cette instruction utilise le quatrième élément (. a ou. w) pour écarter le niveau de détail de l’échantillonnage de texture juste avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="814b6-106">This instruction uses the fourth element (.a or .w) to bias the texture-sampling level-of-detail just before sampling.</span></span>

## <a name="syntax"></a><span data-ttu-id="814b6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="814b6-107">Syntax</span></span>



| <span data-ttu-id="814b6-108">texldb DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="814b6-108">texldb dst, src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="814b6-109">Où :</span><span class="sxs-lookup"><span data-stu-id="814b6-109">Where:</span></span>

-   <span data-ttu-id="814b6-110">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="814b6-110">dst is the destination register.</span></span>
-   <span data-ttu-id="814b6-111">src0 est un registre source qui fournit les coordonnées de texture pour l’échantillon de texture.</span><span class="sxs-lookup"><span data-stu-id="814b6-111">src0 is a source register that provides the texture coordinates for the texture sample.</span></span> <span data-ttu-id="814b6-112">Consultez [Registre de coordonnées de texture](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span><span class="sxs-lookup"><span data-stu-id="814b6-112">See [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span></span>
-   <span data-ttu-id="814b6-113">src1 identifie l' [échantillonneur (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# , où \# spécifie le numéro d’échantillonnage de texture à échantillonner.</span><span class="sxs-lookup"><span data-stu-id="814b6-113">src1 identifies the [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), where \# specifies which texture sampler number to sample.</span></span> <span data-ttu-id="814b6-114">L’échantillonneur lui est associé une texture et un état d’échantillonneur défini par [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span><span class="sxs-lookup"><span data-stu-id="814b6-114">The sampler has associated with it a texture and a sampler state defined by [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span></span>

<span data-ttu-id="814b6-115">Pour connaître les restrictions liées à l’utilisation de texldb, consultez les instructions [texld-PS \_ 2 \_ 0 et up](texld---ps-2-0.md) .</span><span class="sxs-lookup"><span data-stu-id="814b6-115">For the restrictions when using texldb, see the [texld - ps\_2\_0 and up](texld---ps-2-0.md) instruction.</span></span>

### <a name="ps_2_0-and-ps_2_x"></a><span data-ttu-id="814b6-116">PS \_ 2 \_ 0 et PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="814b6-116">ps\_2\_0 and ps\_2\_x</span></span>

<span data-ttu-id="814b6-117">l’heure d’été doit être un [Registre temporaire](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) et seul le masque XYZW (masque par défaut) est autorisé.</span><span class="sxs-lookup"><span data-stu-id="814b6-117">dst must be a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) and only .xyzw mask (default mask) is allowed.</span></span>

<span data-ttu-id="814b6-118">src0 doit être un [Registre de coordonnées de texture](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t \# ) ou un [Registre temporaire](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ), sans modificateur ni Swizzle.</span><span class="sxs-lookup"><span data-stu-id="814b6-118">src0 must be either a [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t\#) or a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#), with no modifier or swizzle.</span></span>

<span data-ttu-id="814b6-119">src1 doit être un [échantillonneur (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) , sans \# modificateur ni Swizzle.</span><span class="sxs-lookup"><span data-stu-id="814b6-119">src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), with no modifier or swizzle.</span></span>

<span data-ttu-id="814b6-120">Si le \_ \_ bit d’extrémité D3DD3DPSHADERCAPS2 0 NODEPENDENTREADLIMIT n’est pas défini (dans D3DPSHADERCAPS2 \_ 0), une instruction de texture donnée (texld, texldp, texldb, texldd) peut dépendre, au plus, du troisième ordre.</span><span class="sxs-lookup"><span data-stu-id="814b6-120">If the D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT cap bit is not set (in D3DPSHADERCAPS2\_0), a given texture instruction (texld, texldp, texldb, texldd) may be dependent upon, at most, third order.</span></span> <span data-ttu-id="814b6-121">Une instruction de texture dépendante de premier ordre est une instruction de texture dans laquelle :</span><span class="sxs-lookup"><span data-stu-id="814b6-121">A first-order dependent texture instruction is a texture instruction in which either:</span></span>

-   <span data-ttu-id="814b6-122">src0 est un [Registre temporaire](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).</span><span class="sxs-lookup"><span data-stu-id="814b6-122">src0 is a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#).</span></span>
-   <span data-ttu-id="814b6-123">l’heure d’été a été écrite précédemment, en cours de réécriture.</span><span class="sxs-lookup"><span data-stu-id="814b6-123">dst was previously written, now being written again.</span></span>

<span data-ttu-id="814b6-124">Une instruction de texture dépendante d’une seconde commande est définie comme une instruction de texture qui lit ou écrit dans un [Registre temporaire](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) dont le contenu, avant d’exécuter l’instruction de texture, dépend (peut-être indirectement) du résultat d’une instruction de texture dépendante de premier ordre.</span><span class="sxs-lookup"><span data-stu-id="814b6-124">A second-order dependent texture instruction is defined as a texture instruction that reads or writes to a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) whose contents, before executing the texture instruction, depend (perhaps indirectly) on the outcome of a first-order dependent texture instruction.</span></span> <span data-ttu-id="814b6-125">Une instruction de texture dépendante (n)<sup>th</sup>dérive d’une instruction de texture (n-1)<sup>th</sup>-Order.</span><span class="sxs-lookup"><span data-stu-id="814b6-125">An (n)<sup>th</sup>-order dependent texture instruction derives from an (n - 1)<sup>th</sup>-order texture instruction.</span></span>

### <a name="ps_3_0"></a><span data-ttu-id="814b6-126">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="814b6-126">ps\_3\_0</span></span>

<span data-ttu-id="814b6-127">src1 doit être un [échantillonneur (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) , sans \# modificateur.</span><span class="sxs-lookup"><span data-stu-id="814b6-127">src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), with no modifier.</span></span> <span data-ttu-id="814b6-128">Swizzle est autorisé sur src1 et, lorsqu’il est appliqué, les résultats de la recherche de texture sont antérieurs à swizzled avant d’être écrits dans l’heure d’été.</span><span class="sxs-lookup"><span data-stu-id="814b6-128">Swizzle is allowed on src1, and when applied, the texture lookup results are pre-swizzled before written to dst.</span></span>

## <a name="remarks"></a><span data-ttu-id="814b6-129">Notes</span><span class="sxs-lookup"><span data-stu-id="814b6-129">Remarks</span></span>



| <span data-ttu-id="814b6-130">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="814b6-130">Pixel shader versions</span></span> | <span data-ttu-id="814b6-131">1\_1</span><span class="sxs-lookup"><span data-stu-id="814b6-131">1\_1</span></span> | <span data-ttu-id="814b6-132">1\_2</span><span class="sxs-lookup"><span data-stu-id="814b6-132">1\_2</span></span> | <span data-ttu-id="814b6-133">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="814b6-133">1\_3</span></span> | <span data-ttu-id="814b6-134">1\_4</span><span class="sxs-lookup"><span data-stu-id="814b6-134">1\_4</span></span> | <span data-ttu-id="814b6-135">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="814b6-135">2\_0</span></span> | <span data-ttu-id="814b6-136">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="814b6-136">2\_x</span></span> | <span data-ttu-id="814b6-137">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="814b6-137">2\_sw</span></span> | <span data-ttu-id="814b6-138">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="814b6-138">3\_0</span></span> | <span data-ttu-id="814b6-139">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="814b6-139">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="814b6-140">texldb</span><span class="sxs-lookup"><span data-stu-id="814b6-140">texldb</span></span>                |      |      |      |      | <span data-ttu-id="814b6-141">x</span><span class="sxs-lookup"><span data-stu-id="814b6-141">x</span></span>    | <span data-ttu-id="814b6-142">x</span><span class="sxs-lookup"><span data-stu-id="814b6-142">x</span></span>    | <span data-ttu-id="814b6-143">x</span><span class="sxs-lookup"><span data-stu-id="814b6-143">x</span></span>     | <span data-ttu-id="814b6-144">x</span><span class="sxs-lookup"><span data-stu-id="814b6-144">x</span></span>    | <span data-ttu-id="814b6-145">x</span><span class="sxs-lookup"><span data-stu-id="814b6-145">x</span></span>     |



 

<span data-ttu-id="814b6-146">texldb biaise le niveau de détail mipmap, calculé normalement dans le cadre de l’exemple de processus par la valeur (signée) de src0. w.</span><span class="sxs-lookup"><span data-stu-id="814b6-146">texldb biases the mipmap level-of-detail, computed normally as part of the sample process by the (signed) value in src0.w.</span></span> <span data-ttu-id="814b6-147">Les valeurs d’écart positives entraînent la sélection de la des mipmaps plus petite et vice versa.</span><span class="sxs-lookup"><span data-stu-id="814b6-147">Positive bias values will result in smaller mipmaps being selected and vice versa.</span></span> <span data-ttu-id="814b6-148">Pour PS \_ 2 \_ 0 et PS \_ 2 \_ x, les valeurs de biais peuvent être comprises dans la plage \[ -3,0, + 3,0 \] .</span><span class="sxs-lookup"><span data-stu-id="814b6-148">For ps\_2\_0 and ps\_2\_x, bias values can be within the range \[-3.0, +3.0\].</span></span> <span data-ttu-id="814b6-149">Pour PS \_ 3 \_ 0, les valeurs de biais peuvent être comprises dans la plage \[ -16,0, + 15,0 \] .</span><span class="sxs-lookup"><span data-stu-id="814b6-149">For ps\_3\_0, bias values can be within the range \[-16.0, +15.0\].</span></span> <span data-ttu-id="814b6-150">Les valeurs de biais en dehors de ces plages produisent des résultats indéfinis.</span><span class="sxs-lookup"><span data-stu-id="814b6-150">Bias values outside these ranges produce undefined results.</span></span> <span data-ttu-id="814b6-151">L’état de l’échantillonneur D3DSAMP \_ MIPMAPLODBIAS est toujours respecté et le biais du texldb est ajouté à cette valeur, mais pour chaque pixel.</span><span class="sxs-lookup"><span data-stu-id="814b6-151">The sampler state D3DSAMP\_MIPMAPLODBIAS is still honored, and the texldb bias is added to this, but on a per-pixel basis.</span></span> <span data-ttu-id="814b6-152">Une fois le niveau de détail biaisé calculé, D3DSAMP \_ MAXMIPLEVEL est toujours respecté et l’échantillon de texture se produit.</span><span class="sxs-lookup"><span data-stu-id="814b6-152">After the biased level-of-detail is computed, D3DSAMP\_MAXMIPLEVEL is still honored and the texture sample occurs.</span></span> <span data-ttu-id="814b6-153">Après texldb, le contenu de src0 n’est pas affecté (sauf si l’heure d’été est le même registre).</span><span class="sxs-lookup"><span data-stu-id="814b6-153">After texldb, the contents of src0 are unaffected (unless dst is the same register).</span></span>

<span data-ttu-id="814b6-154">Le nombre de coordonnées nécessaires à l’exécution de l’exemple de texture par src0 dépend de la manière dont src1 a été déclaré, plus le composant. w.</span><span class="sxs-lookup"><span data-stu-id="814b6-154">The number of coordinates required for src0 to perform the texture sample depends on how src1 was declared, plus the .w component.</span></span> <span data-ttu-id="814b6-155">Les types d’échantillonneur sont déclarés avec le [ \_ samplerType DCL (SM2, SM3-PS ASM)](dcl-samplertype---ps.md).</span><span class="sxs-lookup"><span data-stu-id="814b6-155">Sampler types are declared with [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md).</span></span> <span data-ttu-id="814b6-156">Si src1 est déclaré comme un échantillonneur 2D, src0 doit contenir des coordonnées. XYW ; Si src1 est déclaré comme un échantillonneur de cube ou un échantillonneur de volume, src0 doit contenir des coordonnées. XYZW.</span><span class="sxs-lookup"><span data-stu-id="814b6-156">If src1 is declared as a 2D sampler, then src0 must contain .xyw coordinates; if src1 is declared as either a cube sampler or a volume sampler, then src0 must contain .xyzw coordinates.</span></span> <span data-ttu-id="814b6-157">L’échantillonnage d’une texture 2D avec des coordonnées. XYZW est autorisé (la coordonnée z est ignorée).</span><span class="sxs-lookup"><span data-stu-id="814b6-157">Sampling a 2D texture with .xyzw coordinates is allowed (the .z coordinate is ignored).</span></span>

<span data-ttu-id="814b6-158">Si la texture source contient moins de quatre composants, les valeurs par défaut sont placées dans les composants manquants.</span><span class="sxs-lookup"><span data-stu-id="814b6-158">If the source texture contains fewer than four components, defaults are placed in the missing components.</span></span> <span data-ttu-id="814b6-159">Les valeurs par défaut dépendent du format de texture, comme indiqué dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="814b6-159">Defaults depend on the texture format as shown in the following table:</span></span>



| <span data-ttu-id="814b6-160">Format de texture</span><span class="sxs-lookup"><span data-stu-id="814b6-160">Texture Format</span></span>                                                                                          | <span data-ttu-id="814b6-161">Valeurs par défaut</span><span class="sxs-lookup"><span data-stu-id="814b6-161">Default Values</span></span>       |
|---------------------------------------------------------------------------------------------------------|----------------------|
| <span data-ttu-id="814b6-162">D3DFMT \_ R5G6B5, D3DFMT \_ R8G8B8, D3DFMT \_ L8, D3DFMT \_ L16, D3DFMT \_ R3G3B2, D3DFMT \_ CxV8U8, D3DFMT \_ L6V5U5</span><span class="sxs-lookup"><span data-stu-id="814b6-162">D3DFMT\_R5G6B5, D3DFMT\_R8G8B8, D3DFMT\_L8, D3DFMT\_L16, D3DFMT\_R3G3B2, D3DFMT\_CxV8U8, D3DFMT\_L6V5U5</span></span> | <span data-ttu-id="814b6-163">A = 1,0</span><span class="sxs-lookup"><span data-stu-id="814b6-163">A = 1.0</span></span>              |
| <span data-ttu-id="814b6-164">D3DFMT \_ V8U8, D3DFMT \_ V16U16, D3DFMT \_ G16R16, D3DFMT \_ G16R16F, D3DFMT \_ G32R32F</span><span class="sxs-lookup"><span data-stu-id="814b6-164">D3DFMT\_V8U8, D3DFMT\_V16U16, D3DFMT\_G16R16, D3DFMT\_G16R16F, D3DFMT\_G32R32F</span></span>                          | <span data-ttu-id="814b6-165">B = A = 1,0</span><span class="sxs-lookup"><span data-stu-id="814b6-165">B = A = 1.0</span></span>          |
| <span data-ttu-id="814b6-166">D3DFMT \_ a8</span><span class="sxs-lookup"><span data-stu-id="814b6-166">D3DFMT\_A8</span></span>                                                                                              | <span data-ttu-id="814b6-167">R = G = B = 0,0</span><span class="sxs-lookup"><span data-stu-id="814b6-167">R = G = B = 0.0</span></span>      |
| <span data-ttu-id="814b6-168">D3DFMT \_ R16F, D3DFMT \_ R32F</span><span class="sxs-lookup"><span data-stu-id="814b6-168">D3DFMT\_R16F, D3DFMT\_R32F</span></span>                                                                              | <span data-ttu-id="814b6-169">G = B = A = 1,0</span><span class="sxs-lookup"><span data-stu-id="814b6-169">G = B = A = 1.0</span></span>      |
| <span data-ttu-id="814b6-170">Tous les formats de profondeur/gabarit</span><span class="sxs-lookup"><span data-stu-id="814b6-170">All depth/stencil formats</span></span>                                                                               | <span data-ttu-id="814b6-171">R = B = 0,0, A = 1,0</span><span class="sxs-lookup"><span data-stu-id="814b6-171">R = B = 0.0, A = 1.0</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="814b6-172">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="814b6-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="814b6-173">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="814b6-173">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 