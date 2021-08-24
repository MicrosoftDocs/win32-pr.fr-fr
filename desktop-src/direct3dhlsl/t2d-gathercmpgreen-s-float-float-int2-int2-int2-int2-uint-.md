---
title: 'Texture2D :: GatherCmpGreen (S, float, float, Int2, Int2, Int2, Int2, uint), fonction'
description: 'Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison entre leur composant vert et une valeur de comparaison, ainsi que l’état du mappage de mosaïque. | Texture2D :: GatherCmpGreen (S, float, float, Int2, Int2, Int2, Int2, uint), fonction'
ms.assetid: E7EB3D17-3110-4167-B255-C451BA4EFB27
keywords:
- GatherCmpGreen fonction HLSL
topic_type:
- apiref
api_name:
- GatherCmpGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 68a864ec2feb65a6ab38e647cb145e710f6a81086d69e3bffd797f3b3a00d654
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119367509"
---
# <a name="texture2dgathercmpgreensfloatfloatint2int2int2int2uint-function"></a>Texture2D :: GatherCmpGreen (S, float, float, Int2, Int2, Int2, Int2, uint), fonction

Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison entre leur composant vert et une valeur de comparaison, ainsi que l’état du mappage de mosaïque.

## <a name="syntax"></a>Syntaxe


``` syntax
TemplateType GatherCmpGreen(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int2         Offset1,
  in  int2         Offset2,
  in  int2         Offset3,
  in  int2         Offset4,
  out uint         Status
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

</dd> <dt>

*État* \[ à\]
</dt> <dd>

Type : **uint**

État de l'opération. Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) . **CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features). Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.

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

[Méthodes GatherCmpGreen](texture2d-gathercmpgreen.md)
</dt> </dl>

 

 
