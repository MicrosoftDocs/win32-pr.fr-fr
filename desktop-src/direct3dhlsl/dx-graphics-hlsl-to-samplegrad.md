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
ms.openlocfilehash: 1e315cfc32b10274eee47258360e85543f15311a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127524629"
---
# <a name="samplegrad-directx-hlsl-texture-object"></a>SampleGrad (objet texture HLSL DirectX)

Échantillonne une texture à l’aide d’un dégradé pour influencer la façon dont l’emplacement de l’échantillon est calculé.

&lt;Type &gt; de modèle objet. SampleGrad (état de l’échantillonneur \_ , emplacement flottant, DDX float, float ddy \[ , offset int \] );



 

## <a name="parameters"></a>Paramètres



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Élément</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Dessin</em><br/></td>
<td>Tout type d' <a href="dx-graphics-hlsl-to-type.md">objet texture</a> (sauf Texture2DMS et Texture2DMSArray).<br/></td>
</tr>
<tr class="even">
<td><span id="S"></span><span id="s"></span><em>X</em><br/></td>
<td>dans État de l' <a href="dx-graphics-hlsl-sampler.md">échantillonneur</a>. Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.<br/></td>
</tr>
<tr class="odd">
<td><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Emplacement</em><br/></td>
<td>dans Coordonnées de la texture. Le type d’argument est dépendant du type de texture-objet. <br/> 
<table>
<thead>
<tr class="header">
<th>Type de Texture-Object</th>
<th>Type de paramètre</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Texture1D</td>
<td>float</td>
</tr>
<tr class="even">
<td>Texture1DArray, Texture2D</td>
<td>float2</td>
</tr>
<tr class="odd">
<td>Texture2DArray, Texture3D, TextureCube</td>
<td>float3</td>
</tr>
<tr class="even">
<td>TextureCubeArray </td>
<td>float4</td>
</tr>
<tr class="odd">
<td>Texture2DMS, Texture2DMSArray</td>
<td>non pris en charge</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span id="DDX"></span><span id="ddx"></span><em>DDX</em></p></td>
<td><p>dans Taux de modification de la géométrie de la surface dans l’axe x. Le type d’argument est dépendant du type de texture-objet.</p>

<table>
<thead>
<tr class="header">
<th>Type de Texture-Object</th>
<th>Type de paramètre</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Texture1D, Texture1DArray</td>
<td>float</td>
</tr>
<tr class="even">
<td>Texture2D, Texture2DArray</td>
<td>float2</td>
</tr>
<tr class="odd">
<td>Texture3D, TextureCube, TextureCubeArray </td>
<td>float3</td>
</tr>
<tr class="even">
<td>Texture2DMS, Texture2DMSArray</td>
<td>non pris en charge</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><p><span id="DDY"></span><span id="ddy"></span><em>DDY</em></p></td>
<td><p>dans Taux de modification de la géométrie de la surface dans l’axe y. Le type d’argument est dépendant du type de texture-objet.</p>

<table>
<thead>
<tr class="header">
<th>Type de Texture-Object</th>
<th>Type de paramètre</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Texture1D, Texture1DArray</td>
<td>float</td>
</tr>
<tr class="even">
<td>Texture2D, Texture2DArray</td>
<td>float2</td>
</tr>
<tr class="odd">
<td>Texture3D, TextureCube, TextureCubeArray </td>
<td>float3</td>
</tr>
<tr class="even">
<td>Texture2DMS, Texture2DMSArray</td>
<td>non pris en charge</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Décalage</em></p></td>
<td><p>dans Décalage de coordonnée de texture facultatif, qui peut être utilisé pour tous les types d’objets de texture. L’offset est appliqué à l’emplacement avant l’échantillonnage. Utilisez un décalage uniquement au niveau d’un miplevel entier ; dans le cas contraire, vous risquez d’obtenir des résultats qui ne se traduisent pas bien en matériel. Le type d’argument est dépendant du type de texture-objet. Pour plus d’informations, consultez<a href="dx-graphics-hlsl-to-sample.md">application de décalages d’entiers</a>.</p>

<table>
<thead>
<tr class="header">
<th>Type de Texture-Object</th>
<th>Type de paramètre</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Texture1D, Texture1DArray</td>
<td>int</td>
</tr>
<tr class="even">
<td>Texture2D, Texture2DArray</td>
<td>int2</td>
</tr>
<tr class="odd">
<td>Texture3D</td>
<td>int3</td>
</tr>
<tr class="even">
<td>TextureCube, TextureCubeArray </td>
<td>non pris en charge</td>
</tr>
<tr class="odd">
<td>Texture2DMS, Texture2DMSArray</td>
<td>non pris en charge</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a>Valeur renvoyée

Le type de modèle de la texture, qui peut être un vecteur à un ou plusieurs composants. Le format est basé sur le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)de la texture.

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | PS \_ 4 \_ 0 | PS \_ 4 \_ 1  | GS \_ 4 \_ 0 | GS \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
| x        | x         | x        | x         | x        | x         |



 

1.  TextureCubeArray est disponible dans le nuancier modèle 4,1 ou version ultérieure.
2.  Le modèle de nuanceur 4,1 est disponible dans Direct3D 10,1 ou version ultérieure.

## <a name="example"></a>Exemple

Cet exemple de code partiel provient du fichier MotionBlur. FX de l' [exemple MotionBlur10](https://msdn.microsoft.com/library/Ee416417(v=VS.85).aspx).


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Texture-objet](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

