---
title: Gather (objet texture HLSL DirectX)
description: Obtient les quatre échantillons (composant rouge uniquement) qui seraient utilisés pour l’interpolation bilinéaire lors de l’échantillonnage d’une texture.
ms.assetid: a394d8c2-99cc-4a38-9ac9-34afc666ebe0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f333c204b77d6e0c64119e16f31e170fec1d0f6c
ms.sourcegitcommit: 07ba02719c9779e082b108ae74f9699fb0236c34
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2021
ms.locfileid: "108644101"
---
# <a name="gather-directx-hlsl-texture-object"></a><span data-ttu-id="5c0e8-103">Gather (objet texture HLSL DirectX)</span><span class="sxs-lookup"><span data-stu-id="5c0e8-103">Gather (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="5c0e8-104">Obtient les quatre échantillons (composant rouge uniquement) qui seraient utilisés pour l’interpolation bilinéaire lors de l’échantillonnage d’une texture.</span><span class="sxs-lookup"><span data-stu-id="5c0e8-104">Gets the four samples (red component only) that would be used for bilinear interpolation when sampling a texture.</span></span>



|                                                                                                    |
|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c0e8-105">&lt;Type &gt; de modèle 4 Object. Gather (état de l’échantillonneur \_ , float2 \| 3 \| 4 emplacement \[ , Int2 offset \] );</span><span class="sxs-lookup"><span data-stu-id="5c0e8-105">&lt;Template Type&gt;4 Object.Gather( sampler\_state S, float2\|3\|4 Location \[, int2 Offset\] );</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="5c0e8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5c0e8-106">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5c0e8-107">Élément</span><span class="sxs-lookup"><span data-stu-id="5c0e8-107">Item</span></span></th>
<th><span data-ttu-id="5c0e8-108">Description</span><span class="sxs-lookup"><span data-stu-id="5c0e8-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5c0e8-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Dessin</em></span><span class="sxs-lookup"><span data-stu-id="5c0e8-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="5c0e8-110">Les types d' <a href="dx-graphics-hlsl-to-type.md">objets de texture</a> suivants sont pris en charge : Texture2D, Texture2DArray, TextureCube, TextureCubeArray.</span><span class="sxs-lookup"><span data-stu-id="5c0e8-110">The following <a href="dx-graphics-hlsl-to-type.md">texture-object</a> types are supported: Texture2D, Texture2DArray, TextureCube, TextureCubeArray.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c0e8-111"><span id="S"></span><span id="s"></span><em>X</em></span><span class="sxs-lookup"><span data-stu-id="5c0e8-111"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="5c0e8-112">dans État de l' <a href="dx-graphics-hlsl-sampler.md">échantillonneur</a>.</span><span class="sxs-lookup"><span data-stu-id="5c0e8-112">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="5c0e8-113">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="5c0e8-113">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c0e8-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Emplacement</em></span><span class="sxs-lookup"><span data-stu-id="5c0e8-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="5c0e8-115">dans Coordonnées de la texture.</span><span class="sxs-lookup"><span data-stu-id="5c0e8-115">[in] The texture coordinates.</span></span> <span data-ttu-id="5c0e8-116">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="5c0e8-116">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5c0e8-117">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="5c0e8-117">Texture-Object Type</span></span></th>
<th><span data-ttu-id="5c0e8-118">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="5c0e8-118">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5c0e8-119">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5c0e8-119">Texture2D</span></span></td>
<td><span data-ttu-id="5c0e8-120">float2</span><span class="sxs-lookup"><span data-stu-id="5c0e8-120">float2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c0e8-121">Texture2DArray, TextureCube</span><span class="sxs-lookup"><span data-stu-id="5c0e8-121">Texture2DArray, TextureCube</span></span></td>
<td><span data-ttu-id="5c0e8-122">float3</span><span class="sxs-lookup"><span data-stu-id="5c0e8-122">float3</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c0e8-123">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="5c0e8-123">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="5c0e8-124">float4</span><span class="sxs-lookup"><span data-stu-id="5c0e8-124">float4</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c0e8-125"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Décalage</em></span><span class="sxs-lookup"><span data-stu-id="5c0e8-125"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="5c0e8-126">dans Décalage de coordonnée de texture facultatif, qui peut être utilisé pour tout type d’objet de texture ; l’offset est appliqué à l’emplacement avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="5c0e8-126">[in] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="5c0e8-127">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="5c0e8-127">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="5c0e8-128">Pour les nuanceurs ciblant le modèle de nuanceur 5,0 et versions ultérieures, les 6 bits les plus significatifs de chaque valeur de décalage sont honorés en tant que valeur signée, ce qui donne une plage [-32.. 31].</span><span class="sxs-lookup"><span data-stu-id="5c0e8-128">For shaders targeting Shader Model 5.0 and above, the 6 least significant bits of each offset value is honored as a signed value, yielding [-32..31] range.</span></span> <span data-ttu-id="5c0e8-129">Pour les nuanceurs de modèle de nuanceur précédents, les décalages doivent être des entiers immédiats compris entre-8 et 7.</span><span class="sxs-lookup"><span data-stu-id="5c0e8-129">For previous shader model shaders, offsets need to be immediate integers between -8 and 7.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5c0e8-130">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="5c0e8-130">Texture-Object Type</span></span></th>
<th><span data-ttu-id="5c0e8-131">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="5c0e8-131">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5c0e8-132">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="5c0e8-132">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="5c0e8-133">int2</span><span class="sxs-lookup"><span data-stu-id="5c0e8-133">int2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c0e8-134">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="5c0e8-134">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="5c0e8-135">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c0e8-135">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="5c0e8-136">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5c0e8-136">Return Value</span></span>

