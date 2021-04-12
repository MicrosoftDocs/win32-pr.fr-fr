---
title: texldp-PS
description: Instruction de chargement de texture projetée. Cette instruction divise la coordonnée de texture d’entrée par le quatrième élément (. a ou. w) juste avant l’échantillonnage.
ms.assetid: 82e62ba3-a9f5-4afb-8dca-4c54a00843eb
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 045caf6ec922183893df252488946546602d2459
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316392"
---
# <a name="texldp---ps"></a><span data-ttu-id="abcd7-104">texldp-PS</span><span class="sxs-lookup"><span data-stu-id="abcd7-104">texldp - ps</span></span>

<span data-ttu-id="abcd7-105">Instruction de chargement de texture projetée.</span><span class="sxs-lookup"><span data-stu-id="abcd7-105">Projected texture load instruction.</span></span> <span data-ttu-id="abcd7-106">Cette instruction divise la coordonnée de texture d’entrée par le quatrième élément (. a ou. w) juste avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="abcd7-106">This instruction divides the input texture coordinate by the fourth element (.a or .w) just before sampling.</span></span>

## <a name="syntax"></a><span data-ttu-id="abcd7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="abcd7-107">Syntax</span></span>



| <span data-ttu-id="abcd7-108">texldp DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="abcd7-108">texldp dst, src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="abcd7-109">where</span><span class="sxs-lookup"><span data-stu-id="abcd7-109">where</span></span>

