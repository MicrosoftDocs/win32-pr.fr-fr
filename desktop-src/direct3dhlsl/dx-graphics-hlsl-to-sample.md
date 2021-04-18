---
title: Échantillon (objet de texture HLSL DirectX)
description: Échantillonne une texture. | Sample (objet texture HLSL DirectX)
ms.assetid: 788ba4b4-8013-411f-9a19-fb9983386fa0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ec80d296025684c1bb67642661a31d8cdc119a53
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991872"
---
# <a name="sample-directx-hlsl-texture-object"></a><span data-ttu-id="f794f-104">Échantillon (objet de texture HLSL DirectX)</span><span class="sxs-lookup"><span data-stu-id="f794f-104">Sample (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="f794f-105">Échantillonne une texture.</span><span class="sxs-lookup"><span data-stu-id="f794f-105">Samples a texture.</span></span>

|                                                                                  |
|----------------------------------------------------------------------------------|
| <span data-ttu-id="f794f-106">&lt;Type &gt; de modèle objet. Sample (état de l’échantillonneur \_ , emplacement flottant \[ , décalage int \] );</span><span class="sxs-lookup"><span data-stu-id="f794f-106">&lt;Template Type&gt; Object.Sample( sampler\_state S, float Location \[, int Offset\] );</span></span> |

## <a name="parameters"></a><span data-ttu-id="f794f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f794f-107">Parameters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f794f-108">Élément</span><span class="sxs-lookup"><span data-stu-id="f794f-108">Item</span></span></th>
<th><span data-ttu-id="f794f-109">Description</span><span class="sxs-lookup"><span data-stu-id="f794f-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f794f-110"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Dessin</em></span><span class="sxs-lookup"><span data-stu-id="f794f-110"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="f794f-111">Tout type d' <a href="dx-graphics-hlsl-to-type.md">objet texture</a> (sauf Texture2DMS et Texture2DMSArray).</span><span class="sxs-lookup"><span data-stu-id="f794f-111">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f794f-112"><span id="S"></span><span id="s"></span><em>X</em></span><span class="sxs-lookup"><span data-stu-id="f794f-112"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="f794f-113">dans État de l' <a href="dx-graphics-hlsl-sampler.md">échantillonneur</a>.</span><span class="sxs-lookup"><span data-stu-id="f794f-113">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="f794f-114">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="f794f-114">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f794f-115"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Emplacement</em></span><span class="sxs-lookup"><span data-stu-id="f794f-115"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="f794f-116">dans Coordonnées de la texture.</span><span class="sxs-lookup"><span data-stu-id="f794f-116">[in] The texture coordinates.</span></span> <span data-ttu-id="f794f-117">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="f794f-117">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="f794f-118">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="f794f-118">Texture-Object Type</span></span></th>
<th><span data-ttu-id="f794f-119">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="f794f-119">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f794f-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f794f-120">Texture1D</span></span></td>
<td><span data-ttu-id="f794f-121">float</span><span class="sxs-lookup"><span data-stu-id="f794f-121">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f794f-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="f794f-122">Texture1DArray, Texture2D</span></span></td>
<td><span data-ttu-id="f794f-123">float2</span><span class="sxs-lookup"><span data-stu-id="f794f-123">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f794f-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="f794f-124">Texture2DArray, Texture3D, TextureCube</span></span></td>
<td><span data-ttu-id="f794f-125">float3</span><span class="sxs-lookup"><span data-stu-id="f794f-125">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f794f-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="f794f-126">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="f794f-127">float4</span><span class="sxs-lookup"><span data-stu-id="f794f-127">float4</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f794f-128"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Décalage</em></span><span class="sxs-lookup"><span data-stu-id="f794f-128"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="f794f-129">dans Décalage de coordonnée de texture facultatif, qui peut être utilisé pour tout type d’objet de texture ; l’offset est appliqué à l’emplacement avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="f794f-129">[in] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="f794f-130">Les décalages de texture doivent être statiques.</span><span class="sxs-lookup"><span data-stu-id="f794f-130">The texture offsets need to be static.</span></span> <span data-ttu-id="f794f-131">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="f794f-131">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="f794f-132">Pour plus d’informations, consultez <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">application de décalages de coordonnées de texture</a>.</span><span class="sxs-lookup"><span data-stu-id="f794f-132">For more info, see <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Applying texture coordinate offsets</a>.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="f794f-133">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="f794f-133">Texture-Object Type</span></span></th>
<th><span data-ttu-id="f794f-134">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="f794f-134">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f794f-135">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="f794f-135">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="f794f-136">int</span><span class="sxs-lookup"><span data-stu-id="f794f-136">int</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f794f-137">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="f794f-137">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="f794f-138">int2</span><span class="sxs-lookup"><span data-stu-id="f794f-138">int2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f794f-139">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f794f-139">Texture3D</span></span></td>
<td><span data-ttu-id="f794f-140">int3</span><span class="sxs-lookup"><span data-stu-id="f794f-140">int3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f794f-141">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="f794f-141">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="f794f-142">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="f794f-142">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>

