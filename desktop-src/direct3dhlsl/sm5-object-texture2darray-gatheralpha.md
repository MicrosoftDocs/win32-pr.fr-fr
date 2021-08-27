---
title: 'Texture2DArray :: GatherAlpha (S, float, int) (fonction)'
description: 'Retourne les composants alpha des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire. | Texture2DArray :: GatherAlpha (S, float, int) (fonction)'
ms.assetid: d7270277-53c1-4034-bf66-9a95bc1b51e4
keywords:
- GatherAlpha fonction HLSL
topic_type:
- apiref
api_name:
- GatherAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e79805ff931c6fe2da880c3ae090b72b87713b1c0547e6bafcf5986f07b810f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118219"
---
# <a name="texture2darraygatheralphasfloatint-function"></a>Texture2DArray :: GatherAlpha (S, float, int) (fonction)

Retourne les composants alpha des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.

## <a name="syntax"></a>Syntaxe

``` syntax
TemplateType GatherAlpha(
  in sampler s,
  in float3 location,
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

Type : **float3**

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

## <a name="remarks"></a>Remarques

Les échantillons de texture peuvent être utilisés pour l’interpolation bilinéaire.

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Méthodes GatherAlpha](texture2darray-gatheralpha.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




