---
title: SampleLevel (objet texture HLSL DirectX)
description: Échantillonne une texture à l’aide d’un décalage au niveau du mipmap.
ms.assetid: d61426c8-e09f-4e88-99f6-fa96c4a2b58d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bc3a074641ce5b15a3d837e8bd91dfdae09fe627
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826683"
---
# <a name="samplelevel-directx-hlsl-texture-object"></a><span data-ttu-id="bb0a5-103">SampleLevel (objet texture HLSL DirectX)</span><span class="sxs-lookup"><span data-stu-id="bb0a5-103">SampleLevel (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="bb0a5-104">Échantillonne une texture à l’aide d’un décalage au niveau du mipmap.</span><span class="sxs-lookup"><span data-stu-id="bb0a5-104">Samples a texture using a mipmap-level offset.</span></span>

<span data-ttu-id="bb0a5-105">&lt;Type &gt; de modèle objet. SampleLevel (état de l’échantillonneur \_ , emplacement de flotte, flottant LOD \[ , décalage int \] );</span><span class="sxs-lookup"><span data-stu-id="bb0a5-105">&lt;Template Type&gt; Object.SampleLevel( sampler\_state S, float Location, float LOD \[, int Offset\] );</span></span>



 

<span data-ttu-id="bb0a5-106">Cette fonction est similaire à l' [exemple](dx-graphics-hlsl-to-sample.md) , sauf qu’elle utilise le niveau LOD (dans le dernier composant du paramètre location) pour choisir le niveau de mipmap.</span><span class="sxs-lookup"><span data-stu-id="bb0a5-106">This function is similar to [Sample](dx-graphics-hlsl-to-sample.md) except that it uses the LOD level (in the last component of the location parameter) to choose the mipmap level.</span></span> <span data-ttu-id="bb0a5-107">Par exemple, une texture 2D utilise les deux premiers composants pour les coordonnées UV et le troisième composant pour le niveau de mipmap.</span><span class="sxs-lookup"><span data-stu-id="bb0a5-107">For example, a 2D texture uses the first two components for uv coordinates and the third component for the mipmap level.</span></span>

## <a name="parameters"></a><span data-ttu-id="bb0a5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bb0a5-108">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bb0a5-109">Élément</span><span class="sxs-lookup"><span data-stu-id="bb0a5-109">Item</span></span></th>
<th><span data-ttu-id="bb0a5-110">Description</span><span class="sxs-lookup"><span data-stu-id="bb0a5-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bb0a5-111"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Dessin</em></span><span class="sxs-lookup"><span data-stu-id="bb0a5-111"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="bb0a5-112">Tout type d' <a href="dx-graphics-hlsl-to-type.md">objet texture</a> (sauf Texture2DMS et Texture2DMSArray).</span><span class="sxs-lookup"><span data-stu-id="bb0a5-112">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bb0a5-113"><span id="S"></span><span id="s"></span><em>X</em></span><span class="sxs-lookup"><span data-stu-id="bb0a5-113"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="bb0a5-114">dans État de l' <a href="dx-graphics-hlsl-sampler.md">échantillonneur</a>.</span><span class="sxs-lookup"><span data-stu-id="bb0a5-114">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="bb0a5-115">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="bb0a5-115">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bb0a5-116"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Emplacement</em></span><span class="sxs-lookup"><span data-stu-id="bb0a5-116"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="bb0a5-117">dans Coordonnées de la texture.</span><span class="sxs-lookup"><span data-stu-id="bb0a5-117">[in] The texture coordinates.</span></span> <span data-ttu-id="bb0a5-118">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="bb0a5-118">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="bb0a5-119">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="bb0a5-119">Texture-Object Type</span></span></th>
<th><span data-ttu-id="bb0a5-120">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="bb0a5-120">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bb0a5-121">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bb0a5-121">Texture1D</span></span></td>
<td><span data-ttu-id="bb0a5-122">float</span><span class="sxs-lookup"><span data-stu-id="bb0a5-122">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bb0a5-123">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="bb0a5-123">Texture1DArray, Texture2D</span></span></td>
<td><span data-ttu-id="bb0a5-124">float2</span><span class="sxs-lookup"><span data-stu-id="bb0a5-124">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bb0a5-125">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="bb0a5-125">Texture2DArray, Texture3D, TextureCube</span></span></td>
<td><span data-ttu-id="bb0a5-126">float3</span><span class="sxs-lookup"><span data-stu-id="bb0a5-126">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bb0a5-127">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="bb0a5-127">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="bb0a5-128">float4</span><span class="sxs-lookup"><span data-stu-id="bb0a5-128">float4</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="bb0a5-129">Si l’objet texture est un tableau, le dernier composant est l’index de tableau.</span><span class="sxs-lookup"><span data-stu-id="bb0a5-129">If the texture object is an array, the last component is the array index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb0a5-130"><span id="LOD"></span><span id="lod"></span><em>ÉCART</em></span><span class="sxs-lookup"><span data-stu-id="bb0a5-130"><span id="LOD"></span><span id="lod"></span><em>LOD</em></span></span></p></td>
<td><p><span data-ttu-id="bb0a5-131">dans Nombre qui spécifie le niveau de mipmap.</span><span class="sxs-lookup"><span data-stu-id="bb0a5-131">[in] A number that specifies the mipmap level.</span></span> <span data-ttu-id="bb0a5-132">Si la valeur est égale à 0, zero’th (mappage le plus grand) est utilisé.</span><span class="sxs-lookup"><span data-stu-id="bb0a5-132">If the value is = 0, the zero'th (biggest map) is used.</span></span> <span data-ttu-id="bb0a5-133">La valeur fractionnaire (si fournie) est utilisée pour interpoler entre deux niveaux de mipmap.</span><span class="sxs-lookup"><span data-stu-id="bb0a5-133">The fractional value (if supplied) is used to interpolate between two mipmap levels.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb0a5-134"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Décalage</em></span><span class="sxs-lookup"><span data-stu-id="bb0a5-134"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="bb0a5-135">dans Décalage de coordonnée de texture facultatif, qui peut être utilisé pour tout type d’objet de texture ; l’offset est appliqué à l’emplacement avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="bb0a5-135">[in] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="bb0a5-136">Les décalages de texture doivent être statiques.</span><span class="sxs-lookup"><span data-stu-id="bb0a5-136">The texture offsets need to be static.</span></span> <span data-ttu-id="bb0a5-137">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="bb0a5-137">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="bb0a5-138">Pour plus d’informations, consultez <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">application de décalages de coordonnées de texture</a>.</span><span class="sxs-lookup"><span data-stu-id="bb0a5-138">For more info, see <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Applying texture coordinate offsets</a>.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="bb0a5-139">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="bb0a5-139">Texture-Object Type</span></span></th>
<th><span data-ttu-id="bb0a5-140">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="bb0a5-140">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bb0a5-141">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="bb0a5-141">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="bb0a5-142">int</span><span class="sxs-lookup"><span data-stu-id="bb0a5-142">int</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bb0a5-143">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="bb0a5-143">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="bb0a5-144">int2</span><span class="sxs-lookup"><span data-stu-id="bb0a5-144">int2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bb0a5-145">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bb0a5-145">Texture3D</span></span></td>
<td><span data-ttu-id="bb0a5-146">int3</span><span class="sxs-lookup"><span data-stu-id="bb0a5-146">int3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bb0a5-147">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="bb0a5-147">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="bb0a5-148">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="bb0a5-148">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="bb0a5-149">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bb0a5-149">Return Value</span></span>

