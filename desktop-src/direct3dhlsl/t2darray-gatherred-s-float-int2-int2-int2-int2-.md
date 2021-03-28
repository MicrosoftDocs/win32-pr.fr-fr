---
title: 'Texture2DArray :: GatherRed (S, float, Int2, Int2, Int2, Int2), fonction'
description: 'Retourne les composants rouges des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire. | Texture2DArray :: GatherRed (S, float, Int2, Int2, Int2, Int2), fonction'
ms.assetid: EB367373-D798-4CBA-AEB6-8BF89371D765
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
ms.openlocfilehash: a080580c3735018c9e6459acd6b742ce45e933d3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103953542"
---
# <a name="texture2darraygatherredsfloatint2int2int2int2-function"></a>Texture2DArray :: GatherRed (S, float, Int2, Int2, Int2, Int2), fonction

Retourne les composants rouges des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.

## <a name="syntax"></a>Syntaxe


``` syntax
TemplateType GatherRed(
  in SamplerState S,
  in float        Location,
  in int2         Offset1,
  in int2         Offset2,
  in int2         Offset3,
  in int2         Offset4
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

 \[ Dans\]
</dt> <dd>

Type : **SamplerState**

Index de base zéro de l’échantillonneur.

</dd> <dt>

*Emplacement* \[ dans\]
</dt> <dd>

Type : **float**

Les coordonnées de l’échantillon (u, v).

</dd> <dt>

*Offset1* \[ dans\]
</dt> <dd>

Type : **Int2**

Premier composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.

</dd> <dt>

*Offset2* \[ dans\]
</dt> <dd>

Type : **Int2**

Deuxième composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.

</dd> <dt>

*Offset3* \[ dans\]
</dt> <dd>

Type : **Int2**

Troisième composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.

</dd> <dt>

*Offset4* \[ dans\]
</dt> <dd>

Type : **Int2**

Quatrième composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.

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

[Méthodes GatherRed](texture2darray-gatherred.md)
</dt> </dl>

 

 




