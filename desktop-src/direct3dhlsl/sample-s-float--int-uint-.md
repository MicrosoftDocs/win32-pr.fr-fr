---
title: Sample (S, float, int, float, uint), fonction (référence HLSL)
description: Échantillonne un Texture2D avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à et retourne l’état de l’opération.
ms.assetid: 1B9F48C4-DDB9-4547-B4AF-81A3ADA44C3F
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
ms.openlocfilehash: 9b378cb4031acecb8e0018053c7547e1948cc3e6
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/17/2020
ms.locfileid: "103735220"
---
# <a name="samplesfloatintfloatuint-function-hlsl-reference"></a>Sample (S, float, int, float, uint), fonction (référence HLSL)

Échantillonne un [**Texture2D**](sm5-object-texture2d.md) avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à et retourne l’état de l’opération.

> [!Note]  
> Nécessite un [Shader Model 5](d3d11-graphics-reference-sm5.md) ou version ultérieure.

 

## <a name="syntax"></a>Syntaxe

``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float Location,
  in  int Offset,
  in  float Clamp,
  out uint Status
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

</dd> <dt>

*État* \[ à\]
</dt> <dd>

L’état de l’opération. Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) . **CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features). Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

## <a name="remarks"></a>Notes

L’échantillonnage de texture utilise la position Texel pour rechercher une valeur Texel. Un décalage peut être appliqué à la position avant la recherche. L’état de l’échantillonneur contient les options d’échantillonnage et de filtrage. Cette méthode peut être appelée dans un nuanceur de pixels, mais elle n’est pas prise en charge dans un nuanceur de sommets ou un nuanceur Geometry.

Utilisez un décalage uniquement au niveau d’un miplevel entier ; dans le cas contraire, vous risquez d’obtenir des résultats différents en fonction de l’implémentation matérielle ou des paramètres du pilote.

### <a name="calculating-texel-positions"></a>Calcul des positions de Texel

Les coordonnées de texture sont des valeurs à virgule flottante qui font référence à des données de texture, également appelées « espace de texture normalisé ». Les modes d’habillage des adresses sont appliqués dans cet ordre (coordonnées de texture + décalages + mode habillage) pour modifier les coordonnées de texture en dehors de la \[ plage 0... 1 \] .

Pour les tableaux de textures, une valeur supplémentaire dans le paramètre location spécifie un index dans un tableau de texture. Cet index est traité comme une valeur float mise à l’échelle (au lieu de l’espace normalisé pour les coordonnées de texture standard). La conversion en un index d’entiers est effectuée dans l’ordre suivant (float + arrondi à l’entier le plus proche de la plage du tableau).

### <a name="applying-texture-coordinate-offsets"></a>Application de décalages de coordonnées de texture

Le paramètre offset modifie les coordonnées de texture, dans l’espace Texel. Même si les coordonnées de texture sont des nombres à virgule flottante normalisés, le décalage applique un décalage d’entier. Notez également que les décalages de texture doivent être statiques.

Le format de données retourné est déterminé par le format de texture. Par exemple, si la ressource de texture a été définie au format DXGI \_ \_ A8B8G8R8 \_ UNORM \_ sRGB, l’opération d’échantillonnage convertit les texels échantillonnés de gamma 2,0 en 1,0, filtre, puis écrit le résultat sous la forme d’une valeur à virgule flottante dans la plage \[ 0.. 1 \] .

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Exemples de méthodes](texture-sample-overload.md)
</dt> <dt>

[Texture-objet](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 
