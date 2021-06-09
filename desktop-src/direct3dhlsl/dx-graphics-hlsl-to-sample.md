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
ms.openlocfilehash: 2374063d222d06576f720fed2aa7fb714bcccf04
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111825746"
---
# <a name="sample-directx-hlsl-texture-object"></a>Échantillon (objet de texture HLSL DirectX)

Échantillonne une texture.

&lt;Type &gt; de modèle objet. Sample (état de l’échantillonneur \_ , emplacement flottant \[ , décalage int \] );

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

<p> </p></td>
</tr>
<tr class="even">
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
|          |           | x        | x         |          |           |

1.  TextureCubeArray est disponible dans le nuancier modèle 4,1 ou version ultérieure.
2.  Le modèle de nuanceur 4,1 est disponible dans Direct3D 10,1 ou version ultérieure.

## <a name="example"></a>Exemple

Cet exemple de code partiel est basé sur le fichier BasicHLSL11. fx dans l' [exemple BasicHLSL11](https://github.com/microsoftarchive/msdn-code-gallery-community-a-c/tree/master/Basic%20DXUT%20Win32%20Samples/%5BC%2B%2B%5D-Basic%20DXUT%20Win32%20Samples/C%2B%2B/BasicHLSL11).

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

## <a name="remarks"></a>Remarques

L’échantillonnage de texture utilise la position Texel pour rechercher une valeur Texel. Un décalage peut être appliqué à la position avant la recherche. L’état de l’échantillonneur contient les options d’échantillonnage et de filtrage. Cette méthode peut être appelée dans un nuanceur de pixels, mais elle n’est pas prise en charge dans un nuanceur de sommets ou un nuanceur Geometry.

Utilisez un décalage uniquement au niveau d’un miplevel entier ; dans le cas contraire, vous risquez d’obtenir des résultats différents en fonction de l’implémentation matérielle ou des paramètres du pilote.

### <a name="calculating-texel-positions"></a>Calcul des positions de Texel

Les coordonnées de texture sont des valeurs à virgule flottante qui font référence à des données de texture, également appelées « espace de texture normalisé ». Les modes d’habillage des adresses sont appliqués dans cet ordre (coordonnées de texture + décalages + mode habillage) pour modifier les coordonnées de texture en dehors de la \[ plage 0... 1 \] .

Pour les tableaux de textures, une valeur supplémentaire dans le paramètre location spécifie un index dans un tableau de texture. Cet index est traité comme une valeur float mise à l’échelle (au lieu de l’espace normalisé pour les coordonnées de texture standard). La conversion en un index d’entiers est effectuée dans l’ordre suivant (float + arrondi à l’entier le plus proche de la plage du tableau).

### <a name="applying-texture-coordinate-offsets"></a>Application de décalages de coordonnées de texture

Le paramètre offset modifie les coordonnées de texture, dans l’espace Texel. Même si les coordonnées de texture sont des nombres à virgule flottante normalisés, le décalage applique un décalage d’entier. Notez également que les décalages de texture doivent être statiques.

Le format de données retourné est déterminé par le format de texture. Par exemple, si la ressource de texture a été définie au format DXGI \_ \_ A8B8G8R8 \_ UNORM \_ sRGB, l’opération d’échantillonnage convertit les texels échantillonnés de gamma 2,0 en 1,0, filtre, puis écrit le résultat sous la forme d’une valeur à virgule flottante dans la plage \[ 0.. 1 \] .

## <a name="related-topics"></a>Rubriques connexes

[Texture-objet](dx-graphics-hlsl-to-type.md)
