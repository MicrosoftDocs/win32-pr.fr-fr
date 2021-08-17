---
title: 'Texture2D :: GatherBlue (S, float, Int2, Int2, Int2, Int2), fonction'
description: 'Retourne les composants bleus des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire. | Texture2D :: GatherBlue (S, float, Int2, Int2, Int2, Int2), fonction'
ms.assetid: 0FFD3D82-E849-4C19-BEBC-85B9CCA40CA0
keywords:
- GatherBlue fonction HLSL
topic_type:
- apiref
api_name:
- GatherBlue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d71f166a6e4ea205a8d2e41579e3907576314ce93aaf14cbc926b86e2cbe09e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118507755"
---
# <a name="gatherbluesfloatint2int2int2int2-function"></a>GatherBlue (S, float, Int2, Int2, Int2, Int2) (fonction)

Retourne les composants bleus des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.

## <a name="syntax"></a>Syntaxe


``` syntax
TemplateType GatherBlue(
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

## <a name="remarks"></a>Remarques

Les échantillons de texture peuvent être utilisés pour l’interpolation bilinéaire.

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Méthodes GatherBlue](texture2d-gatherblue.md)
</dt> </dl>

 

 




