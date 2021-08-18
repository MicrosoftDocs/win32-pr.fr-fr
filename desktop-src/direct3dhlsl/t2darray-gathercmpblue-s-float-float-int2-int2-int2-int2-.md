---
title: 'Texture2DArray :: GatherCmpBlue (S, float, float, Int2, Int2, Int2, Int2), fonction'
description: 'Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant bleu par rapport à une valeur de comparaison. | Texture2DArray :: GatherCmpBlue (S, float, float, Int2, Int2, Int2, Int2), fonction'
ms.assetid: 1EAC38DC-51F5-41B8-926F-8D0626C37798
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
ms.openlocfilehash: b9a3e86398fdda94a686a52bab04fb3313857d2172e536a3b8ca832234233d23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118788914"
---
# <a name="texture2darraygathercmpbluesfloatfloatint2int2int2int2-function"></a>Texture2DArray :: GatherCmpBlue (S, float, float, Int2, Int2, Int2, Int2), fonction

Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant bleu par rapport à une valeur de comparaison.

## <a name="syntax"></a>Syntaxe


``` syntax
TemplateType GatherCmpBlue(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
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

*CompareValue* \[ dans\]
</dt> <dd>

Type : **float**

Valeur à comparer pour chaque valeur échantillonnée.

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

## <a name="remarks"></a>Remarques

Les échantillons de texture peuvent être utilisés pour l’interpolation bilinéaire.

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Méthodes GatherCmpBlue](texture2darray-gathercmpblue.md)
</dt> </dl>

 

 




