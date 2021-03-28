---
title: Fonction Sample (S, float, int, float) (référence HLSL)
description: Échantillonne un Texture2D avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à.
ms.assetid: 899FACB6-40BB-471B-82A7-BDBBC63B206E
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
ms.openlocfilehash: e5c151c3d93f5e2fe374f0f60fd06798cf1ce52a
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/17/2020
ms.locfileid: "104102585"
---
# <a name="samplesfloatintfloat-function-hlsl-reference"></a><span data-ttu-id="c6fe8-104">Fonction Sample (S, float, int, float) (référence HLSL)</span><span class="sxs-lookup"><span data-stu-id="c6fe8-104">Sample(S,float,int,float) function (HLSL reference)</span></span>

<span data-ttu-id="c6fe8-105">Échantillonne un [**Texture2D**](sm5-object-texture2d.md) avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-105">Samples a [**Texture2D**](sm5-object-texture2d.md) with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

> [!Note]  
> <span data-ttu-id="c6fe8-106">Nécessite un [Shader Model 5](d3d11-graphics-reference-sm5.md) ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-106">Requires [shader model 5](d3d11-graphics-reference-sm5.md) or higher.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c6fe8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c6fe8-107">Syntax</span></span>

``` syntax
DXGI_FORMAT Sample(
  in SamplerState S,
  in float Location,
  in int Offset,
  in float Clamp
);
```

## <a name="parameters"></a><span data-ttu-id="c6fe8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c6fe8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6fe8-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="c6fe8-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6fe8-110">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="c6fe8-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="c6fe8-111">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="c6fe8-112">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c6fe8-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6fe8-113">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-113">The texture coordinates.</span></span> <span data-ttu-id="c6fe8-114">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-114">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="c6fe8-115">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="c6fe8-115">Texture-Object Type</span></span>                    | <span data-ttu-id="c6fe8-116">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="c6fe8-116">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="c6fe8-117">Texture1D</span><span class="sxs-lookup"><span data-stu-id="c6fe8-117">Texture1D</span></span>                              | <span data-ttu-id="c6fe8-118">float</span><span class="sxs-lookup"><span data-stu-id="c6fe8-118">float</span></span>          |
| <span data-ttu-id="c6fe8-119">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="c6fe8-119">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="c6fe8-120">float2</span><span class="sxs-lookup"><span data-stu-id="c6fe8-120">float2</span></span>         |
| <span data-ttu-id="c6fe8-121">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="c6fe8-121">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="c6fe8-122">float3</span><span class="sxs-lookup"><span data-stu-id="c6fe8-122">float3</span></span>         |
| <span data-ttu-id="c6fe8-123">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="c6fe8-123">TextureCubeArray</span></span>                       | <span data-ttu-id="c6fe8-124">float4</span><span class="sxs-lookup"><span data-stu-id="c6fe8-124">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="c6fe8-125">*Décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c6fe8-125">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6fe8-126">Décalage de coordonnée de texture facultatif, qui peut être utilisé pour tout type d’objet de texture ; l’offset est appliqué à l’emplacement avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-126">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="c6fe8-127">Les décalages de texture doivent être statiques.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-127">The texture offsets need to be static.</span></span> <span data-ttu-id="c6fe8-128">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-128">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="c6fe8-129">Pour plus d’informations, consultez [application de décalages de coordonnées de texture](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="c6fe8-129">For more info, see [Applying texture coordinate offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="c6fe8-130">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="c6fe8-130">Texture-Object Type</span></span>           | <span data-ttu-id="c6fe8-131">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="c6fe8-131">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="c6fe8-132">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="c6fe8-132">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="c6fe8-133">int</span><span class="sxs-lookup"><span data-stu-id="c6fe8-133">int</span></span>            |
| <span data-ttu-id="c6fe8-134">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="c6fe8-134">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="c6fe8-135">int2</span><span class="sxs-lookup"><span data-stu-id="c6fe8-135">int2</span></span>           |
| <span data-ttu-id="c6fe8-136">Texture3D</span><span class="sxs-lookup"><span data-stu-id="c6fe8-136">Texture3D</span></span>                     | <span data-ttu-id="c6fe8-137">int3</span><span class="sxs-lookup"><span data-stu-id="c6fe8-137">int3</span></span>           |
| <span data-ttu-id="c6fe8-138">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="c6fe8-138">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="c6fe8-139">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6fe8-139">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="c6fe8-140">*Clamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c6fe8-140">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6fe8-141">Valeur facultative pour fixer l’exemple de valeurs LOD à.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-141">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="c6fe8-142">Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-142">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6fe8-143">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c6fe8-143">Return value</span></span>

<span data-ttu-id="c6fe8-144">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="c6fe8-144">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="remarks"></a><span data-ttu-id="c6fe8-145">Notes</span><span class="sxs-lookup"><span data-stu-id="c6fe8-145">Remarks</span></span>

