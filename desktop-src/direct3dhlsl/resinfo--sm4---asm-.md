---
title: ResInfo (SM4-ASM)
description: Interrogez les dimensions d’une ressource d’entrée donnée.
ms.assetid: 5D549AC6-E0CB-4395-953C-5E5ECEEE234D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a252195a4b59ed791f6ac625fe1d95bbd9925f1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381158"
---
# <a name="resinfo-sm4---asm"></a><span data-ttu-id="81efe-103">ResInfo (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="81efe-103">resinfo (sm4 - asm)</span></span>

<span data-ttu-id="81efe-104">Interrogez les dimensions d’une ressource d’entrée donnée.</span><span class="sxs-lookup"><span data-stu-id="81efe-104">Query the dimensions of a given input resource.</span></span>



| <span data-ttu-id="81efe-105">ResInfo \[ \_ uint </span><span class="sxs-lookup"><span data-stu-id="81efe-105">resinfo\[\_uint</span></span>\|<span data-ttu-id="81efe-106">\_rcpFloat \] dest \[ . Mask \] , srcMipLevel. Select, \_ srcResource \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="81efe-106">\_rcpFloat\] dest\[.mask\], srcMipLevel.select\_component, srcResource\[.swizzle\]</span></span> |
|-----------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="81efe-107">Élément</span><span class="sxs-lookup"><span data-stu-id="81efe-107">Item</span></span>                                                                                                               | <span data-ttu-id="81efe-108">Description</span><span class="sxs-lookup"><span data-stu-id="81efe-108">Description</span></span>                                                                               |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="81efe-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="81efe-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="81efe-110">\[dans \] l’adresse du résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="81efe-110">\[in\] The address of the result of the operation.</span></span><br/>                             |
| <span data-ttu-id="81efe-111"><span id="srcMipLevel"></span><span id="srcmiplevel"></span><span id="SRCMIPLEVEL"></span>*srcMipLevel*</span><span class="sxs-lookup"><span data-stu-id="81efe-111"><span id="srcMipLevel"></span><span id="srcmiplevel"></span><span id="SRCMIPLEVEL"></span>*srcMipLevel*</span></span><br/> | <span data-ttu-id="81efe-112">\[au \] niveau MIP.</span><span class="sxs-lookup"><span data-stu-id="81efe-112">\[in\] The mip level.</span></span><br/>                                                          |
| <span data-ttu-id="81efe-113"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="81efe-113"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="81efe-114">\[dans \] une \# \# texture d’entrée t ou u pour laquelle les dimensions sont interrogées.</span><span class="sxs-lookup"><span data-stu-id="81efe-114">\[in\] A t\# or u\# input texture for which the dimensions are being queried.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="81efe-115">Notes</span><span class="sxs-lookup"><span data-stu-id="81efe-115">Remarks</span></span>

<span data-ttu-id="81efe-116">*srcMipLevel* est lu en tant que valeur scalaire d’entier non signé, ce qui signifie qu’un sélecteur de composant unique est requis pour le registre source, s’il ne s’agit pas d’une valeur immédiate scalaire.</span><span class="sxs-lookup"><span data-stu-id="81efe-116">*srcMipLevel* is read as an unsigned integer scalar so a single component selector is required for the source register, if it is not a scalar immediate value.</span></span>

<span data-ttu-id="81efe-117">*dest* reçoit \[ la largeur, la hauteur, la profondeur ou la taille du tableau, total-MIP-Count \] , sélectionné par le masque d’écriture.</span><span class="sxs-lookup"><span data-stu-id="81efe-117">*dest* receives \[width, height, depth or array size, total-mip-count\], selected by the write mask.</span></span>