-   <span data-ttu-id="abcd7-110">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="abcd7-110">dst is the destination register.</span></span>
-   <span data-ttu-id="abcd7-111">src0 est un registre source qui fournit les coordonnées de texture pour l’échantillon de texture.</span><span class="sxs-lookup"><span data-stu-id="abcd7-111">src0 is a source register that provides the texture coordinates for the texture sample.</span></span> <span data-ttu-id="abcd7-112">Consultez [Registre de coordonnées de texture](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span><span class="sxs-lookup"><span data-stu-id="abcd7-112">See [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span></span>
-   <span data-ttu-id="abcd7-113">src1 identifie l' [échantillonneur (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# , où \# spécifie le numéro d’échantillonnage de texture à échantillonner.</span><span class="sxs-lookup"><span data-stu-id="abcd7-113">src1 identifies the [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), where \# specifies which texture sampler number to sample.</span></span> <span data-ttu-id="abcd7-114">L’échantillonneur lui est associé une texture et un état d’échantillonneur défini par [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span><span class="sxs-lookup"><span data-stu-id="abcd7-114">The sampler has associated with it a texture and a sampler state defined by [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span></span>

<span data-ttu-id="abcd7-115">Pour obtenir le jeu de restrictions lors de l’utilisation de texldp, consultez [texld](texld---ps-2-0.md).</span><span class="sxs-lookup"><span data-stu-id="abcd7-115">For the set of restrictions when using texldp, see [texld](texld---ps-2-0.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="abcd7-116">Notes</span><span class="sxs-lookup"><span data-stu-id="abcd7-116">Remarks</span></span>

<span data-ttu-id="abcd7-117">texldp effectue la projection sur les coordonnées lues à partir de src0 avant d’effectuer l’exemple.</span><span class="sxs-lookup"><span data-stu-id="abcd7-117">texldp performs projection on the coordinates read from src0 before performing the sample.</span></span> <span data-ttu-id="abcd7-118">Chaque coordonnée de texture est divisée par src0. w, puis la texture est échantillonnée.</span><span class="sxs-lookup"><span data-stu-id="abcd7-118">Each texture coordinate is divided by src0.w, then the texture is sampled.</span></span> <span data-ttu-id="abcd7-119">Quand texldp se termine, le contenu de src0 n’est pas affecté (sauf si l’heure d’été est le même registre).</span><span class="sxs-lookup"><span data-stu-id="abcd7-119">When texldp completes, the contents of src0 are unaffected (unless dst is the same register).</span></span> <span data-ttu-id="abcd7-120">Une alternative à l’utilisation de texldp consiste à effectuer manuellement la Division de projection dans le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="abcd7-120">An alternative to using texldp is to manually perform the projection division in the shader.</span></span> <span data-ttu-id="abcd7-121">Toutefois, l’exécution de la division dans le code du nuanceur est généralement plus lente que lorsqu’elle est exécutée par l’instruction texldp. par conséquent, évitez de tels calculs supplémentaires lorsque cela est possible.</span><span class="sxs-lookup"><span data-stu-id="abcd7-121">However, performing the division in shader code is usually slower than when performed by the texldp instruction, so avoid such additional math when possible.</span></span>

<span data-ttu-id="abcd7-122">Le nombre de coordonnées nécessaires à l’exécution de l’exemple de texture par src0 dépend de la manière dont src1 a été déclaré, plus le composant. w.</span><span class="sxs-lookup"><span data-stu-id="abcd7-122">The number of coordinates required for src0 to perform the texture sample depends on how src1 was declared, plus the .w component.</span></span> <span data-ttu-id="abcd7-123">Les types d’échantillonneur sont déclarés avec le [ \_ samplerType DCL (SM2, SM3-PS ASM)](dcl-samplertype---ps.md).</span><span class="sxs-lookup"><span data-stu-id="abcd7-123">Sampler types are declared with [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md).</span></span> <span data-ttu-id="abcd7-124">Si src1 est déclaré comme un échantillonneur 2D, src0 doit contenir des coordonnées. XYW ; Si src1 est déclaré comme un échantillonneur de cube ou un échantillonneur de volume, src0 doit contenir des coordonnées. XYZW.</span><span class="sxs-lookup"><span data-stu-id="abcd7-124">If src1 is declared as a 2D sampler, then src0 must contain .xyw coordinates; if src1 is declared as either a cube sampler or a volume sampler, then src0 must contain .xyzw coordinates.</span></span> <span data-ttu-id="abcd7-125">L’échantillonnage d’une texture 2D avec des coordonnées. XYZW est autorisé (la coordonnée z est ignorée).</span><span class="sxs-lookup"><span data-stu-id="abcd7-125">Sampling a 2D texture with .xyzw coordinates is allowed (the .z coordinate is ignored).</span></span>

<span data-ttu-id="abcd7-126">Si la texture source contient moins de quatre composants, les valeurs par défaut sont placées dans les composants manquants.</span><span class="sxs-lookup"><span data-stu-id="abcd7-126">If the source texture contains fewer than four components, defaults are placed in the missing components.</span></span> <span data-ttu-id="abcd7-127">Les valeurs par défaut dépendent du format de texture, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="abcd7-127">Defaults depend on the texture format as shown in the following table.</span></span>



| <span data-ttu-id="abcd7-128">Format de texture</span><span class="sxs-lookup"><span data-stu-id="abcd7-128">Texture Format</span></span>                                                                                          | <span data-ttu-id="abcd7-129">Valeurs par défaut pour les composants manquants</span><span class="sxs-lookup"><span data-stu-id="abcd7-129">Default Values for missing components</span></span> |
|---------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span data-ttu-id="abcd7-130">D3DFMT \_ R5G6B5, D3DFMT \_ R8G8B8, D3DFMT \_ L8, D3DFMT \_ L16, D3DFMT \_ R3G3B2, D3DFMT \_ CxV8U8, D3DFMT \_ L6V5U5</span><span class="sxs-lookup"><span data-stu-id="abcd7-130">D3DFMT\_R5G6B5, D3DFMT\_R8G8B8, D3DFMT\_L8, D3DFMT\_L16, D3DFMT\_R3G3B2, D3DFMT\_CxV8U8, D3DFMT\_L6V5U5</span></span> | <span data-ttu-id="abcd7-131">A = 1,0</span><span class="sxs-lookup"><span data-stu-id="abcd7-131">A = 1.0</span></span>                               |
| <span data-ttu-id="abcd7-132">D3DFMT \_ V8U8, D3DFMT \_ V16U16, D3DFMT \_ G16R16, D3DFMT \_ G16R16F, D3DFMT \_ G32R32F</span><span class="sxs-lookup"><span data-stu-id="abcd7-132">D3DFMT\_V8U8, D3DFMT\_V16U16, D3DFMT\_G16R16, D3DFMT\_G16R16F, D3DFMT\_G32R32F</span></span>                          | <span data-ttu-id="abcd7-133">B = A = 1,0</span><span class="sxs-lookup"><span data-stu-id="abcd7-133">B = A = 1.0</span></span>                           |
| <span data-ttu-id="abcd7-134">D3DFMT \_ a8</span><span class="sxs-lookup"><span data-stu-id="abcd7-134">D3DFMT\_A8</span></span>                                                                                              | <span data-ttu-id="abcd7-135">R = G = B = 0,0</span><span class="sxs-lookup"><span data-stu-id="abcd7-135">R = G = B = 0.0</span></span>                       |
| <span data-ttu-id="abcd7-136">D3DFMT \_ R16F, D3DFMT \_ R32F</span><span class="sxs-lookup"><span data-stu-id="abcd7-136">D3DFMT\_R16F, D3DFMT\_R32F</span></span>                                                                              | <span data-ttu-id="abcd7-137">G = B = A = 1,0</span><span class="sxs-lookup"><span data-stu-id="abcd7-137">G = B = A = 1.0</span></span>                       |
| <span data-ttu-id="abcd7-138">Tous les formats de profondeur/gabarit</span><span class="sxs-lookup"><span data-stu-id="abcd7-138">All depth/stencil formats</span></span>                                                                               | <span data-ttu-id="abcd7-139">R = B = 0,0, A = 1,0</span><span class="sxs-lookup"><span data-stu-id="abcd7-139">R = B = 0.0, A = 1.0</span></span>                  |



 

<span data-ttu-id="abcd7-140">Cette instruction est prise en charge dans les versions suivantes :</span><span class="sxs-lookup"><span data-stu-id="abcd7-140">This instruction is supported in the following versions:</span></span>



| <span data-ttu-id="abcd7-141">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="abcd7-141">Pixel shader versions</span></span> | <span data-ttu-id="abcd7-142">1\_1</span><span class="sxs-lookup"><span data-stu-id="abcd7-142">1\_1</span></span> | <span data-ttu-id="abcd7-143">1\_2</span><span class="sxs-lookup"><span data-stu-id="abcd7-143">1\_2</span></span> | <span data-ttu-id="abcd7-144">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="abcd7-144">1\_3</span></span> | <span data-ttu-id="abcd7-145">1\_4</span><span class="sxs-lookup"><span data-stu-id="abcd7-145">1\_4</span></span> | <span data-ttu-id="abcd7-146">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="abcd7-146">2\_0</span></span> | <span data-ttu-id="abcd7-147">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="abcd7-147">2\_x</span></span> | <span data-ttu-id="abcd7-148">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="abcd7-148">2\_sw</span></span> | <span data-ttu-id="abcd7-149">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="abcd7-149">3\_0</span></span> | <span data-ttu-id="abcd7-150">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="abcd7-150">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="abcd7-151">texldp</span><span class="sxs-lookup"><span data-stu-id="abcd7-151">texldp</span></span>                |      |      |      |      | <span data-ttu-id="abcd7-152">x</span><span class="sxs-lookup"><span data-stu-id="abcd7-152">x</span></span>    | <span data-ttu-id="abcd7-153">x</span><span class="sxs-lookup"><span data-stu-id="abcd7-153">x</span></span>    | <span data-ttu-id="abcd7-154">x</span><span class="sxs-lookup"><span data-stu-id="abcd7-154">x</span></span>     | <span data-ttu-id="abcd7-155">x</span><span class="sxs-lookup"><span data-stu-id="abcd7-155">x</span></span>    | <span data-ttu-id="abcd7-156">x</span><span class="sxs-lookup"><span data-stu-id="abcd7-156">x</span></span>     |



 

### <a name="ps_2_0-and-ps_2_x"></a><span data-ttu-id="abcd7-157">PS \_ 2 \_ 0 et PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="abcd7-157">ps\_2\_0 and ps\_2\_x</span></span>

<span data-ttu-id="abcd7-158">l’heure d’été doit être un [Registre temporaire](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) et seul le masque XYZW (masque par défaut) est autorisé.</span><span class="sxs-lookup"><span data-stu-id="abcd7-158">dst must be a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) and only .xyzw mask (default mask) is allowed.</span></span>

<span data-ttu-id="abcd7-159">src0 doit être un [Registre de coordonnées de texture](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t \# ) ou un [Registre temporaire](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ), sans modificateur ni Swizzle.</span><span class="sxs-lookup"><span data-stu-id="abcd7-159">src0 must be either a [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t\#) or a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#), with no modifier or swizzle.</span></span>

<span data-ttu-id="abcd7-160">src1 doit être un [échantillonneur (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) , sans \# modificateur ni Swizzle.</span><span class="sxs-lookup"><span data-stu-id="abcd7-160">src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), with no modifier or swizzle.</span></span>

<span data-ttu-id="abcd7-161">Si le \_ \_ bit d’extrémité D3DD3DPSHADERCAPS2 0 NODEPENDENTREADLIMIT n’est pas défini (dans D3DPSHADERCAPS2 \_ 0), une instruction de texture donnée ([texld](texld---ps-1-4.md), texldp, [texldb-PS](texldb---ps.md), [texldd](texldd---ps.md) ) peut dépendre, au plus, du troisième ordre.</span><span class="sxs-lookup"><span data-stu-id="abcd7-161">If the D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT cap bit is not set (in D3DPSHADERCAPS2\_0), a given texture instruction ([texld](texld---ps-1-4.md), texldp, [texldb - ps](texldb---ps.md), [texldd](texldd---ps.md) ) may be dependent upon, at most, third order.</span></span> <span data-ttu-id="abcd7-162">Une instruction de texture dépendante de premier ordre est une instruction de texture dans laquelle :</span><span class="sxs-lookup"><span data-stu-id="abcd7-162">A first-order dependent texture instruction is a texture instruction in which either:</span></span>

-   <span data-ttu-id="abcd7-163">src0 est un [Registre temporaire](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# )</span><span class="sxs-lookup"><span data-stu-id="abcd7-163">src0 is a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#)</span></span>
-   <span data-ttu-id="abcd7-164">l’heure d’été a été écrite précédemment, en cours de réécriture.</span><span class="sxs-lookup"><span data-stu-id="abcd7-164">dst was previously written, now being written again.</span></span>

<span data-ttu-id="abcd7-165">Une instruction de texture dépendante d’une seconde commande est définie comme une instruction de texture qui lit ou écrit dans un [Registre temporaire](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) dont le contenu, avant d’exécuter l’instruction de texture, dépend (peut-être indirectement) du résultat d’une instruction de texture dépendante de premier ordre.</span><span class="sxs-lookup"><span data-stu-id="abcd7-165">A second-order dependent texture instruction is defined as a texture instruction that reads or writes to a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) whose contents, before executing the texture instruction, depend (perhaps indirectly) on the outcome of a first-order dependent texture instruction.</span></span> <span data-ttu-id="abcd7-166">Une instruction de texture dépendante (n)<sup>th</sup>dérive d’une instruction de texture (n-1)<sup>th</sup>-Order.</span><span class="sxs-lookup"><span data-stu-id="abcd7-166">An (n)<sup>th</sup>-order dependent texture instruction derives from an (n - 1)<sup>th</sup>-order texture instruction.</span></span>

### <a name="ps_3_0"></a><span data-ttu-id="abcd7-167">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="abcd7-167">ps\_3\_0</span></span>

<span data-ttu-id="abcd7-168">Pour PS \_ 3 \_ 0, src1 doit être un [échantillonneur (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) , sans \# modificateur.</span><span class="sxs-lookup"><span data-stu-id="abcd7-168">For ps\_3\_0, src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), with no modifier.</span></span> <span data-ttu-id="abcd7-169">Swizzle est autorisé sur src1 et, lorsqu’il est appliqué, les résultats de la recherche de texture sont antérieurs à swizzled avant d’être écrits dans l’heure d’été.</span><span class="sxs-lookup"><span data-stu-id="abcd7-169">Swizzle is allowed on src1, and when applied, the texture lookup results are pre-swizzled before written to dst.</span></span>

## <a name="related-topics"></a><span data-ttu-id="abcd7-170">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="abcd7-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="abcd7-171">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="abcd7-171">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 