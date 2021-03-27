---
title: 'Texture2DArray :: GatherCmpBlue (S, float, float, int) (fonction)'
description: 'Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant bleu par rapport à une valeur de comparaison. | Texture2DArray :: GatherCmpBlue (S, float, float, int) (fonction)'
ms.assetid: 5fa23e27-368a-4c55-b6d6-33506c932a43
keywords:
- GatherCmpBlue fonction HLSL
topic_type:
- apiref
api_name:
- GatherCmpBlue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 42c645333cc45c6de55a609439445936f65b85f4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761708"
---
# <a name="texture2darraygathercmpbluesfloatfloatint-function"></a>Texture2DArray :: GatherCmpBlue (S, float, float, int) (fonction)

Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant bleu par rapport à une valeur de comparaison.

## <a name="syntax"></a>Syntaxe

``` syntax
float4 GatherCmpBlue(
  in SamplerComparisonState s,
  in float3 location,
  in float compare_value,
  in int2 offset
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

 \[ dans\]
</dt> <dd>

Type : **SamplerComparisonState**

Index de base zéro de l’échantillonneur.

</dd> <dt>

*emplacement* \[ dans\]
</dt> <dd>

Type : **float3**

Les coordonnées de l’échantillon (u, v).

</dd> <dt>

*comparer la \_ valeur* \[ dans\]
</dt> <dd>

Type : **float**

Valeur à comparer pour chaque valeur échantillonnée.

</dd> <dt>

*décalage* \[ dans\]
</dt> <dd>

Type : **Int2**

Offset appliqué à la coordonnée de texture avant l’échantillonnage.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **float4**

Une valeur à quatre composants, chaque composant est le résultat d’une comparaison par composant.

## <a name="remarks"></a>Notes

Les échantillons de texture peuvent être utilisés pour l’interpolation bilinéaire.

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Méthodes GatherCmpBlue](texture2darray-gathercmpblue.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




