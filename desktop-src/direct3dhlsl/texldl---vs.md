---
title: texldl-vs
description: Échantillonner une texture avec un échantillonneur particulier. Le niveau de détail mipmap spécifique échantillonné doit être spécifié en tant que quatrième composant de la coordonnée de texture. | texldl-vs
ms.assetid: 774c058d-7b3e-46a9-adce-c9a44efefd78
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: be9240f5307bb1e70b1f10cc1e392b92e5833fd8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104043016"
---
# <a name="texldl---vs"></a><span data-ttu-id="aa3ed-105">texldl-vs</span><span class="sxs-lookup"><span data-stu-id="aa3ed-105">texldl - vs</span></span>

<span data-ttu-id="aa3ed-106">Échantillonner une texture avec un échantillonneur particulier.</span><span class="sxs-lookup"><span data-stu-id="aa3ed-106">Sample a texture with a particular sampler.</span></span> <span data-ttu-id="aa3ed-107">Le niveau de détail mipmap spécifique échantillonné doit être spécifié en tant que quatrième composant de la coordonnée de texture.</span><span class="sxs-lookup"><span data-stu-id="aa3ed-107">The particular mipmap level-of-detail being sampled has to be specified as the fourth component of the texture coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa3ed-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aa3ed-108">Syntax</span></span>



| <span data-ttu-id="aa3ed-109">texldl DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="aa3ed-109">texldl dst, src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="aa3ed-110">Où :</span><span class="sxs-lookup"><span data-stu-id="aa3ed-110">Where:</span></span>

-   <span data-ttu-id="aa3ed-111">l’heure d’été est un registre de destination.</span><span class="sxs-lookup"><span data-stu-id="aa3ed-111">dst is a destination register.</span></span>
-   <span data-ttu-id="aa3ed-112">src0 est un registre source qui fournit les coordonnées de texture pour l’échantillon de texture.</span><span class="sxs-lookup"><span data-stu-id="aa3ed-112">src0 is a source register that provides the texture coordinates for the texture sample.</span></span>
-   <span data-ttu-id="aa3ed-113">src1 identifie le ou les registres de l’échantillonneur \# de source, où \# spécifie le numéro d’échantillonnage de texture à échantillonner.</span><span class="sxs-lookup"><span data-stu-id="aa3ed-113">src1 identifies the source sampler register (s\#), where \# specifies which texture sampler number to sample.</span></span> <span data-ttu-id="aa3ed-114">L’échantillonneur s’est associé à une texture et à un état de contrôle défini par l’énumération [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) (par exemple, D3DSAMP \_ MINFILTER).</span><span class="sxs-lookup"><span data-stu-id="aa3ed-114">The sampler has associated with it a texture and a control state defined by the [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) enumeration (for example, D3DSAMP\_MINFILTER).</span></span>

## <a name="remarks"></a><span data-ttu-id="aa3ed-115">Notes</span><span class="sxs-lookup"><span data-stu-id="aa3ed-115">Remarks</span></span>



| <span data-ttu-id="aa3ed-116">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="aa3ed-116">Vertex shader versions</span></span> | <span data-ttu-id="aa3ed-117">1\_1</span><span class="sxs-lookup"><span data-stu-id="aa3ed-117">1\_1</span></span> | <span data-ttu-id="aa3ed-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="aa3ed-118">2\_0</span></span> | <span data-ttu-id="aa3ed-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="aa3ed-119">2\_x</span></span> | <span data-ttu-id="aa3ed-120">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="aa3ed-120">2\_sw</span></span> | <span data-ttu-id="aa3ed-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="aa3ed-121">3\_0</span></span> | <span data-ttu-id="aa3ed-122">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="aa3ed-122">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="aa3ed-123">texldl</span><span class="sxs-lookup"><span data-stu-id="aa3ed-123">texldl</span></span>                 |      |      |      |       | <span data-ttu-id="aa3ed-124">x</span><span class="sxs-lookup"><span data-stu-id="aa3ed-124">x</span></span>    | <span data-ttu-id="aa3ed-125">x</span><span class="sxs-lookup"><span data-stu-id="aa3ed-125">x</span></span>     |



 

