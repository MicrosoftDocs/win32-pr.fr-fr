---
title: 'TextureCube :: GatherCmpGreen (S, float, float, uint), fonction'
description: 'Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison entre leur composant vert et une valeur de comparaison, ainsi que l’état du mappage de mosaïque. | TextureCube :: GatherCmpGreen (S, float, float, uint), fonction'
ms.assetid: 3EFCEFE1-BFE2-4448-962E-108C3C0861E5
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
ms.openlocfilehash: 23d1ede1bcbdcc330b5385c90f0f753888d7248191efc4108a141ad61fc3125b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118284873"
---
# <a name="texturecubegathercmpgreensfloatfloatuint-function"></a>TextureCube :: GatherCmpGreen (S, float, float, uint), fonction

Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison entre leur composant vert et une valeur de comparaison, ainsi que l’état du mappage de mosaïque.

## <a name="syntax"></a>Syntaxe


``` syntax
TemplateType GatherCmpGreen(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
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

*État* \[ à\]
</dt> <dd>

Type : **uint**

État de l'opération. Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) . **CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features). Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **TemplateType**

Valeur à quatre composants dont le type est identique au type de modèle.

## <a name="remarks"></a>Notes

Les échantillons de texture peuvent être utilisés pour l’interpolation bilinéaire.

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Méthodes GatherCmpGreen](texturecube-gathercmpgreen.md)
</dt> <dt>

[**TextureCube**](texturecube.md)
</dt> </dl>

 

 
