---
title: 'Texture2D :: GatherGreen (S, float, int) (fonction)'
description: 'Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant vert par rapport à une valeur de comparaison. | Texture2D :: GatherGreen (S, float, int) (fonction)'
ms.assetid: 97e1fb52-75f4-4e73-93f1-98b7a5925efc
keywords:
- GatherGreen fonction HLSL
topic_type:
- apiref
api_name:
- GatherGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 722d7a3ac90fa3083b8f42f7704f5c9e0aeb1829
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992001"
---
# <a name="texture2dgathergreensfloatint-function"></a>Texture2D :: GatherGreen (S, float, int) (fonction)

Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant vert par rapport à une valeur de comparaison.

## <a name="syntax"></a>Syntaxe

``` syntax
TemplateType GatherGreen(
  in sampler s,
  in float2 location,
  in int2 offset
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

 \[ dans\]
</dt> <dd>

Type : **échantillonneur**

Index de base zéro de l’échantillonneur.

</dd> <dt>

*emplacement* \[ dans\]
</dt> <dd>

Type : **float2**

Les coordonnées de l’échantillon (u, v).

</dd> <dt>

*décalage* \[ dans\]
</dt> <dd>

Type : **Int2**

Offset appliqué à la coordonnée de texture avant l’échantillonnage.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **TemplateType**

Valeur à quatre composants dont le type est identique au type de modèle.

## <a name="remarks"></a>Notes

Les échantillons de texture peuvent être utilisés pour l’interpolation bilinéaire.

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Méthodes GatherGreen](texture2d-gathergreen.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




