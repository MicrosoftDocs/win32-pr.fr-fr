---
title: Sample (S, float, int, float, uint), fonction (référence HLSL)
description: Échantillonne un Texture2D avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à et retourne l’état de l’opération.
ms.assetid: 1B9F48C4-DDB9-4547-B4AF-81A3ADA44C3F
keywords:
- Exemple de fonction HLSL
topic_type:
- apiref
api_name:
- Sample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9b378cb4031acecb8e0018053c7547e1948cc3e6
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/17/2020
ms.locfileid: "103735220"
---
# <a name="samplesfloatintfloatuint-function-hlsl-reference"></a><span data-ttu-id="398fd-104">Sample (S, float, int, float, uint), fonction (référence HLSL)</span><span class="sxs-lookup"><span data-stu-id="398fd-104">Sample(S,float,int,float,uint) function (HLSL reference)</span></span>

<span data-ttu-id="398fd-105">Échantillonne un [**Texture2D**](sm5-object-texture2d.md) avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à et retourne l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="398fd-105">Samples a [**Texture2D**](sm5-object-texture2d.md) with an optional value to clamp sample level-of-detail (LOD) values to, and returns status of the operation.</span></span>

> [!Note]  
> <span data-ttu-id="398fd-106">Nécessite un [Shader Model 5](d3d11-graphics-reference-sm5.md) ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="398fd-106">Requires [shader model 5](d3d11-graphics-reference-sm5.md) or higher.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="398fd-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="398fd-107">Syntax</span></span>