## <a name="return-value"></a><span data-ttu-id="f794f-143">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f794f-143">Return value</span></span>

<span data-ttu-id="f794f-144">Le type de modèle de la texture, qui peut être un vecteur à un ou plusieurs composants.</span><span class="sxs-lookup"><span data-stu-id="f794f-144">The texture's template type, which may be a single- or multi-component vector.</span></span> <span data-ttu-id="f794f-145">Le format est basé sur le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)de la texture.</span><span class="sxs-lookup"><span data-stu-id="f794f-145">The format is based on the texture's [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="f794f-146">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="f794f-146">Minimum Shader Model</span></span>

<span data-ttu-id="f794f-147">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="f794f-147">This function is supported in the following shader models.</span></span>

| <span data-ttu-id="f794f-148">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f794f-148">vs\_4\_0</span></span> | <span data-ttu-id="f794f-149">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="f794f-149">vs\_4\_1</span></span>  | <span data-ttu-id="f794f-150">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f794f-150">ps\_4\_0</span></span> | <span data-ttu-id="f794f-151">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="f794f-151">ps\_4\_1</span></span>  | <span data-ttu-id="f794f-152">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f794f-152">gs\_4\_0</span></span> | <span data-ttu-id="f794f-153">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="f794f-153">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | <span data-ttu-id="f794f-154">x</span><span class="sxs-lookup"><span data-stu-id="f794f-154">x</span></span>        | <span data-ttu-id="f794f-155">x</span><span class="sxs-lookup"><span data-stu-id="f794f-155">x</span></span>         |          |           |

1.  <span data-ttu-id="f794f-156">TextureCubeArray est disponible dans le nuancier modèle 4,1 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="f794f-156">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="f794f-157">Le modèle de nuanceur 4,1 est disponible dans Direct3D 10,1 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="f794f-157">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="f794f-158">Exemple</span><span class="sxs-lookup"><span data-stu-id="f794f-158">Example</span></span>

<span data-ttu-id="f794f-159">Cet exemple de code partiel est basé sur le fichier BasicHLSL11. fx dans l' [exemple BasicHLSL11](https://github.com/microsoftarchive/msdn-code-gallery-community-a-c/tree/master/Basic%20DXUT%20Win32%20Samples/%5BC%2B%2B%5D-Basic%20DXUT%20Win32%20Samples/C%2B%2B/BasicHLSL11).</span><span class="sxs-lookup"><span data-stu-id="f794f-159">This partial code example is based on the BasicHLSL11.fx file in the [BasicHLSL11 Sample](https://github.com/microsoftarchive/msdn-code-gallery-community-a-c/tree/master/Basic%20DXUT%20Win32%20Samples/%5BC%2B%2B%5D-Basic%20DXUT%20Win32%20Samples/C%2B%2B/BasicHLSL11).</span></span>

```
// Object Declarations
Texture2D g_MeshTexture;            // Color texture for mesh

SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};

struct VS_OUTPUT
{
    float4 Position   : SV_POSITION; // vertex position 
    float4 Diffuse    : COLOR0;      // vertex diffuse color (note that COLOR0 is clamped from 0..1)
    float2 TextureUV  : TEXCOORD0;   // vertex texture coords 
};

VS_OUTPUT In;

// Shader body calling the intrinsic function
   ...
        Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) * In.Diffuse;
```

## <a name="remarks"></a><span data-ttu-id="f794f-160">Notes</span><span class="sxs-lookup"><span data-stu-id="f794f-160">Remarks</span></span>

<span data-ttu-id="f794f-161">L’échantillonnage de texture utilise la position Texel pour rechercher une valeur Texel.</span><span class="sxs-lookup"><span data-stu-id="f794f-161">Texture sampling uses the texel position to look up a texel value.</span></span> <span data-ttu-id="f794f-162">Un décalage peut être appliqué à la position avant la recherche.</span><span class="sxs-lookup"><span data-stu-id="f794f-162">An offset can be applied to the position before lookup.</span></span> <span data-ttu-id="f794f-163">L’état de l’échantillonneur contient les options d’échantillonnage et de filtrage.</span><span class="sxs-lookup"><span data-stu-id="f794f-163">The sampler state contains the sampling and filtering options.</span></span> <span data-ttu-id="f794f-164">Cette méthode peut être appelée dans un nuanceur de pixels, mais elle n’est pas prise en charge dans un nuanceur de sommets ou un nuanceur Geometry.</span><span class="sxs-lookup"><span data-stu-id="f794f-164">This method can be invoked within a pixel shader, but it is not supported in a vertex shader or a geometry shader.</span></span>

<span data-ttu-id="f794f-165">Utilisez un décalage uniquement au niveau d’un miplevel entier ; dans le cas contraire, vous risquez d’obtenir des résultats différents en fonction de l’implémentation matérielle ou des paramètres du pilote.</span><span class="sxs-lookup"><span data-stu-id="f794f-165">Use an offset only at an integer miplevel; otherwise, you may get different results depending on hardware implementation or driver settings.</span></span>

### <a name="calculating-texel-positions"></a><span data-ttu-id="f794f-166">Calcul des positions de Texel</span><span class="sxs-lookup"><span data-stu-id="f794f-166">Calculating texel positions</span></span>

<span data-ttu-id="f794f-167">Les coordonnées de texture sont des valeurs à virgule flottante qui font référence à des données de texture, également appelées « espace de texture normalisé ».</span><span class="sxs-lookup"><span data-stu-id="f794f-167">Texture coordinates are floating-point values that reference texture data, which is also known as normalized texture space.</span></span> <span data-ttu-id="f794f-168">Les modes d’habillage des adresses sont appliqués dans cet ordre (coordonnées de texture + décalages + mode habillage) pour modifier les coordonnées de texture en dehors de la \[ plage 0... 1 \] .</span><span class="sxs-lookup"><span data-stu-id="f794f-168">Address wrapping modes are applied in this order (texture coordinates + offsets + wrap mode) to modify texture coordinates outside the \[0...1\] range.</span></span>

<span data-ttu-id="f794f-169">Pour les tableaux de textures, une valeur supplémentaire dans le paramètre location spécifie un index dans un tableau de texture.</span><span class="sxs-lookup"><span data-stu-id="f794f-169">For texture arrays, an additional value in the location parameter specifies an index into a texture array.</span></span> <span data-ttu-id="f794f-170">Cet index est traité comme une valeur float mise à l’échelle (au lieu de l’espace normalisé pour les coordonnées de texture standard).</span><span class="sxs-lookup"><span data-stu-id="f794f-170">This index is treated as a scaled float value (instead of the normalized space for standard texture coordinates).</span></span> <span data-ttu-id="f794f-171">La conversion en un index d’entiers est effectuée dans l’ordre suivant (float + arrondi à l’entier le plus proche de la plage du tableau).</span><span class="sxs-lookup"><span data-stu-id="f794f-171">The conversion to an integer index is done in the following order (float + round-to-nearest-even integer + clamp to the array range).</span></span>

### <a name="applying-texture-coordinate-offsets"></a><span data-ttu-id="f794f-172">Application de décalages de coordonnées de texture</span><span class="sxs-lookup"><span data-stu-id="f794f-172">Applying texture coordinate offsets</span></span>

<span data-ttu-id="f794f-173">Le paramètre offset modifie les coordonnées de texture, dans l’espace Texel.</span><span class="sxs-lookup"><span data-stu-id="f794f-173">The offset parameter modifies the texture coordinates, in texel space.</span></span> <span data-ttu-id="f794f-174">Même si les coordonnées de texture sont des nombres à virgule flottante normalisés, le décalage applique un décalage d’entier.</span><span class="sxs-lookup"><span data-stu-id="f794f-174">Even though texture coordinates are normalized floating-point numbers, the offset applies an integer offset.</span></span> <span data-ttu-id="f794f-175">Notez également que les décalages de texture doivent être statiques.</span><span class="sxs-lookup"><span data-stu-id="f794f-175">Also note that the texture offsets need to be static.</span></span>

<span data-ttu-id="f794f-176">Le format de données retourné est déterminé par le format de texture.</span><span class="sxs-lookup"><span data-stu-id="f794f-176">The data format returned is determined by the texture format.</span></span> <span data-ttu-id="f794f-177">Par exemple, si la ressource de texture a été définie au format DXGI \_ \_ A8B8G8R8 \_ UNORM \_ sRGB, l’opération d’échantillonnage convertit les texels échantillonnés de gamma 2,0 en 1,0, filtre, puis écrit le résultat sous la forme d’une valeur à virgule flottante dans la plage \[ 0.. 1 \] .</span><span class="sxs-lookup"><span data-stu-id="f794f-177">For example, if the texture resource was defined with the DXGI\_FORMAT\_A8B8G8R8\_UNORM\_SRGB format, the sampling operation converts sampled texels from gamma 2.0 to 1.0, filter, and writes the result as a floating-point value in the range \[0..1\].</span></span>

## <a name="related-topics"></a><span data-ttu-id="f794f-178">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f794f-178">Related topics</span></span>

[<span data-ttu-id="f794f-179">Texture-objet</span><span class="sxs-lookup"><span data-stu-id="f794f-179">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
