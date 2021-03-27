---
title: SampleGrad (objet texture HLSL DirectX)
description: Échantillonne une texture à l’aide d’un dégradé pour influencer la façon dont l’emplacement de l’échantillon est calculé. | SampleGrad (objet texture HLSL DirectX)
ms.assetid: f3d73296-23c4-4178-b89e-6f84cfcb48a5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 236c453f3636452cbba8ed6000b2416e5187898d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211428"
---
# <a name="samplegrad-directx-hlsl-texture-object"></a><span data-ttu-id="ff026-104">SampleGrad (objet texture HLSL DirectX)</span><span class="sxs-lookup"><span data-stu-id="ff026-104">SampleGrad (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="ff026-105">Échantillonne une texture à l’aide d’un dégradé pour influencer la façon dont l’emplacement de l’échantillon est calculé.</span><span class="sxs-lookup"><span data-stu-id="ff026-105">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span>



|                                                                                                            |
|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff026-106">&lt;Type &gt; de modèle objet. SampleGrad (état de l’échantillonneur \_ , emplacement flottant, DDX float, float ddy \[ , offset int \] );</span><span class="sxs-lookup"><span data-stu-id="ff026-106">&lt;Template Type&gt; Object.SampleGrad( sampler\_state S, float Location, float DDX, float DDY \[, int Offset\] );</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="ff026-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ff026-107">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ff026-108">Élément</span><span class="sxs-lookup"><span data-stu-id="ff026-108">Item</span></span></th>
<th><span data-ttu-id="ff026-109">Description</span><span class="sxs-lookup"><span data-stu-id="ff026-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ff026-110"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Dessin</em></span><span class="sxs-lookup"><span data-stu-id="ff026-110"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="ff026-111">Tout type d' <a href="dx-graphics-hlsl-to-type.md">objet texture</a> (sauf Texture2DMS et Texture2DMSArray).</span><span class="sxs-lookup"><span data-stu-id="ff026-111">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff026-112"><span id="S"></span><span id="s"></span><em>X</em></span><span class="sxs-lookup"><span data-stu-id="ff026-112"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="ff026-113">dans État de l' <a href="dx-graphics-hlsl-sampler.md">échantillonneur</a>.</span><span class="sxs-lookup"><span data-stu-id="ff026-113">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="ff026-114">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="ff026-114">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ff026-115"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Emplacement</em></span><span class="sxs-lookup"><span data-stu-id="ff026-115"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="ff026-116">dans Coordonnées de la texture.</span><span class="sxs-lookup"><span data-stu-id="ff026-116">[in] The Texture coordinates.</span></span> <span data-ttu-id="ff026-117">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="ff026-117">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ff026-118">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="ff026-118">Texture-Object Type</span></span></th>
<th><span data-ttu-id="ff026-119">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="ff026-119">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ff026-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ff026-120">Texture1D</span></span></td>
<td><span data-ttu-id="ff026-121">float</span><span class="sxs-lookup"><span data-stu-id="ff026-121">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff026-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="ff026-122">Texture1DArray, Texture2D</span></span></td>
<td><span data-ttu-id="ff026-123">float2</span><span class="sxs-lookup"><span data-stu-id="ff026-123">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ff026-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="ff026-124">Texture2DArray, Texture3D, TextureCube</span></span></td>
<td><span data-ttu-id="ff026-125">float3</span><span class="sxs-lookup"><span data-stu-id="ff026-125">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff026-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="ff026-126">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="ff026-127">float4</span><span class="sxs-lookup"><span data-stu-id="ff026-127">float4</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ff026-128">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="ff026-128">Texture2DMS, Texture2DMSArray</span></span></td>
<td><span data-ttu-id="ff026-129">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff026-129">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff026-130"><span id="DDX"></span><span id="ddx"></span><em>DDX</em></span><span class="sxs-lookup"><span data-stu-id="ff026-130"><span id="DDX"></span><span id="ddx"></span><em>DDX</em></span></span></p></td>
<td><p><span data-ttu-id="ff026-131">dans Taux de modification de la géométrie de la surface dans l’axe x.</span><span class="sxs-lookup"><span data-stu-id="ff026-131">[in] The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="ff026-132">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="ff026-132">The argument type is dependent on the texture-object type.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ff026-133">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="ff026-133">Texture-Object Type</span></span></th>
<th><span data-ttu-id="ff026-134">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="ff026-134">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ff026-135">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="ff026-135">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="ff026-136">float</span><span class="sxs-lookup"><span data-stu-id="ff026-136">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff026-137">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="ff026-137">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="ff026-138">float2</span><span class="sxs-lookup"><span data-stu-id="ff026-138">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ff026-139">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="ff026-139">Texture3D, TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="ff026-140">float3</span><span class="sxs-lookup"><span data-stu-id="ff026-140">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff026-141">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="ff026-141">Texture2DMS, Texture2DMSArray</span></span></td>
<td><span data-ttu-id="ff026-142">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff026-142">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff026-143"><span id="DDY"></span><span id="ddy"></span><em>DDY</em></span><span class="sxs-lookup"><span data-stu-id="ff026-143"><span id="DDY"></span><span id="ddy"></span><em>DDY</em></span></span></p></td>
<td><p><span data-ttu-id="ff026-144">dans Taux de modification de la géométrie de la surface dans l’axe y.</span><span class="sxs-lookup"><span data-stu-id="ff026-144">[in] The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="ff026-145">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="ff026-145">The argument type is dependent on the texture-object type.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ff026-146">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="ff026-146">Texture-Object Type</span></span></th>
<th><span data-ttu-id="ff026-147">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="ff026-147">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ff026-148">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="ff026-148">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="ff026-149">float</span><span class="sxs-lookup"><span data-stu-id="ff026-149">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff026-150">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="ff026-150">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="ff026-151">float2</span><span class="sxs-lookup"><span data-stu-id="ff026-151">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ff026-152">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="ff026-152">Texture3D, TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="ff026-153">float3</span><span class="sxs-lookup"><span data-stu-id="ff026-153">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff026-154">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="ff026-154">Texture2DMS, Texture2DMSArray</span></span></td>
<td><span data-ttu-id="ff026-155">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff026-155">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff026-156"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Décalage</em></span><span class="sxs-lookup"><span data-stu-id="ff026-156"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="ff026-157">dans Décalage de coordonnée de texture facultatif, qui peut être utilisé pour tous les types d’objets de texture.</span><span class="sxs-lookup"><span data-stu-id="ff026-157">[in] An optional texture coordinate offset, which can be used for any texture-object types.</span></span> <span data-ttu-id="ff026-158">L’offset est appliqué à l’emplacement avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="ff026-158">The offset is applied to the location before sampling.</span></span> <span data-ttu-id="ff026-159">Utilisez un décalage uniquement au niveau d’un miplevel entier ; dans le cas contraire, vous risquez d’obtenir des résultats qui ne se traduisent pas bien en matériel.</span><span class="sxs-lookup"><span data-stu-id="ff026-159">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="ff026-160">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="ff026-160">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="ff026-161">Pour plus d’informations, consultez<a href="dx-graphics-hlsl-to-sample.md">application de décalages d’entiers</a>.</span><span class="sxs-lookup"><span data-stu-id="ff026-161">For more info, see<a href="dx-graphics-hlsl-to-sample.md">Applying Integer Offsets</a>.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ff026-162">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="ff026-162">Texture-Object Type</span></span></th>
<th><span data-ttu-id="ff026-163">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="ff026-163">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ff026-164">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="ff026-164">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="ff026-165">int</span><span class="sxs-lookup"><span data-stu-id="ff026-165">int</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff026-166">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="ff026-166">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="ff026-167">int2</span><span class="sxs-lookup"><span data-stu-id="ff026-167">int2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ff026-168">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ff026-168">Texture3D</span></span></td>
<td><span data-ttu-id="ff026-169">int3</span><span class="sxs-lookup"><span data-stu-id="ff026-169">int3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff026-170">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="ff026-170">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="ff026-171">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff026-171">not supported</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ff026-172">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="ff026-172">Texture2DMS, Texture2DMSArray</span></span></td>
<td><span data-ttu-id="ff026-173">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff026-173">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="ff026-174">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ff026-174">Return Value</span></span>