<span data-ttu-id="5c0e8-137">Vecteur à quatre composants, avec quatre composants de données rouges, dont le type est le même que le type de modèle de la texture.</span><span class="sxs-lookup"><span data-stu-id="5c0e8-137">A four-component vector, with four components of red data, whose type is the same as the texture's template type.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="5c0e8-138">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="5c0e8-138">Minimum Shader Model</span></span>

<span data-ttu-id="5c0e8-139">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="5c0e8-139">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5c0e8-140">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5c0e8-140">vs\_4\_0</span></span> | <span data-ttu-id="5c0e8-141">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="5c0e8-141">vs\_4\_1</span></span>  | <span data-ttu-id="5c0e8-142">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5c0e8-142">ps\_4\_0</span></span> | <span data-ttu-id="5c0e8-143">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="5c0e8-143">ps\_4\_1</span></span>  | <span data-ttu-id="5c0e8-144">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5c0e8-144">gs\_4\_0</span></span> | <span data-ttu-id="5c0e8-145">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="5c0e8-145">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          | <span data-ttu-id="5c0e8-146">x</span><span class="sxs-lookup"><span data-stu-id="5c0e8-146">x</span></span>         |          | <span data-ttu-id="5c0e8-147">x</span><span class="sxs-lookup"><span data-stu-id="5c0e8-147">x</span></span>         |          | <span data-ttu-id="5c0e8-148">x</span><span class="sxs-lookup"><span data-stu-id="5c0e8-148">x</span></span>         |



 

1.  <span data-ttu-id="5c0e8-149">TextureCubeArray est disponible dans le nuancier modèle 4,1 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="5c0e8-149">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="5c0e8-150">Le modèle de nuanceur 4,1 est disponible dans Direct3D 10,1 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="5c0e8-150">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="5c0e8-151">Exemple</span><span class="sxs-lookup"><span data-stu-id="5c0e8-151">Example</span></span>


```
Texture2D<int1> Tex2d;
Texture2DArray<int2> Tex2dArray;
TextureCube<int3> TexCube;
TextureCubeArray<float2> TexCubeArray;

SamplerState s;

int4 main (float4 f : SV_Position) : SV_Target
{
    int2 iOffset = int2(2,3);

    int4 i1 = Tex2d.Gather(s, f.xy);
    int4 i2 = Tex2d.Gather(s, f.xy, iOffset);

    int4 i3 = Tex2dArray.Gather(s, f.xyz);
    int4 i4 = Tex2dArray.Gather(s, f.xyz, iOffset);

    int4 i5 = TexCube.Gather(s, f.xyzw);

    float4 f6 = TexCubeArray.Gather(s, f.xyzw);

    return i1+i2+i3+i4+i5+int4(i6);
}
  
```



## <a name="related-topics"></a><span data-ttu-id="5c0e8-152">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5c0e8-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c0e8-153">Texture-objet</span><span class="sxs-lookup"><span data-stu-id="5c0e8-153">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





