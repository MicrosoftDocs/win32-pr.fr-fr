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
ms.openlocfilehash: d22cf5fa8a8fe03a62b554def7caf28b4c4e8ab9065446bab9281e4e791e5d3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986219"
---
# <a name="samplesfloatintfloat-function-hlsl-reference"></a>Fonction Sample (S, float, int, float) (référence HLSL)

Échantillonne un [**Texture2D**](sm5-object-texture2d.md) avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à.

> [!Note]  
> Nécessite un [Shader Model 5](d3d11-graphics-reference-sm5.md) ou version ultérieure.

 

## <a name="syntax"></a>Syntaxe

``` syntax
DXGI_FORMAT Sample(
  in SamplerState S,
  in float Location,
  in int Offset,
  in float Clamp
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

 \[ Dans\]
</dt> <dd>

État de l' [échantillonneur](dx-graphics-hlsl-sampler.md). Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.

</dd> <dt>

*Emplacement* \[ dans\]
</dt> <dd>

Coordonnées de texture. Le type d’argument est dépendant du type de texture-objet.



| Type de Texture-Object                    | Type de paramètre |
|----------------------------------------|----------------|
| Texture1D                              | float          |
| Texture1DArray, Texture2D              | float2         |
| Texture2DArray, Texture3D, TextureCube | float3         |
| TextureCubeArray                       | float4         |



 

</dd> <dt>

*Décalage* \[ dans\]
</dt> <dd>

Décalage de coordonnée de texture facultatif, qui peut être utilisé pour tout type d’objet de texture ; l’offset est appliqué à l’emplacement avant l’échantillonnage. Les décalages de texture doivent être statiques. Le type d’argument est dépendant du type de texture-objet. Pour plus d’informations, consultez [application de décalages de coordonnées de texture](dx-graphics-hlsl-to-sample.md).



| Type de Texture-Object           | Type de paramètre |
|-------------------------------|----------------|
| Texture1D, Texture1DArray     | int            |
| Texture2D, Texture2DArray     | int2           |
| Texture3D                     | int3           |
| TextureCube, TextureCubeArray | non pris en charge  |



 

</dd> <dt>

*Clamp* \[ dans\]
</dt> <dd>

Valeur facultative pour fixer l’exemple de valeurs LOD à. Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

## <a name="remarks"></a>Remarques

L’échantillonnage de texture utilise la position Texel pour rechercher une valeur Texel. Un décalage peut être appliqué à la position avant la recherche. L’état de l’échantillonneur contient les options d’échantillonnage et de filtrage. Cette méthode peut être appelée dans un nuanceur de pixels, mais elle n’est pas prise en charge dans un nuanceur de sommets ou un nuanceur Geometry.

Utilisez un décalage uniquement au niveau d’un miplevel entier ; dans le cas contraire, vous risquez d’obtenir des résultats différents en fonction de l’implémentation matérielle ou des paramètres du pilote.

### <a name="calculating-texel-positions"></a>Calcul des positions de Texel

Les coordonnées de texture sont des valeurs à virgule flottante qui font référence à des données de texture, également appelées « espace de texture normalisé ». Les modes d’habillage des adresses sont appliqués dans cet ordre (coordonnées de texture + décalages + mode habillage) pour modifier les coordonnées de texture en dehors de la \[ plage 0... 1 \] .

Pour les tableaux de textures, une valeur supplémentaire dans le paramètre location spécifie un index dans un tableau de texture. Cet index est traité comme une valeur float mise à l’échelle (au lieu de l’espace normalisé pour les coordonnées de texture standard). La conversion en un index d’entiers est effectuée dans l’ordre suivant (float + arrondi à l’entier le plus proche de la plage du tableau).

### <a name="applying-texture-coordinate-offsets"></a>Application de décalages de coordonnées de texture

Le paramètre offset modifie les coordonnées de texture, dans l’espace Texel. Même si les coordonnées de texture sont des nombres à virgule flottante normalisés, le décalage applique un décalage d’entier. Notez également que les décalages de texture doivent être statiques.

Le format de données retourné est déterminé par le format de texture. Par exemple, si la ressource de texture a été définie au format DXGI \_ \_ A8B8G8R8 \_ UNORM \_ sRGB, l’opération d’échantillonnage convertit les texels échantillonnés de gamma 2,0 en 1,0, filtre, puis écrit le résultat sous la forme d’une valeur à virgule flottante dans la plage \[ 0.. 1 \] .

Utilisez un décalage uniquement au niveau d’un miplevel entier ; dans le cas contraire, vous risquez d’obtenir des résultats qui ne se traduisent pas bien en matériel.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Exemples de méthodes](texture-sample-overload.md)
</dt> <dt>

[Texture-objet](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 
