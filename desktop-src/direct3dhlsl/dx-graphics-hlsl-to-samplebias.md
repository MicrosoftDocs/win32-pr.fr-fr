---
title: SampleBias (objet texture HLSL DirectX)
description: Échantillonne une texture après avoir appliqué le biais d’entrée au niveau de mipmap.
ms.assetid: 1bc03ad8-7b69-4001-81c7-64d8c631d68d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e710b8a6c7dd2983c6d0c635d16356f95d0b4fe7
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/17/2020
ms.locfileid: "104383400"
---
# <a name="samplebias-directx-hlsl-texture-object"></a><span data-ttu-id="dbc40-103">SampleBias (objet texture HLSL DirectX)</span><span class="sxs-lookup"><span data-stu-id="dbc40-103">SampleBias (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="dbc40-104">Échantillonne une texture après avoir appliqué le biais d’entrée au niveau de mipmap.</span><span class="sxs-lookup"><span data-stu-id="dbc40-104">Samples a texture, after applying the input bias to the mipmap level.</span></span>



|                                                                                                  |
|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbc40-105">&lt;Type &gt; de modèle objet. SampleBias (état de l’échantillonneur \_ , emplacement de flotte, biais de virgule flottante \[ , décalage int \] );</span><span class="sxs-lookup"><span data-stu-id="dbc40-105">&lt;Template Type&gt; Object.SampleBias( sampler\_state S, float Location, float Bias \[, int Offset\] );</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="dbc40-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dbc40-106">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dbc40-107">Élément</span><span class="sxs-lookup"><span data-stu-id="dbc40-107">Item</span></span></th>
<th><span data-ttu-id="dbc40-108">Description</span><span class="sxs-lookup"><span data-stu-id="dbc40-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dbc40-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Dessin</em></span><span class="sxs-lookup"><span data-stu-id="dbc40-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="dbc40-110">Tout type d' <a href="dx-graphics-hlsl-to-type.md">objet texture</a> (sauf Texture2DMS et Texture2DMSArray).</span><span class="sxs-lookup"><span data-stu-id="dbc40-110">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dbc40-111"><span id="S"></span><span id="s"></span><em>X</em></span><span class="sxs-lookup"><span data-stu-id="dbc40-111"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="dbc40-112">dans État de l' <a href="dx-graphics-hlsl-sampler.md">échantillonneur</a>.</span><span class="sxs-lookup"><span data-stu-id="dbc40-112">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="dbc40-113">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="dbc40-113">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dbc40-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Emplacement</em></span><span class="sxs-lookup"><span data-stu-id="dbc40-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="dbc40-115">dans Coordonnées de la texture.</span><span class="sxs-lookup"><span data-stu-id="dbc40-115">[in] The texture coordinates.</span></span> <span data-ttu-id="dbc40-116">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="dbc40-116">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="dbc40-117">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="dbc40-117">Texture-Object Type</span></span></th>
<th><span data-ttu-id="dbc40-118">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="dbc40-118">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dbc40-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="dbc40-119">Texture1D</span></span></td>
<td><span data-ttu-id="dbc40-120">float</span><span class="sxs-lookup"><span data-stu-id="dbc40-120">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dbc40-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="dbc40-121">Texture1DArray, Texture2D</span></span></td>
<td><span data-ttu-id="dbc40-122">float2</span><span class="sxs-lookup"><span data-stu-id="dbc40-122">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dbc40-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="dbc40-123">Texture2DArray, Texture3D, TextureCube</span></span></td>
<td><span data-ttu-id="dbc40-124">float3</span><span class="sxs-lookup"><span data-stu-id="dbc40-124">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dbc40-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="dbc40-125">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="dbc40-126">float4</span><span class="sxs-lookup"><span data-stu-id="dbc40-126">float4</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbc40-127"><span id="Bias"></span><span id="bias"></span><span id="BIAS"></span><em>Biais</em></span><span class="sxs-lookup"><span data-stu-id="dbc40-127"><span id="Bias"></span><span id="bias"></span><span id="BIAS"></span><em>Bias</em></span></span></p></td>
<td><p><span data-ttu-id="dbc40-128">dans La valeur de biais, qui est un nombre à virgule flottante compris entre-16,0 et 15,99, est appliquée à un niveau MIP avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="dbc40-128">[in] The bias value, which is a floating-point number between -16.0 and 15.99, is applied to a mip level before sampling.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbc40-129"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Décalage</em></span><span class="sxs-lookup"><span data-stu-id="dbc40-129"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="dbc40-130">dans Décalage de coordonnée de texture facultatif, qui peut être utilisé pour tout type d’objet de texture ; l’offset est appliqué à l’emplacement avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="dbc40-130">[in] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="dbc40-131">Les décalages de texture doivent être statiques.</span><span class="sxs-lookup"><span data-stu-id="dbc40-131">The texture offsets need to be static.</span></span> <span data-ttu-id="dbc40-132">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="dbc40-132">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="dbc40-133">Pour plus d’informations, consultez <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">application de décalages de coordonnées de texture</a>.</span><span class="sxs-lookup"><span data-stu-id="dbc40-133">For more info, see <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Applying texture coordinate offsets</a>.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="dbc40-134">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="dbc40-134">Texture-Object Type</span></span></th>
<th><span data-ttu-id="dbc40-135">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="dbc40-135">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dbc40-136">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="dbc40-136">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="dbc40-137">int</span><span class="sxs-lookup"><span data-stu-id="dbc40-137">int</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dbc40-138">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="dbc40-138">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="dbc40-139">int2</span><span class="sxs-lookup"><span data-stu-id="dbc40-139">int2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dbc40-140">Texture3D</span><span class="sxs-lookup"><span data-stu-id="dbc40-140">Texture3D</span></span></td>
<td><span data-ttu-id="dbc40-141">int3</span><span class="sxs-lookup"><span data-stu-id="dbc40-141">int3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dbc40-142">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="dbc40-142">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="dbc40-143">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="dbc40-143">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="dbc40-144">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="dbc40-144">Return Value</span></span>

