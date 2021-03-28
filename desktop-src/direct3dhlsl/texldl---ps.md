---
title: texldl-PS
description: Échantillonner une texture avec un échantillonneur particulier. Le niveau de détail mipmap spécifique échantillonné doit être spécifié en tant que quatrième composant de la coordonnée de texture. | texldl-PS
ms.assetid: f0ca8a1d-ac98-49ef-850a-c534e986c7ac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a6ab8a6f55ce5e069a01edb5d281bfe506c5fee6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104973942"
---
# <a name="texldl---ps"></a><span data-ttu-id="c62ff-105">texldl-PS</span><span class="sxs-lookup"><span data-stu-id="c62ff-105">texldl - ps</span></span>

<span data-ttu-id="c62ff-106">Échantillonner une texture avec un échantillonneur particulier.</span><span class="sxs-lookup"><span data-stu-id="c62ff-106">Sample a texture with a particular sampler.</span></span> <span data-ttu-id="c62ff-107">Le niveau de détail mipmap spécifique échantillonné doit être spécifié en tant que quatrième composant de la coordonnée de texture.</span><span class="sxs-lookup"><span data-stu-id="c62ff-107">The particular mipmap level-of-detail being sampled has to be specified as the fourth component of the texture coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="c62ff-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c62ff-108">Syntax</span></span>



| <span data-ttu-id="c62ff-109">texldl DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="c62ff-109">texldl dst, src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="c62ff-110">Où :</span><span class="sxs-lookup"><span data-stu-id="c62ff-110">Where:</span></span>