``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float Location,
  in  int Offset,
  in  float Clamp,
  out uint Status
);
```

## <a name="parameters"></a><span data-ttu-id="398fd-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="398fd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="398fd-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="398fd-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="398fd-110">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="398fd-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="398fd-111">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="398fd-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="398fd-112">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="398fd-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="398fd-113">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="398fd-113">The texture coordinates.</span></span> <span data-ttu-id="398fd-114">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="398fd-114">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="398fd-115">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="398fd-115">Texture-Object Type</span></span>                    | <span data-ttu-id="398fd-116">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="398fd-116">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="398fd-117">Texture1D</span><span class="sxs-lookup"><span data-stu-id="398fd-117">Texture1D</span></span>                              | <span data-ttu-id="398fd-118">float</span><span class="sxs-lookup"><span data-stu-id="398fd-118">float</span></span>          |
| <span data-ttu-id="398fd-119">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="398fd-119">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="398fd-120">float2</span><span class="sxs-lookup"><span data-stu-id="398fd-120">float2</span></span>         |
| <span data-ttu-id="398fd-121">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="398fd-121">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="398fd-122">float3</span><span class="sxs-lookup"><span data-stu-id="398fd-122">float3</span></span>         |
| <span data-ttu-id="398fd-123">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="398fd-123">TextureCubeArray</span></span>                       | <span data-ttu-id="398fd-124">float4</span><span class="sxs-lookup"><span data-stu-id="398fd-124">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="398fd-125">*Décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="398fd-125">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="398fd-126">Décalage de coordonnée de texture facultatif, qui peut être utilisé pour tout type d’objet de texture ; l’offset est appliqué à l’emplacement avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="398fd-126">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="398fd-127">Les décalages de texture doivent être statiques.</span><span class="sxs-lookup"><span data-stu-id="398fd-127">The texture offsets need to be static.</span></span> <span data-ttu-id="398fd-128">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="398fd-128">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="398fd-129">Pour plus d’informations, consultez [application de décalages de coordonnées de texture](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="398fd-129">For more info, see [Applying texture coordinate offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="398fd-130">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="398fd-130">Texture-Object Type</span></span>           | <span data-ttu-id="398fd-131">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="398fd-131">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="398fd-132">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="398fd-132">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="398fd-133">int</span><span class="sxs-lookup"><span data-stu-id="398fd-133">int</span></span>            |
| <span data-ttu-id="398fd-134">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="398fd-134">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="398fd-135">int2</span><span class="sxs-lookup"><span data-stu-id="398fd-135">int2</span></span>           |
| <span data-ttu-id="398fd-136">Texture3D</span><span class="sxs-lookup"><span data-stu-id="398fd-136">Texture3D</span></span>                     | <span data-ttu-id="398fd-137">int3</span><span class="sxs-lookup"><span data-stu-id="398fd-137">int3</span></span>           |
| <span data-ttu-id="398fd-138">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="398fd-138">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="398fd-139">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="398fd-139">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="398fd-140">*Clamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="398fd-140">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="398fd-141">Valeur facultative pour fixer l’exemple de valeurs LOD à.</span><span class="sxs-lookup"><span data-stu-id="398fd-141">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="398fd-142">Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="398fd-142">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="398fd-143">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="398fd-143">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="398fd-144">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="398fd-144">The status of the operation.</span></span> <span data-ttu-id="398fd-145">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="398fd-145">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="398fd-146">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="398fd-146">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="398fd-147">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="398fd-147">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="398fd-148">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="398fd-148">Return value</span></span>

<span data-ttu-id="398fd-149">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="398fd-149">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="remarks"></a><span data-ttu-id="398fd-150">Notes</span><span class="sxs-lookup"><span data-stu-id="398fd-150">Remarks</span></span>

<span data-ttu-id="398fd-151">L’échantillonnage de texture utilise la position Texel pour rechercher une valeur Texel.</span><span class="sxs-lookup"><span data-stu-id="398fd-151">Texture sampling uses the texel position to look up a texel value.</span></span> <span data-ttu-id="398fd-152">Un décalage peut être appliqué à la position avant la recherche.</span><span class="sxs-lookup"><span data-stu-id="398fd-152">An offset can be applied to the position before lookup.</span></span> <span data-ttu-id="398fd-153">L’état de l’échantillonneur contient les options d’échantillonnage et de filtrage.</span><span class="sxs-lookup"><span data-stu-id="398fd-153">The sampler state contains the sampling and filtering options.</span></span> <span data-ttu-id="398fd-154">Cette méthode peut être appelée dans un nuanceur de pixels, mais elle n’est pas prise en charge dans un nuanceur de sommets ou un nuanceur Geometry.</span><span class="sxs-lookup"><span data-stu-id="398fd-154">This method can be invoked within a pixel shader, but it is not supported in a vertex shader or a geometry shader.</span></span>

<span data-ttu-id="398fd-155">Utilisez un décalage uniquement au niveau d’un miplevel entier ; dans le cas contraire, vous risquez d’obtenir des résultats différents en fonction de l’implémentation matérielle ou des paramètres du pilote.</span><span class="sxs-lookup"><span data-stu-id="398fd-155">Use an offset only at an integer miplevel; otherwise, you may get different results depending on hardware implementation or driver settings.</span></span>

### <a name="calculating-texel-positions"></a><span data-ttu-id="398fd-156">Calcul des positions de Texel</span><span class="sxs-lookup"><span data-stu-id="398fd-156">Calculating Texel Positions</span></span>

<span data-ttu-id="398fd-157">Les coordonnées de texture sont des valeurs à virgule flottante qui font référence à des données de texture, également appelées « espace de texture normalisé ».</span><span class="sxs-lookup"><span data-stu-id="398fd-157">Texture coordinates are floating-point values that reference texture data, which is also known as normalized texture space.</span></span> <span data-ttu-id="398fd-158">Les modes d’habillage des adresses sont appliqués dans cet ordre (coordonnées de texture + décalages + mode habillage) pour modifier les coordonnées de texture en dehors de la \[ plage 0... 1 \] .</span><span class="sxs-lookup"><span data-stu-id="398fd-158">Address wrapping modes are applied in this order (texture coordinates + offsets + wrap mode) to modify texture coordinates outside the \[0...1\] range.</span></span>

<span data-ttu-id="398fd-159">Pour les tableaux de textures, une valeur supplémentaire dans le paramètre location spécifie un index dans un tableau de texture.</span><span class="sxs-lookup"><span data-stu-id="398fd-159">For texture arrays, an additional value in the location parameter specifies an index into a texture array.</span></span> <span data-ttu-id="398fd-160">Cet index est traité comme une valeur float mise à l’échelle (au lieu de l’espace normalisé pour les coordonnées de texture standard).</span><span class="sxs-lookup"><span data-stu-id="398fd-160">This index is treated as a scaled float value (instead of the normalized space for standard texture coordinates).</span></span> <span data-ttu-id="398fd-161">La conversion en un index d’entiers est effectuée dans l’ordre suivant (float + arrondi à l’entier le plus proche de la plage du tableau).</span><span class="sxs-lookup"><span data-stu-id="398fd-161">The conversion to an integer index is done in the following order (float + round-to-nearest-even integer + clamp to the array range).</span></span>

### <a name="applying-texture-coordinate-offsets"></a><span data-ttu-id="398fd-162">Application de décalages de coordonnées de texture</span><span class="sxs-lookup"><span data-stu-id="398fd-162">Applying Texture Coordinate Offsets</span></span>

<span data-ttu-id="398fd-163">Le paramètre offset modifie les coordonnées de texture, dans l’espace Texel.</span><span class="sxs-lookup"><span data-stu-id="398fd-163">The offset parameter modifies the texture coordinates, in texel space.</span></span> <span data-ttu-id="398fd-164">Même si les coordonnées de texture sont des nombres à virgule flottante normalisés, le décalage applique un décalage d’entier.</span><span class="sxs-lookup"><span data-stu-id="398fd-164">Even though texture coordinates are normalized floating-point numbers, the offset applies an integer offset.</span></span> <span data-ttu-id="398fd-165">Notez également que les décalages de texture doivent être statiques.</span><span class="sxs-lookup"><span data-stu-id="398fd-165">Also note that the texture offsets need to be static.</span></span>

<span data-ttu-id="398fd-166">Le format de données retourné est déterminé par le format de texture.</span><span class="sxs-lookup"><span data-stu-id="398fd-166">The data format returned is determined by the texture format.</span></span> <span data-ttu-id="398fd-167">Par exemple, si la ressource de texture a été définie au format DXGI \_ \_ A8B8G8R8 \_ UNORM \_ sRGB, l’opération d’échantillonnage convertit les texels échantillonnés de gamma 2,0 en 1,0, filtre, puis écrit le résultat sous la forme d’une valeur à virgule flottante dans la plage \[ 0.. 1 \] .</span><span class="sxs-lookup"><span data-stu-id="398fd-167">For example, if the texture resource was defined with the DXGI\_FORMAT\_A8B8G8R8\_UNORM\_SRGB format, the sampling operation converts sampled texels from gamma 2.0 to 1.0, filter, and writes the result as a floating-point value in the range \[0..1\].</span></span>

## <a name="see-also"></a><span data-ttu-id="398fd-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="398fd-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="398fd-169">Exemples de méthodes</span><span class="sxs-lookup"><span data-stu-id="398fd-169">Sample methods</span></span>](texture-sample-overload.md)
</dt> <dt>

[<span data-ttu-id="398fd-170">Texture-objet</span><span class="sxs-lookup"><span data-stu-id="398fd-170">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 
