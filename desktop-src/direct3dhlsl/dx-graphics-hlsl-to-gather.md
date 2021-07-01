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
ms.openlocfilehash: 4659ba19e9fa950a659969f2491533858f4658fb
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120544"
---
# <a name="gather-directx-hlsl-texture-object"></a>Gather (objet texture HLSL DirectX)

Obtient les quatre échantillons (composant rouge uniquement) qui seraient utilisés pour l’interpolation bilinéaire lors de l’échantillonnage d’une texture.

&lt;Type &gt; de modèle 4 Object. Gather (état de l’échantillonneur \_ , float2 \| 3 \| 4 emplacement \[ , Int2 offset \] );



 

## <a name="parameters"></a>Paramètres



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
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
<td>Les types d' <a href="dx-graphics-hlsl-to-type.md">objets de texture</a> suivants sont pris en charge : Texture2D, Texture2DArray, TextureCube, TextureCubeArray.<br/></td>
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
<td>Texture2D</td>
<td>float2</td>
</tr>
<tr class="even">
<td>Texture2DArray, TextureCube</td>
<td>float3</td>
</tr>
<tr class="odd">
<td>TextureCubeArray </td>
<td>float4</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Décalage</em></p></td>
<td><p>dans Décalage de coordonnée de texture facultatif, qui peut être utilisé pour tout type d’objet de texture ; l’offset est appliqué à l’emplacement avant l’échantillonnage. Le type d’argument est dépendant du type de texture-objet. Pour les nuanceurs ciblant le modèle de nuanceur 5,0 et versions ultérieures, les 6 bits les plus significatifs de chaque valeur de décalage sont honorés en tant que valeur signée, ce qui donne une plage [-32.. 31]. Pour les nuanceurs de modèle de nuanceur précédents, les décalages doivent être des entiers immédiats compris entre-8 et 7.</p>

<table>
<thead>
<tr class="header">
<th>Type de Texture-Object</th>
<th>Type de paramètre</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Texture2D, Texture2DArray</td>
<td>int2</td>
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

Vecteur à quatre composants, avec quatre composants de données rouges, dont le type est le même que le type de modèle de la texture.

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | PS \_ 4 \_ 0 | PS \_ 4 \_ 1  | GS \_ 4 \_ 0 | GS \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
|          | x         |          | x         |          | x         |



 

1.  TextureCubeArray est disponible dans le nuancier modèle 4,1 ou version ultérieure.
2.  Le modèle de nuanceur 4,1 est disponible dans Direct3D 10,1 ou version ultérieure.

## <a name="example"></a>Exemple


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Texture-objet](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





