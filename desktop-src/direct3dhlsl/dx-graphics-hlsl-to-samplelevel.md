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
ms.openlocfilehash: 4249d094f142af8a9015f4e8a3b32d4e39cd42fb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127232428"
---
# <a name="samplelevel-directx-hlsl-texture-object"></a>SampleLevel (objet texture HLSL DirectX)

Échantillonne une texture à l’aide d’un décalage au niveau du mipmap.

&lt;Type &gt; de modèle objet. SampleLevel (état de l’échantillonneur \_ , emplacement de flotte, flottant LOD \[ , décalage int \] );



 

Cette fonction est similaire à l' [exemple](dx-graphics-hlsl-to-sample.md) , sauf qu’elle utilise le niveau LOD (dans le dernier composant du paramètre location) pour choisir le niveau de mipmap. Par exemple, une texture 2D utilise les deux premiers composants pour les coordonnées UV et le troisième composant pour le niveau de mipmap.

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
</tbody>
</table>

<p> </p>
<p>Si l’objet texture est un tableau, le dernier composant est l’index de tableau.</p></td>
</tr>
<tr class="even">
<td><p><span id="LOD"></span><span id="lod"></span><em>ÉCART</em></p></td>
<td><p>dans Nombre qui spécifie le niveau de mipmap. Si la valeur est égale à 0, zero’th (mappage le plus grand) est utilisé. La valeur fractionnaire (si fournie) est utilisée pour interpoler entre deux niveaux de mipmap.</p></td>
</tr>
<tr class="odd">
<td><p><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Décalage</em></p></td>
<td><p>dans Décalage de coordonnée de texture facultatif, qui peut être utilisé pour tout type d’objet de texture ; l’offset est appliqué à l’emplacement avant l’échantillonnage. Les décalages de texture doivent être statiques. Le type d’argument est dépendant du type de texture-objet. Pour plus d’informations, consultez <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">application de décalages de coordonnées de texture</a>.</p>

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

Cet exemple de code partiel provient du fichier Instancing. FX de l' [exemple Instancing10](https://msdn.microsoft.com/library/Ee416415(v=VS.85).aspx).


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Texture-objet](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