-   <span data-ttu-id="c62ff-111">l’heure d’été est un registre de destination.</span><span class="sxs-lookup"><span data-stu-id="c62ff-111">dst is a destination register.</span></span>
-   <span data-ttu-id="c62ff-112">src0 est un registre source qui fournit les coordonnées de texture pour l’échantillon de texture.</span><span class="sxs-lookup"><span data-stu-id="c62ff-112">src0 is a source register that provides the texture coordinates for the texture sample.</span></span> <span data-ttu-id="c62ff-113">Consultez [Registre de coordonnées de texture](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span><span class="sxs-lookup"><span data-stu-id="c62ff-113">See [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span></span>
-   <span data-ttu-id="c62ff-114">src1 identifie le ou les registres de l’échantillonneur \# de source, où \# spécifie le numéro d’échantillonnage de texture à échantillonner.</span><span class="sxs-lookup"><span data-stu-id="c62ff-114">src1 identifies the source sampler register (s\#), where \# specifies which texture sampler number to sample.</span></span> <span data-ttu-id="c62ff-115">L’échantillonneur s’est associé à une texture et à un état de contrôle défini par l’énumération [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) (par exemple, D3DSAMP \_ MINFILTER).</span><span class="sxs-lookup"><span data-stu-id="c62ff-115">The sampler has associated with it a texture and a control state defined by the [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) enumeration (for example, D3DSAMP\_MINFILTER).</span></span>

## <a name="remarks"></a><span data-ttu-id="c62ff-116">Notes</span><span class="sxs-lookup"><span data-stu-id="c62ff-116">Remarks</span></span>



| <span data-ttu-id="c62ff-117">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="c62ff-117">Pixel shader versions</span></span> | <span data-ttu-id="c62ff-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="c62ff-118">1\_1</span></span> | <span data-ttu-id="c62ff-119">1\_2</span><span class="sxs-lookup"><span data-stu-id="c62ff-119">1\_2</span></span> | <span data-ttu-id="c62ff-120">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="c62ff-120">1\_3</span></span> | <span data-ttu-id="c62ff-121">1\_4</span><span class="sxs-lookup"><span data-stu-id="c62ff-121">1\_4</span></span> | <span data-ttu-id="c62ff-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c62ff-122">2\_0</span></span> | <span data-ttu-id="c62ff-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c62ff-123">2\_x</span></span> | <span data-ttu-id="c62ff-124">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="c62ff-124">2\_sw</span></span> | <span data-ttu-id="c62ff-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c62ff-125">3\_0</span></span> | <span data-ttu-id="c62ff-126">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="c62ff-126">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="c62ff-127">texldl</span><span class="sxs-lookup"><span data-stu-id="c62ff-127">texldl</span></span>                |      |      |      |      |      |      |       | <span data-ttu-id="c62ff-128">x</span><span class="sxs-lookup"><span data-stu-id="c62ff-128">x</span></span>    | <span data-ttu-id="c62ff-129">x</span><span class="sxs-lookup"><span data-stu-id="c62ff-129">x</span></span>     |



 

<span data-ttu-id="c62ff-130">texldl recherche la texture définie à l’étape d’échantillonnage référencée par src1.</span><span class="sxs-lookup"><span data-stu-id="c62ff-130">texldl looks up the texture set at the sampler stage referenced by src1.</span></span> <span data-ttu-id="c62ff-131">Le niveau de détail est sélectionné dans src0. w.</span><span class="sxs-lookup"><span data-stu-id="c62ff-131">The level-of-detail is selected from src0.w.</span></span> <span data-ttu-id="c62ff-132">Cette valeur peut être négative dans le cas où le niveau de détail sélectionné est le avant toute chose (le plus grand mappage) avec le MAGFILTER.</span><span class="sxs-lookup"><span data-stu-id="c62ff-132">This value can be negative in which case the level-of-detail selected is the zeroth one (biggest map) with the MAGFILTER.</span></span> <span data-ttu-id="c62ff-133">Étant donné que src0. w est une valeur à virgule flottante, la valeur fractionnaire est utilisée pour interpoler (si MIPFILTER est linéaire) entre deux niveaux MIP.</span><span class="sxs-lookup"><span data-stu-id="c62ff-133">Since src0.w is a floating point value, the fractional value is used to interpolate (if MIPFILTER is LINEAR) between two mip levels.</span></span> <span data-ttu-id="c62ff-134">Les États de l’échantillonneur MIPMAPLODBIAS et MAXMIPLEVEL sont honorés.</span><span class="sxs-lookup"><span data-stu-id="c62ff-134">Sampler states MIPMAPLODBIAS and MAXMIPLEVEL are honored.</span></span> <span data-ttu-id="c62ff-135">Pour plus d’informations sur les États de l’échantillonneur, consultez [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span><span class="sxs-lookup"><span data-stu-id="c62ff-135">For more information about sampler states, see [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span></span>

<span data-ttu-id="c62ff-136">Si un programme de nuanceur échantillonne à partir d’un échantillonneur qui n’a pas de texture définie, 0001 est obtenu dans le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="c62ff-136">If a shader program samples from a sampler that does not have a texture set, then 0001 is obtained in the destination register.</span></span>

<span data-ttu-id="c62ff-137">Voici un algorithme approximatif que suit l’appareil de référence :</span><span class="sxs-lookup"><span data-stu-id="c62ff-137">The following is a rough algorithm that the reference device follows:</span></span>


```
LOD = src0.w + LODBIAS;
if (LOD <= 0 )
{
   LOD = 0;
   Filter = MagFilter;
   tex = Lookup( MAX(MAXMIPLEVEL, LOD), Filter );
}
else
{
   Filter = MinFilter;
   LOD = MAX( MAXMIPLEVEL, LOD );
   tex = Lookup( Floor(LOD), Filter );
   if( MipFilter == LINEAR )
   {
      tex1 = Lookup( Ceil(LOD), Filter );                        
      tex = (1 - frac(src0.w))*tex + frac(src0.w)*tex1;
   }
}
```



<span data-ttu-id="c62ff-138">Restrictions :</span><span class="sxs-lookup"><span data-stu-id="c62ff-138">Restrictions:</span></span>

-   <span data-ttu-id="c62ff-139">Les coordonnées de texture ne doivent pas être mises à l’échelle par taille de texture.</span><span class="sxs-lookup"><span data-stu-id="c62ff-139">The texture coordinates should not be scaled by texture size.</span></span>
-   <span data-ttu-id="c62ff-140">l’heure d’été doit être un [Registre temporaire](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).</span><span class="sxs-lookup"><span data-stu-id="c62ff-140">dst must be a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#).</span></span>
-   <span data-ttu-id="c62ff-141">l’heure d’été peut accepter un writemask.</span><span class="sxs-lookup"><span data-stu-id="c62ff-141">dst can accept a writemask.</span></span> <span data-ttu-id="c62ff-142">Voir [masque d’écriture de registre de destination](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span><span class="sxs-lookup"><span data-stu-id="c62ff-142">See [Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span></span>
-   <span data-ttu-id="c62ff-143">Les valeurs par défaut pour les composants manquants sont 0 ou 1 et dépendent du format de texture.</span><span class="sxs-lookup"><span data-stu-id="c62ff-143">Defaults for missing components are either 0 or 1, and depend on the texture format.</span></span>
-   <span data-ttu-id="c62ff-144">src1 doit être un [échantillonneur (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# .</span><span class="sxs-lookup"><span data-stu-id="c62ff-144">src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#).</span></span> <span data-ttu-id="c62ff-145">src1 ne peut pas utiliser de modificateur de négation (voir [masque d’écriture de registre de destination](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)).</span><span class="sxs-lookup"><span data-stu-id="c62ff-145">src1 may not use a negate modifier (see [Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)).</span></span> <span data-ttu-id="c62ff-146">src1 peut utiliser Swizzle (voir [Registre source Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md)), qui est appliqué après l’échantillonnage, mais avant le masque d’écriture (voir masque d’écriture de registre de destination) est respecté.</span><span class="sxs-lookup"><span data-stu-id="c62ff-146">src1 may use swizzle (see [Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md)), which is applied after sampling, but before the write mask (see Destination Register Write Mask) is honored.</span></span> <span data-ttu-id="c62ff-147">L’échantillonneur doit avoir été déclaré (à l’aide de la [ \_ samplerType DCL (SM2, SM3-PS ASM)](dcl-samplertype---ps.md)) au début du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="c62ff-147">The sampler must have been declared (using [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md)) at the beginning of the shader.</span></span>
-   <span data-ttu-id="c62ff-148">Le nombre de coordonnées requises pour exécuter l’exemple de texture dépend de la façon dont l’échantillonneur a été déclaré.</span><span class="sxs-lookup"><span data-stu-id="c62ff-148">The number of coordinates required to perform the texture sample depends on how the sampler was declared.</span></span> <span data-ttu-id="c62ff-149">Si elle a été déclarée en tant que cube, une coordonnée de texture à trois composants est requise (. RGB).</span><span class="sxs-lookup"><span data-stu-id="c62ff-149">If it was declared as a cube, a three-component texture coordinate is required (.rgb).</span></span> <span data-ttu-id="c62ff-150">La validation garantit que les coordonnées fournies pour Tex \_ LDL sont suffisantes pour la dimension de texture déclarée pour l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="c62ff-150">Validation enforces that coordinates provided to tex\_ldl Are sufficient for the texture dimension declared for the sampler.</span></span> <span data-ttu-id="c62ff-151">Toutefois, il n’est pas garanti que l’application définit en fait une texture (via l’API) dont les dimensions sont égales à la dimension déclarée pour l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="c62ff-151">However, it is not guaranteed that the application actually sets a texture (through the API) with dimensions equal to the dimension declared for the sampler.</span></span> <span data-ttu-id="c62ff-152">Dans ce cas, le runtime tente de détecter les incompatibilités (éventuellement en débogage uniquement).</span><span class="sxs-lookup"><span data-stu-id="c62ff-152">In such a case, the runtime will attempt to detect mismatches (possibly in debug only).</span></span> <span data-ttu-id="c62ff-153">L’échantillonnage d’une texture avec moins de dimensions que celles présentes dans la coordonnée de texture sera autorisé et supposé ignorer les composants de coordonnée de texture supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="c62ff-153">Sampling a texture with fewer dimensions than are present in the texture coordinate will be allowed and assumed to ignore the extra texture coordinate components.</span></span> <span data-ttu-id="c62ff-154">Inversement, l’échantillonnage d’une texture avec plus de dimensions que celles présentes dans la coordonnée de texture n’est pas conforme.</span><span class="sxs-lookup"><span data-stu-id="c62ff-154">Conversely, sampling a texture with more dimensions than are present in the texture coordinate is illegal.</span></span>
-   <span data-ttu-id="c62ff-155">Si le src0 (coordonnée de texture) est un [Registre temporaire](dx9-graphics-reference-asm-ps-registers-temporary.md), les composants requis pour la recherche (décrite ci-dessus) doivent avoir été préalablement écrits.</span><span class="sxs-lookup"><span data-stu-id="c62ff-155">If the src0 (texture coordinate) is [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md), the components required for the lookup (described above) must have been previously written.</span></span>
-   <span data-ttu-id="c62ff-156">Les textures RVB non signées d’échantillonnage entraînent des valeurs float comprises entre 0,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="c62ff-156">Sampling unsigned RGB textures will result in float values between 0.0 and 1.0.</span></span>
-   <span data-ttu-id="c62ff-157">L’échantillonnage des textures signées entraîne des valeurs float comprises entre-1,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="c62ff-157">Sampling signed textures will result in float values between -1.0 to 1.0.</span></span>
-   <span data-ttu-id="c62ff-158">Lors de l’échantillonnage de textures à virgule flottante, Float16 signifie que les données seront comprises dans le \_ FLOAT16 maximal.</span><span class="sxs-lookup"><span data-stu-id="c62ff-158">When sampling floating-point textures, Float16 means that the data will range within MAX\_FLOAT16.</span></span> <span data-ttu-id="c62ff-159">Float32 signifie que la plage maximale du pipeline sera utilisée.</span><span class="sxs-lookup"><span data-stu-id="c62ff-159">Float32 means the maximum range of the pipeline will be used.</span></span> <span data-ttu-id="c62ff-160">L’échantillonnage en dehors de l’une des limites n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="c62ff-160">Sampling outside of either range is undefined.</span></span>
-   <span data-ttu-id="c62ff-161">Il n’existe aucune limite de lecture dépendante.</span><span class="sxs-lookup"><span data-stu-id="c62ff-161">There is no dependent read limit.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c62ff-162">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c62ff-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c62ff-163">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="c62ff-163">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 