<span data-ttu-id="ff026-175">Le type de modèle de la texture, qui peut être un vecteur à un ou plusieurs composants.</span><span class="sxs-lookup"><span data-stu-id="ff026-175">The texture's template type, which may be a single- or multi-component vector.</span></span> <span data-ttu-id="ff026-176">Le format est basé sur le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)de la texture.</span><span class="sxs-lookup"><span data-stu-id="ff026-176">The format is based on the texture's [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="ff026-177">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="ff026-177">Minimum Shader Model</span></span>

<span data-ttu-id="ff026-178">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="ff026-178">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ff026-179">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ff026-179">vs\_4\_0</span></span> | <span data-ttu-id="ff026-180">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="ff026-180">vs\_4\_1</span></span>  | <span data-ttu-id="ff026-181">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ff026-181">ps\_4\_0</span></span> | <span data-ttu-id="ff026-182">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="ff026-182">ps\_4\_1</span></span>  | <span data-ttu-id="ff026-183">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ff026-183">gs\_4\_0</span></span> | <span data-ttu-id="ff026-184">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="ff026-184">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
| <span data-ttu-id="ff026-185">x</span><span class="sxs-lookup"><span data-stu-id="ff026-185">x</span></span>        | <span data-ttu-id="ff026-186">x</span><span class="sxs-lookup"><span data-stu-id="ff026-186">x</span></span>         | <span data-ttu-id="ff026-187">x</span><span class="sxs-lookup"><span data-stu-id="ff026-187">x</span></span>        | <span data-ttu-id="ff026-188">x</span><span class="sxs-lookup"><span data-stu-id="ff026-188">x</span></span>         | <span data-ttu-id="ff026-189">x</span><span class="sxs-lookup"><span data-stu-id="ff026-189">x</span></span>        | <span data-ttu-id="ff026-190">x</span><span class="sxs-lookup"><span data-stu-id="ff026-190">x</span></span>         |



 

1.  <span data-ttu-id="ff026-191">TextureCubeArray est disponible dans le nuancier modèle 4,1 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ff026-191">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="ff026-192">Le modèle de nuanceur 4,1 est disponible dans Direct3D 10,1 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ff026-192">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="ff026-193">Exemple</span><span class="sxs-lookup"><span data-stu-id="ff026-193">Example</span></span>

<span data-ttu-id="ff026-194">Cet exemple de code partiel provient du fichier MotionBlur. FX de l' [exemple MotionBlur10](https://msdn.microsoft.com/library/Ee416417(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="ff026-194">This partial code example is from the MotionBlur.fx file in the [MotionBlur10 Sample](https://msdn.microsoft.com/library/Ee416417(v=VS.85).aspx).</span></span>


```
// Object Declarations
Texture2D g_txDiffuse;

SamplerState g_samLinear
{
    Filter = ANISOTROPIC;
    MaxAnisotropy = 8;
    AddressU = Wrap;
    AddressV = Wrap;
};

struct VSSceneOut
{
    float4 Pos : SV_POSITION;
    float4 Color : COLOR0;
    float2 Tex : TEXCOORD;
    float2 Aniso : ANISOTROPY;
};

float4 PSSceneMain( VSSceneOut Input ) : SV_TARGET
{
    float2 ddx = Input.Aniso;
    float2 ddy = Input.Aniso;
    
    // Shader body calling the intrinsic function
    float4 diff = g_txDiffuse.SampleGrad( g_samLinear, Input.Tex, ddx, ddy);
    
    ...
}
```



## <a name="related-topics"></a><span data-ttu-id="ff026-195">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ff026-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff026-196">Texture-objet</span><span class="sxs-lookup"><span data-stu-id="ff026-196">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

