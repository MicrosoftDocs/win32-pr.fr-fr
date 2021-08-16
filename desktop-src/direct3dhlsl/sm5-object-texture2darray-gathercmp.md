---
title: 'Texture2DArray :: GatherCmp (S, float, float, int) (fonction)'
description: 'Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne leur comparaison par rapport à une valeur de comparaison. | Texture2DArray :: GatherCmp (S, float, float, int) (fonction)'
ms.assetid: 7bb86448-cc73-4423-9ef4-149427cffc95
keywords:
- GatherCmp fonction HLSL
topic_type:
- apiref
api_name:
- GatherCmp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2753ac82ab653634a1c211f1eedde6b2867ade42f645d2f63d3cab41776ebb31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724637"
---
# <a name="texture2darraygathercmpsfloatfloatint-function"></a>Texture2DArray :: GatherCmp (S, float, float, int) (fonction)

Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne leur comparaison par rapport à une valeur de comparaison.

## <a name="syntax"></a>Syntaxe

``` syntax
float4 GatherCmp(
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

## <a name="remarks"></a>Remarques

Les échantillons de texture peuvent être utilisés pour l’interpolation bilinéaire.

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Méthodes GatherCmp](texture2darray-gathercmp.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