<span data-ttu-id="aa3ed-126">texldl recherche la texture définie à l’étape d’échantillonnage référencée par src1.</span><span class="sxs-lookup"><span data-stu-id="aa3ed-126">texldl looks up the texture set at the sampler stage referenced by src1.</span></span> <span data-ttu-id="aa3ed-127">Le niveau de détail est sélectionné dans src0. w.</span><span class="sxs-lookup"><span data-stu-id="aa3ed-127">The level-of-detail is selected from src0.w.</span></span> <span data-ttu-id="aa3ed-128">Cette valeur peut être négative. dans ce cas, le niveau de détail sélectionné est le « avant toute chose un » (mappage le plus grand) avec le MAGFILTER.</span><span class="sxs-lookup"><span data-stu-id="aa3ed-128">This value can be negative, in which case the level-of-detail selected is the "zeroth one" (biggest map) with the MAGFILTER.</span></span> <span data-ttu-id="aa3ed-129">Comme src0. w est une valeur à virgule flottante, la valeur fractionnaire est utilisée pour interpoler (si MIPFILTER est linéaire) entre deux niveaux MIP.</span><span class="sxs-lookup"><span data-stu-id="aa3ed-129">Because src0.w is a floating point value, the fractional value is used to interpolate (if MIPFILTER is LINEAR) between two mip levels.</span></span> <span data-ttu-id="aa3ed-130">Les États de l’échantillonneur MIPMAPLODBIAS et MAXMIPLEVEL sont honorés.</span><span class="sxs-lookup"><span data-stu-id="aa3ed-130">Sampler states MIPMAPLODBIAS and MAXMIPLEVEL are honored.</span></span> <span data-ttu-id="aa3ed-131">Pour plus d’informations sur les États de l’échantillonneur, consultez [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span><span class="sxs-lookup"><span data-stu-id="aa3ed-131">For more information about sampler states, see [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span></span>

<span data-ttu-id="aa3ed-132">Si un programme Shader échantillonne à partir d’un échantillonneur qui n’a pas de texture définie, 0001 est obtenu dans le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="aa3ed-132">If a shader program samples from a sampler that does not have a texture set, 0001 is obtained in the destination register.</span></span>

<span data-ttu-id="aa3ed-133">Il s’agit d’une approximation de l’algorithme de l’appareil de référence.</span><span class="sxs-lookup"><span data-stu-id="aa3ed-133">This is an approximation to the reference device algorithm.</span></span>


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
   LOD = MAX( MAXMIPLEVEL, LOD);
   tex = Lookup( Floor(LOD), Filter );
   if( MipFilter == LINEAR )
   {
      tex1 = Lookup( Ceil(LOD), Filter );                        
      tex = (1 - frac(src0.w))*tex + frac(src0.w)*tex1;
   }
}
```



<span data-ttu-id="aa3ed-134">Restrictions :</span><span class="sxs-lookup"><span data-stu-id="aa3ed-134">Restrictions:</span></span>

-   <span data-ttu-id="aa3ed-135">Les coordonnées de texture ne doivent pas être mises à l’échelle par taille de texture.</span><span class="sxs-lookup"><span data-stu-id="aa3ed-135">The texture coordinates should not be scaled by texture size.</span></span>
-   <span data-ttu-id="aa3ed-136">l’heure d’été doit être un [Registre temporaire](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ).</span><span class="sxs-lookup"><span data-stu-id="aa3ed-136">dst must be a [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md) (r\#).</span></span>
-   <span data-ttu-id="aa3ed-137">l’heure d’été peut accepter un masque d’écriture.</span><span class="sxs-lookup"><span data-stu-id="aa3ed-137">dst can accept a write mask.</span></span> <span data-ttu-id="aa3ed-138">Consultez [masquage du registre de destination](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md).</span><span class="sxs-lookup"><span data-stu-id="aa3ed-138">See [Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md).</span></span>
-   <span data-ttu-id="aa3ed-139">Les valeurs par défaut pour les composants manquants sont 0 ou 1 et dépendent du format de texture.</span><span class="sxs-lookup"><span data-stu-id="aa3ed-139">Defaults for missing components are either 0 or 1, and depend on the texture format.</span></span>
-   <span data-ttu-id="aa3ed-140">src1 doit être un [échantillonneur (Direct3D 9 ASM-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md) \# .</span><span class="sxs-lookup"><span data-stu-id="aa3ed-140">src1 must be a [Sampler (Direct3D 9 asm-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md) (s\#).</span></span> <span data-ttu-id="aa3ed-141">src1 ne peut pas utiliser de modificateur de négation.</span><span class="sxs-lookup"><span data-stu-id="aa3ed-141">src1 may not use a negate modifier.</span></span> <span data-ttu-id="aa3ed-142">src1 peut utiliser Swizzle, qui est appliqué après l’échantillonnage avant que le masque d’écriture soit respecté.</span><span class="sxs-lookup"><span data-stu-id="aa3ed-142">src1 may use swizzle, which is applied after sampling before the write mask is honored.</span></span> <span data-ttu-id="aa3ed-143">L’échantillonneur doit avoir été déclaré (à l’aide de la [ \_ samplerType DCL (SM3-vs ASM)](dcl-samplertype---vs.md)) au début du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="aa3ed-143">The sampler must have been declared (using [dcl\_samplerType (sm3 - vs asm)](dcl-samplertype---vs.md)) at the beginning of the shader.</span></span>
-   <span data-ttu-id="aa3ed-144">Le nombre de coordonnées requises pour exécuter l’exemple de texture dépend de la façon dont l’échantillonneur a été déclaré.</span><span class="sxs-lookup"><span data-stu-id="aa3ed-144">The number of coordinates required to perform the texture sample depends on how the sampler was declared.</span></span> <span data-ttu-id="aa3ed-145">Si elle a été déclarée en tant que cube, une coordonnée de texture à trois composants est requise (. RGB).</span><span class="sxs-lookup"><span data-stu-id="aa3ed-145">If it was declared as a cube, a three-component texture coordinate is required (.rgb).</span></span> <span data-ttu-id="aa3ed-146">La validation garantit que les coordonnées fournies à texldl sont suffisantes pour la dimension de texture déclarée pour l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="aa3ed-146">Validation enforces that coordinates provided to texldl Are sufficient for the texture dimension declared for the sampler.</span></span> <span data-ttu-id="aa3ed-147">Toutefois, il n’est pas garanti que l’application définit effectivement une texture (via l’API) avec des dimensions égales à la dimension déclarée pour l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="aa3ed-147">However, it is not guaranteed that the application actually set a texture (through the API) with dimensions equal to the dimension declared for the sampler.</span></span> <span data-ttu-id="aa3ed-148">Dans ce cas, le runtime tente de détecter les incompatibilités (éventuellement en débogage uniquement).</span><span class="sxs-lookup"><span data-stu-id="aa3ed-148">In such a case, the runtime will attempt to detect mismatches (possibly in debug only).</span></span> <span data-ttu-id="aa3ed-149">L’échantillonnage d’une texture avec moins de dimensions que celles présentes dans la coordonnée de texture sera autorisé et sera supposé ignorer les composants de coordonnée de texture supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="aa3ed-149">Sampling a texture with fewer dimensions than are present in the texture coordinate will be allowed, and will be assumed to ignore the extra texture coordinate components.</span></span> <span data-ttu-id="aa3ed-150">Inversement, l’échantillonnage d’une texture avec davantage de dimensions que celles présentes dans la coordonnée de texture n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="aa3ed-150">Conversely, sampling a texture with more dimensions than are present in the texture coordinate is not allowed.</span></span>
-   <span data-ttu-id="aa3ed-151">Si le src0 (coordonnée de texture) est un [Registre temporaire](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ), les composants requis pour la recherche (décrite ci-dessus) doivent avoir été préalablement écrits.</span><span class="sxs-lookup"><span data-stu-id="aa3ed-151">If the src0 (texture coordinate) is a [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md) (r\#), the components required for the lookup (described above) must have been previously written.</span></span>
-   <span data-ttu-id="aa3ed-152">Les textures RVB non signées d’échantillonnage entraînent des valeurs float comprises entre 0,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="aa3ed-152">Sampling unsigned RGB textures will result in float values between 0.0 and 1.0.</span></span>
-   <span data-ttu-id="aa3ed-153">L’échantillonnage des textures signées entraîne des valeurs float comprises entre-1,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="aa3ed-153">Sampling signed textures will result in float values between -1.0 to 1.0.</span></span>
-   <span data-ttu-id="aa3ed-154">Lors de l’échantillonnage de textures à virgule flottante, Float16 signifie que les données seront comprises dans le \_ FLOAT16 maximal.</span><span class="sxs-lookup"><span data-stu-id="aa3ed-154">When sampling floating point textures, Float16 means that the data will range within MAX\_FLOAT16.</span></span> <span data-ttu-id="aa3ed-155">Float32 signifie que la plage maximale du pipeline sera utilisée.</span><span class="sxs-lookup"><span data-stu-id="aa3ed-155">Float32 means the maximum range of the pipeline will be used.</span></span> <span data-ttu-id="aa3ed-156">L’échantillonnage en dehors de l’une des limites n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="aa3ed-156">Sampling outside of either range is undefined.</span></span>
-   <span data-ttu-id="aa3ed-157">Il n’existe aucune limite de lecture dépendante.</span><span class="sxs-lookup"><span data-stu-id="aa3ed-157">There is no dependent read limit.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa3ed-158">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="aa3ed-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa3ed-159">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="aa3ed-159">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
