---
description: Définit les paramètres utilisés pour les calculs de frame tangent de maillage.
ms.assetid: b525b4cc-9a2d-4569-bae8-7cc7f7832cbc
title: Énumération D3DXTANGENT (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTANGENT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 43e3c5ced0eee3366b85070ce89d19154d048ab4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522953"
---
# <a name="d3dxtangent-enumeration"></a>Énumération D3DXTANGENT

Définit les paramètres utilisés pour les calculs de frame tangent de maillage.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DXTANGENT { 
  D3DXTANGENT_WRAP_U                   = 0x01,
  D3DXTANGENT_WRAP_V                   = 0x02,
  D3DXTANGENT_WRAP_UV                  = 0x03,
  D3DXTANGENT_DONT_NORMALIZE_PARTIALS  = 0x04,
  D3DXTANGENT_DONT_ORTHOGONALIZE       = 0x08,
  D3DXTANGENT_ORTHOGONALIZE_FROM_V     = 0x010,
  D3DXTANGENT_ORTHOGONALIZE_FROM_U     = 0x020,
  D3DXTANGENT_WEIGHT_BY_AREA           = 0x040,
  D3DXTANGENT_WEIGHT_EQUAL             = 0x080,
  D3DXTANGENT_WIND_CW                  = 0x0100,
  D3DXTANGENT_CALCULATE_NORMALS        = 0x0200,
  D3DXTANGENT_GENERATE_IN_PLACE        = 0x0400
} D3DXTANGENT, *LPD3DXTANGENT;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXTANGENT_WRAP_U"></span><span id="d3dxtangent_wrap_u"></span>**D3DXTANGENT \_ Wrap \_ U**
</dt> <dd>

Les valeurs de coordonnée de texture de la direction u sont comprises entre 0 et 1. Dans ce cas, un jeu de coordonnées de texture est choisi pour réduire le périmètre du triangle. Consultez [habillage de texture (Direct3D 9)](texture-wrapping.md).

</dd> <dt>

<span id="D3DXTANGENT_WRAP_V"></span><span id="d3dxtangent_wrap_v"></span>**D3DXTANGENT \_ Wrap \_ V**
</dt> <dd>

Les valeurs de coordonnée de texture dans la direction v sont comprises entre 0 et 1. Dans ce cas, un jeu de coordonnées de texture est choisi pour réduire le périmètre du triangle. Consultez [habillage de texture (Direct3D 9)](texture-wrapping.md).

</dd> <dt>

<span id="D3DXTANGENT_WRAP_UV"></span><span id="d3dxtangent_wrap_uv"></span>**D3DXTANGENT \_ enveloppe \_ UV**
</dt> <dd>

Les valeurs de coordonnée de texture dans les directions v et v sont comprises entre 0 et 1. Dans ce cas, un jeu de coordonnées de texture est choisi pour réduire le périmètre du triangle. Consultez [habillage de texture (Direct3D 9)](texture-wrapping.md).

</dd> <dt>

<span id="D3DXTANGENT_DONT_NORMALIZE_PARTIALS"></span><span id="d3dxtangent_dont_normalize_partials"></span>**D3DXTANGENT \_ ne \_ normalisent pas les \_ partiels**
</dt> <dd>

Ne normalisez pas les dérivées partielles en ce qui concerne les coordonnées de texture. Si elle n’est pas normalisée, l’échelle des dérivées partielles est proportionnelle à l’échelle du modèle 3D divisée par l’échelle du triangle dans l’espace (u, v). Cette valeur de mise à l’échelle fournit une mesure du degré d’étirement de la texture dans une direction donnée. La longueur du vecteur résultant est une somme pondérée des longueurs des dérivées partielles.

</dd> <dt>

<span id="D3DXTANGENT_DONT_ORTHOGONALIZE"></span><span id="d3dxtangent_dont_orthogonalize"></span>**D3DXTANGENT ne pas faire la \_ \_ orthogonalisation**
</dt> <dd>

Ne transformez pas les coordonnées de texture en coordonnées cartésiennes orthogonales. S’exclut mutuellement avec D3DXTANGENT \_ orthogonale \_ de \_ vous et D3DXTANGENT \_ orthogonale \_ de \_ V.

</dd> <dt>

<span id="D3DXTANGENT_ORTHOGONALIZE_FROM_V"></span><span id="d3dxtangent_orthogonalize_from_v"></span>**D3DXTANGENT \_ orthogonaliser \_ à partir de \_ V**
</dt> <dd>

Calculez la dérivée partielle par rapport à la coordonnée de texture v indépendamment pour chaque vertex, puis calculez la dérivée partielle par rapport à vous en tant que produit croisé de la dérivée partielle par rapport à v et au vecteur normal. L’exception s’exclut mutuellement avec D3DXTANGENT \_ \_ \_ \_ \_ .

</dd> <dt>

<span id="D3DXTANGENT_ORTHOGONALIZE_FROM_U"></span><span id="d3dxtangent_orthogonalize_from_u"></span>**D3DXTANGENT \_ orthogonaliser \_ à partir de \_ U**
</dt> <dd>

Calculez la dérivée partielle par rapport à la coordonnée de texture u indépendamment pour chaque vertex, puis calculez la dérivée partielle par rapport à v comme produit croisé du vecteur normal et du dérivé partiel par rapport à vous. L’exception s’exclut mutuellement avec D3DXTANGENT \_ \_ \_ \_ \_ .

</dd> <dt>

<span id="D3DXTANGENT_WEIGHT_BY_AREA"></span><span id="d3dxtangent_weight_by_area"></span>**D3DXTANGENT \_ poids \_ par \_ zone**
</dt> <dd>

Pondérez la direction du vecteur de vecteurs normaux ou dérivés partiels calculé en fonction des zones de triangles attachées à ce vertex. S’exclut mutuellement avec le poids de D3DXTANGENT \_ \_ égal à.

</dd> <dt>

<span id="D3DXTANGENT_WEIGHT_EQUAL"></span><span id="d3dxtangent_weight_equal"></span>**Poids de D3DXTANGENT \_ \_ égal à**
</dt> <dd>

Calculez un vecteur normal de longueur unitaire pour chaque triangle du maillage d’entrée. S’exclut mutuellement avec le \_ poids \_ de D3DXTANGENT par \_ zone.

</dd> <dt>

<span id="D3DXTANGENT_WIND_CW"></span><span id="d3dxtangent_wind_cw"></span>**D3DXTANGENT \_ vent- \_ PV**
</dt> <dd>

Les vertex sont classés dans le sens des aiguilles d’une montre autour de chaque triangle. La direction du vecteur normal calculé est donc inversée 180 degrés à partir de la direction calculée à l’aide du classement des sommets dans le sens inverse des aiguilles d’une passe.

</dd> <dt>

<span id="D3DXTANGENT_CALCULATE_NORMALS"></span><span id="d3dxtangent_calculate_normals"></span>**D3DXTANGENT \_ calculer les \_ normales**
</dt> <dd>

Calcule le vecteur normal par vertex pour chaque triangle du maillage d’entrée et ignore tous les vecteurs normaux déjà présents dans le maillage d’entrée.

</dd> <dt>

<span id="D3DXTANGENT_GENERATE_IN_PLACE"></span><span id="d3dxtangent_generate_in_place"></span>**D3DXTANGENT \_ Générer \_ sur \_ place**
</dt> <dd>

Les résultats sont stockés dans le maillage d’entrée d’origine et le maillage de sortie n’est pas utilisé.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md)
</dt> </dl>

 

 