<span data-ttu-id="dbc40-145">Le type de modèle de la texture, qui peut être un vecteur à un ou plusieurs composants.</span><span class="sxs-lookup"><span data-stu-id="dbc40-145">The texture's template type, which may be a single- or multi-component vector.</span></span> <span data-ttu-id="dbc40-146">Le format est basé sur le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)de la texture.</span><span class="sxs-lookup"><span data-stu-id="dbc40-146">The format is based on the texture's [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="dbc40-147">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="dbc40-147">Minimum Shader Model</span></span>

<span data-ttu-id="dbc40-148">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="dbc40-148">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="dbc40-149">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="dbc40-149">vs\_4\_0</span></span> | <span data-ttu-id="dbc40-150">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="dbc40-150">vs\_4\_1</span></span>  | <span data-ttu-id="dbc40-151">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="dbc40-151">ps\_4\_0</span></span> | <span data-ttu-id="dbc40-152">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="dbc40-152">ps\_4\_1</span></span>  | <span data-ttu-id="dbc40-153">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="dbc40-153">gs\_4\_0</span></span> | <span data-ttu-id="dbc40-154">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="dbc40-154">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | <span data-ttu-id="dbc40-155">x</span><span class="sxs-lookup"><span data-stu-id="dbc40-155">x</span></span>        | <span data-ttu-id="dbc40-156">x</span><span class="sxs-lookup"><span data-stu-id="dbc40-156">x</span></span>         |          |           |



 

1.  <span data-ttu-id="dbc40-157">TextureCubeArray est disponible dans le nuancier modèle 4,1 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="dbc40-157">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="dbc40-158">Le modèle de nuanceur 4,1 est disponible dans Direct3D 10,1 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="dbc40-158">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dbc40-159">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dbc40-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dbc40-160">Texture-objet</span><span class="sxs-lookup"><span data-stu-id="dbc40-160">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