<span data-ttu-id="c6fe8-146">L’échantillonnage de texture utilise la position Texel pour rechercher une valeur Texel.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-146">Texture sampling uses the texel position to look up a texel value.</span></span> <span data-ttu-id="c6fe8-147">Un décalage peut être appliqué à la position avant la recherche.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-147">An offset can be applied to the position before lookup.</span></span> <span data-ttu-id="c6fe8-148">L’état de l’échantillonneur contient les options d’échantillonnage et de filtrage.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-148">The sampler state contains the sampling and filtering options.</span></span> <span data-ttu-id="c6fe8-149">Cette méthode peut être appelée dans un nuanceur de pixels, mais elle n’est pas prise en charge dans un nuanceur de sommets ou un nuanceur Geometry.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-149">This method can be invoked within a pixel shader, but it is not supported in a vertex shader or a geometry shader.</span></span>

<span data-ttu-id="c6fe8-150">Utilisez un décalage uniquement au niveau d’un miplevel entier ; dans le cas contraire, vous risquez d’obtenir des résultats différents en fonction de l’implémentation matérielle ou des paramètres du pilote.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-150">Use an offset only at an integer miplevel; otherwise, you may get different results depending on hardware implementation or driver settings.</span></span>

### <a name="calculating-texel-positions"></a><span data-ttu-id="c6fe8-151">Calcul des positions de Texel</span><span class="sxs-lookup"><span data-stu-id="c6fe8-151">Calculating Texel Positions</span></span>

<span data-ttu-id="c6fe8-152">Les coordonnées de texture sont des valeurs à virgule flottante qui font référence à des données de texture, également appelées « espace de texture normalisé ».</span><span class="sxs-lookup"><span data-stu-id="c6fe8-152">Texture coordinates are floating-point values that reference texture data, which is also known as normalized texture space.</span></span> <span data-ttu-id="c6fe8-153">Les modes d’habillage des adresses sont appliqués dans cet ordre (coordonnées de texture + décalages + mode habillage) pour modifier les coordonnées de texture en dehors de la \[ plage 0... 1 \] .</span><span class="sxs-lookup"><span data-stu-id="c6fe8-153">Address wrapping modes are applied in this order (texture coordinates + offsets + wrap mode) to modify texture coordinates outside the \[0...1\] range.</span></span>

<span data-ttu-id="c6fe8-154">Pour les tableaux de textures, une valeur supplémentaire dans le paramètre location spécifie un index dans un tableau de texture.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-154">For texture arrays, an additional value in the location parameter specifies an index into a texture array.</span></span> <span data-ttu-id="c6fe8-155">Cet index est traité comme une valeur float mise à l’échelle (au lieu de l’espace normalisé pour les coordonnées de texture standard).</span><span class="sxs-lookup"><span data-stu-id="c6fe8-155">This index is treated as a scaled float value (instead of the normalized space for standard texture coordinates).</span></span> <span data-ttu-id="c6fe8-156">La conversion en un index d’entiers est effectuée dans l’ordre suivant (float + arrondi à l’entier le plus proche de la plage du tableau).</span><span class="sxs-lookup"><span data-stu-id="c6fe8-156">The conversion to an integer index is done in the following order (float + round-to-nearest-even integer + clamp to the array range).</span></span>

### <a name="applying-texture-coordinate-offsets"></a><span data-ttu-id="c6fe8-157">Application de décalages de coordonnées de texture</span><span class="sxs-lookup"><span data-stu-id="c6fe8-157">Applying Texture Coordinate Offsets</span></span>

<span data-ttu-id="c6fe8-158">Le paramètre offset modifie les coordonnées de texture, dans l’espace Texel.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-158">The offset parameter modifies the texture coordinates, in texel space.</span></span> <span data-ttu-id="c6fe8-159">Même si les coordonnées de texture sont des nombres à virgule flottante normalisés, le décalage applique un décalage d’entier.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-159">Even though texture coordinates are normalized floating-point numbers, the offset applies an integer offset.</span></span> <span data-ttu-id="c6fe8-160">Notez également que les décalages de texture doivent être statiques.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-160">Also note that the texture offsets need to be static.</span></span>

<span data-ttu-id="c6fe8-161">Le format de données retourné est déterminé par le format de texture.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-161">The data format returned is determined by the texture format.</span></span> <span data-ttu-id="c6fe8-162">Par exemple, si la ressource de texture a été définie au format DXGI \_ \_ A8B8G8R8 \_ UNORM \_ sRGB, l’opération d’échantillonnage convertit les texels échantillonnés de gamma 2,0 en 1,0, filtre, puis écrit le résultat sous la forme d’une valeur à virgule flottante dans la plage \[ 0.. 1 \] .</span><span class="sxs-lookup"><span data-stu-id="c6fe8-162">For example, if the texture resource was defined with the DXGI\_FORMAT\_A8B8G8R8\_UNORM\_SRGB format, the sampling operation converts sampled texels from gamma 2.0 to 1.0, filter, and writes the result as a floating-point value in the range \[0..1\].</span></span>

<span data-ttu-id="c6fe8-163">Utilisez un décalage uniquement au niveau d’un miplevel entier ; dans le cas contraire, vous risquez d’obtenir des résultats qui ne se traduisent pas bien en matériel.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-163">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span>

## <a name="see-also"></a><span data-ttu-id="c6fe8-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6fe8-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6fe8-165">Exemples de méthodes</span><span class="sxs-lookup"><span data-stu-id="c6fe8-165">Sample methods</span></span>](texture-sample-overload.md)
</dt> <dt>

[<span data-ttu-id="c6fe8-166">Texture-objet</span><span class="sxs-lookup"><span data-stu-id="c6fe8-166">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 