<span data-ttu-id="bb0a5-150">Le type de modèle de la texture, qui peut être un vecteur à un ou plusieurs composants.</span><span class="sxs-lookup"><span data-stu-id="bb0a5-150">The texture's template type, which may be a single- or multi-component vector.</span></span> <span data-ttu-id="bb0a5-151">Le format est basé sur le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)de la texture.</span><span class="sxs-lookup"><span data-stu-id="bb0a5-151">The format is based on the texture's [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="bb0a5-152">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="bb0a5-152">Minimum Shader Model</span></span>

<span data-ttu-id="bb0a5-153">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="bb0a5-153">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="bb0a5-154">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bb0a5-154">vs\_4\_0</span></span> | <span data-ttu-id="bb0a5-155">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="bb0a5-155">vs\_4\_1</span></span>  | <span data-ttu-id="bb0a5-156">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bb0a5-156">ps\_4\_0</span></span> | <span data-ttu-id="bb0a5-157">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="bb0a5-157">ps\_4\_1</span></span>  | <span data-ttu-id="bb0a5-158">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bb0a5-158">gs\_4\_0</span></span> | <span data-ttu-id="bb0a5-159">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="bb0a5-159">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
| <span data-ttu-id="bb0a5-160">x</span><span class="sxs-lookup"><span data-stu-id="bb0a5-160">x</span></span>        | <span data-ttu-id="bb0a5-161">x</span><span class="sxs-lookup"><span data-stu-id="bb0a5-161">x</span></span>         | <span data-ttu-id="bb0a5-162">x</span><span class="sxs-lookup"><span data-stu-id="bb0a5-162">x</span></span>        | <span data-ttu-id="bb0a5-163">x</span><span class="sxs-lookup"><span data-stu-id="bb0a5-163">x</span></span>         | <span data-ttu-id="bb0a5-164">x</span><span class="sxs-lookup"><span data-stu-id="bb0a5-164">x</span></span>        | <span data-ttu-id="bb0a5-165">x</span><span class="sxs-lookup"><span data-stu-id="bb0a5-165">x</span></span>         |



 

1.  <span data-ttu-id="bb0a5-166">TextureCubeArray est disponible dans le nuancier modèle 4,1 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="bb0a5-166">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="bb0a5-167">Le modèle de nuanceur 4,1 est disponible dans Direct3D 10,1 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="bb0a5-167">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="bb0a5-168">Exemple</span><span class="sxs-lookup"><span data-stu-id="bb0a5-168">Example</span></span>

<span data-ttu-id="bb0a5-169">Cet exemple de code partiel provient du fichier Instancing. FX de l' [exemple Instancing10](https://msdn.microsoft.com/library/Ee416415(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="bb0a5-169">This partial code example is from the Instancing.fx file in the [Instancing10 Sample](https://msdn.microsoft.com/library/Ee416415(v=VS.85).aspx).</span></span>


```
// Object Declarations
Texture1D g_txRandom;

SamplerState g_samPoint
{
    Filter = MIN_MAG_MIP_POINT;
    AddressU = Wrap;
    AddressV = Wrap;
};

    
// Shader body calling the intrinsic function
float3 RandomDir(float fOffset)
{   
    float tCoord = (fOffset) / 300.0;
    return g_txRandom.SampleLevel( g_samPoint, tCoord, 0 );
   ...

```



## <a name="related-topics"></a><span data-ttu-id="bb0a5-170">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bb0a5-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb0a5-171">Texture-objet</span><span class="sxs-lookup"><span data-stu-id="bb0a5-171">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