<span data-ttu-id="81efe-118">Les valeurs de largeur, de hauteur et de profondeur retournées sont pour le niveau MIP sélectionné par le paramètre *srcMipLevel* et sont en nombre de texels, indépendamment de la taille des données Texel.</span><span class="sxs-lookup"><span data-stu-id="81efe-118">The returned width, height and depth values are for the mip-level selected by the *srcMipLevel* parameter, and are in number of texels, independent of texel data size.</span></span> <span data-ttu-id="81efe-119">Pour les exemples de ressources (texture2D \[ array \] MS \# ), la largeur et la hauteur sont également retournées dans des texels, et non des exemples.</span><span class="sxs-lookup"><span data-stu-id="81efe-119">For multisample resources (texture2D\[Array\]MS\#), width and height are also returned in texels, not samples.</span></span>

<span data-ttu-id="81efe-120">Le nombre total de MIP renvoyés dans *dest. w* n’est pas affecté par le paramètre *srcMipLevel* .</span><span class="sxs-lookup"><span data-stu-id="81efe-120">The total mip count returned in *dest.w* is unaffected by the *srcMipLevel* parameter.</span></span>

<span data-ttu-id="81efe-121">Pour UAVs (u \# ), le nombre de niveaux MIP est toujours 1.</span><span class="sxs-lookup"><span data-stu-id="81efe-121">For UAVs (u\#), the number of mip levels is always 1.</span></span>

<span data-ttu-id="81efe-122">Tous les aspects de cette instruction sont basés sur les caractéristiques de la vue de ressource liée au t \# /u \# , et non sur la ressource de base sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="81efe-122">All aspects of this instruction are based on the characteristics of the resource view bound at the t\#/u\#, not the underlying base resource.</span></span>

<span data-ttu-id="81efe-123">Les valeurs retournées sont toutes à virgule flottante, sauf si le \_ modificateur uint est utilisé, auquel cas les valeurs retournées sont tous des entiers.</span><span class="sxs-lookup"><span data-stu-id="81efe-123">Returned values are all floating point, unless the \_uint modifier is used, in which case the returned values are all integers.</span></span> <span data-ttu-id="81efe-124">Si le \_ modificateur rcpFloat est utilisé, toutes les valeurs retournées sont à virgule flottante, et la largeur, la hauteur et la profondeur sont retournées en tant que réciproques (1,0 f/Width, 1,0 f/Height, 1,0 f/depth), y compris le fichier INF si la largeur/hauteur/profondeur est 0 du comportement *srcMipLevel* hors limites.</span><span class="sxs-lookup"><span data-stu-id="81efe-124">If the \_rcpFloat modifier is used, all returned values are floating point, and the width, height and depth are returned as reciprocals (1.0f/width, 1.0f/height, 1.0f/depth), including INF if width/height/depth are 0 from out-of-range *srcMipLevel* behavior.</span></span> <span data-ttu-id="81efe-125">Le \_ modificateur rcpFloat s’applique uniquement aux valeurs retournées de largeur, de hauteur et de profondeur. il ne s’applique pas aux valeurs qui ont la valeur 0 et n’est donc pas retourné, et il ne s’applique pas non plus aux retours de taille de tableau.</span><span class="sxs-lookup"><span data-stu-id="81efe-125">The \_rcpFloat modifier only applies to width, height, and depth returned values and does not apply to values that are set to 0 and thus not returned, and also does not apply to array size returns.</span></span>

<span data-ttu-id="81efe-126">Swizzle sur *srcResource* permet aux valeurs retournées d’être swizzled arbitrairement avant d’être écrites dans la destination.</span><span class="sxs-lookup"><span data-stu-id="81efe-126">The swizzle on *srcResource* allows the returned values to be swizzled arbitrarily before they are written to the destination.</span></span>

<span data-ttu-id="81efe-127">Si *srcResource* est un Texture1D, la largeur est retournée dans *dest. x*, tandis que *dest. YZ* a la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="81efe-127">If *srcResource* is a Texture1D, then width is returned in *dest.x*, and *dest.yz* are set to 0.</span></span>

<span data-ttu-id="81efe-128">Si *srcResource* est un Texture1DArray, la largeur est retournée dans *dest. x*, la taille du tableau est retournée dans *dest. y*, tandis que *dest. z* a la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="81efe-128">If *srcResource* is a Texture1DArray, then width is returned in *dest.x*, the array size is returned in *dest.y*, and *dest.z* is set to 0.</span></span>

<span data-ttu-id="81efe-129">Si *srcResource* est un Texture2D, la largeur et la hauteur sont retournées dans *dest. XY*, tandis que *dest. z* a la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="81efe-129">If *srcResource* is a Texture2D, then width and height are returned in *dest.xy*, and *dest.z* is set to 0.</span></span>

<span data-ttu-id="81efe-130">Si *srcResource* est un Texture2DArray, la largeur et la hauteur sont retournées dans *dest. XY*, et la taille du tableau est retournée dans *dest. z*.</span><span class="sxs-lookup"><span data-stu-id="81efe-130">If *srcResource* is a Texture2DArray, then width and height are returned in *dest.xy*, and the array size is returned in *dest.z*.</span></span>

<span data-ttu-id="81efe-131">Si *srcResource* est un Texture3D, la largeur, la hauteur et la profondeur sont retournées dans *dest.xyz*.</span><span class="sxs-lookup"><span data-stu-id="81efe-131">If *srcResource* is a Texture3D, then width, height and depth are returned in *dest.xyz*.</span></span>

<span data-ttu-id="81efe-132">Si *srcResource* est un TextureCube, la largeur et la hauteur des dimensions de la face individuelle du cube sont retournées dans *dest. XY*, tandis que *dest. z* a la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="81efe-132">If *srcResource* is a TextureCube, then the width and height of the individual cube face dimensions are returned in *dest.xy*, and *dest.z* is set to 0.</span></span>

<span data-ttu-id="81efe-133">Si *srcResource* est un TextureCubeArray, la largeur et la hauteur des dimensions de la face individuelle du cube sont retournées dans *dest. XY*.</span><span class="sxs-lookup"><span data-stu-id="81efe-133">If *srcResource* is a TextureCubeArray, then the width and height the individual cube face dimensions are returned in *dest.xy*.</span></span> <span data-ttu-id="81efe-134">*dest. z* est défini sur une valeur non définie.</span><span class="sxs-lookup"><span data-stu-id="81efe-134">*dest.z* is set to an undefined value.</span></span>

<span data-ttu-id="81efe-135">Si la bride MIP par ressource a été spécifiée sur *srcResource*, ResInfo retourne toujours le nombre total de des mipmaps dans la vue pour le nombre MIP, quelle que soit la bride.</span><span class="sxs-lookup"><span data-stu-id="81efe-135">If the a per-resource mip clamp has been specified on *srcResource*, resinfo always returns the total number of mipmaps in the view for the mip count, regardless of the clamp.</span></span> <span data-ttu-id="81efe-136">Toutefois, si les dimensions d’un miplevel donné sont demandées par ResInfo et que le miplevel a été désactivé (par exemple, une bride de 2,2 signifie que les mips 0 et 1 ont été désactivés), les dimensions retournées ne sont pas définies.</span><span class="sxs-lookup"><span data-stu-id="81efe-136">However, if the dimensions of a given miplevel are requested by resinfo and the miplevel has been clamped off (e.g. a clamp of 2.2 means that mips 0 and 1 have been clamped off), the dimensions returned are undefined.</span></span> <span data-ttu-id="81efe-137">Certaines implémentations retournent le comportement hors limites spécifié pour ResInfo lorsque le miplevel est hors limites.</span><span class="sxs-lookup"><span data-stu-id="81efe-137">Some implementations will return the out of bounds behavior specified for resinfo when the miplevel is out of range.</span></span> <span data-ttu-id="81efe-138">D’autres implémentations retournent les dimensions du MIP comme s’il n’avait pas été ancré.</span><span class="sxs-lookup"><span data-stu-id="81efe-138">Other implementations will return the dimensions of the mip as if it had not been clamped.</span></span>

### <a name="restrictions"></a><span data-ttu-id="81efe-139">Restrictions</span><span class="sxs-lookup"><span data-stu-id="81efe-139">Restrictions</span></span>

-   <span data-ttu-id="81efe-140">*srcResource* doit être un \# Registre t ou u \# qui n’est pas une mémoire tampon, mais qui est une texture \* .</span><span class="sxs-lookup"><span data-stu-id="81efe-140">*srcResource* must be a t\# or u\# register that is not a Buffer, but is a Texture\*.</span></span>
-   <span data-ttu-id="81efe-141">L’adressage relatif de *srcResource* n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="81efe-141">Relative addressing of *srcResource* is not permitted.</span></span>
-   <span data-ttu-id="81efe-142">*srcMipLevel* doit utiliser un sélecteur de composant unique s’il n’est pas un scalaire immédiat.</span><span class="sxs-lookup"><span data-stu-id="81efe-142">*srcMipLevel* must use a single component selector if it is not a scalar immediate.</span></span>
-   <span data-ttu-id="81efe-143">Une extraction à partir de t \# ou u \# qui n’a rien lié à elle retourne 0 pour la largeur, la hauteur, la profondeur ou le arraySize et le nombre total-MIP-Count.</span><span class="sxs-lookup"><span data-stu-id="81efe-143">Fetching from t\# or u\# that has nothing bound to it returns 0 for width, height, depth or arraysize, and total-mip-count.</span></span> <span data-ttu-id="81efe-144">Le \_ modificateur rcpFloat est toujours respecté dans ce cas, renvoyant donc INF aux valeurs retournées applicables.</span><span class="sxs-lookup"><span data-stu-id="81efe-144">The \_rcpFloat modifier is still honored in this case, thus returning INF for the applicable returned values.</span></span>
-   <span data-ttu-id="81efe-145">Si *srcMipLevel* est en dehors de la plage du nombre de miplevels a disponibles dans la ressource, le comportement de la valeur Return size (*dest.xyz*) est identique à celui d’une \# ressource t ou u indépendante \# .</span><span class="sxs-lookup"><span data-stu-id="81efe-145">If *srcMipLevel* is out of the range of the available number of miplevels in the resource, the behavior for the size return (*dest.xyz*) is identical to that of an unbound t\# or u\# resource.</span></span> <span data-ttu-id="81efe-146">Le nombre total de MIP est toujours retourné dans *dest. w* pour ce cas.</span><span class="sxs-lookup"><span data-stu-id="81efe-146">The total mip count is still returned in *dest.w* for this case.</span></span>

<span data-ttu-id="81efe-147">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="81efe-147">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="81efe-148">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="81efe-148">Vertex Shader</span></span> | <span data-ttu-id="81efe-149">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="81efe-149">Geometry Shader</span></span> | <span data-ttu-id="81efe-150">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="81efe-150">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="81efe-151">x</span><span class="sxs-lookup"><span data-stu-id="81efe-151">x</span></span>             | <span data-ttu-id="81efe-152">x</span><span class="sxs-lookup"><span data-stu-id="81efe-152">x</span></span>               | <span data-ttu-id="81efe-153">x</span><span class="sxs-lookup"><span data-stu-id="81efe-153">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="81efe-154">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="81efe-154">Minimum Shader Model</span></span>

<span data-ttu-id="81efe-155">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="81efe-155">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="81efe-156">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="81efe-156">Shader Model</span></span>                                              | <span data-ttu-id="81efe-157">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="81efe-157">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="81efe-158">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="81efe-158">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="81efe-159">Oui</span><span class="sxs-lookup"><span data-stu-id="81efe-159">yes</span></span>       |
| [<span data-ttu-id="81efe-160">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="81efe-160">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="81efe-161">Oui</span><span class="sxs-lookup"><span data-stu-id="81efe-161">yes</span></span>       |
| [<span data-ttu-id="81efe-162">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="81efe-162">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="81efe-163">Oui</span><span class="sxs-lookup"><span data-stu-id="81efe-163">yes</span></span>       |
| [<span data-ttu-id="81efe-164">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="81efe-164">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="81efe-165">non</span><span class="sxs-lookup"><span data-stu-id="81efe-165">no</span></span>        |
| [<span data-ttu-id="81efe-166">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="81efe-166">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="81efe-167">non</span><span class="sxs-lookup"><span data-stu-id="81efe-167">no</span></span>        |
| [<span data-ttu-id="81efe-168">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="81efe-168">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="81efe-169">non</span><span class="sxs-lookup"><span data-stu-id="81efe-169">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="81efe-170">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="81efe-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81efe-171">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="81efe-171">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





