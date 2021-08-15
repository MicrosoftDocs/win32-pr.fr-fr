---
title: 'Texture2D :: GatherRed (S, float, int) (fonction)'
description: 'Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant rouge par rapport à une valeur de comparaison. | Texture2D :: GatherRed (S, float, int) (fonction)'
ms.assetid: 6d2d1556-d52f-4625-93ca-34da399f9a8b
keywords:
- GatherRed fonction HLSL
topic_type:
- apiref
api_name:
- GatherRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 879ba1cdad400a065fae46bd858db5569390ae0ae2a2ad338bfb9faed62bbdca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118508638"
---
# <a name="texture2dgatherredsfloatint-function"></a>Texture2D :: GatherRed (S, float, int) (fonction)

Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant rouge par rapport à une valeur de comparaison.

## <a name="syntax"></a>Syntaxe

``` syntax
TemplateType GatherRed(
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

## <a name="remarks"></a>Remarques

Les échantillons de texture peuvent être utilisés pour l’interpolation bilinéaire.

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Méthodes GatherRed](texture2d-gatherred.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




