---
title: 'Texture2DArray :: GatherRed (S, float, Int2, Int2, Int2, Int2, uint), fonction'
description: 'Retourne les composants rouges des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, ainsi que l’état du mappage de mosaïques. | Texture2DArray :: GatherRed (S, float, Int2, Int2, Int2, Int2, uint), fonction'
ms.assetid: 9DD399A4-E6ED-499B-ACA3-28028C0AB271
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
ms.openlocfilehash: 8ce2ce0ab8b79a2335cc8e02d89751da3b30d856
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530145"
---
# <a name="texture2darraygatherredsfloatint2int2int2int2uint-function"></a>Texture2DArray :: GatherRed (S, float, Int2, Int2, Int2, Int2, uint), fonction

Retourne les composants rouges des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, ainsi que l’état du mappage de mosaïques.

## <a name="syntax"></a>Syntaxe


``` syntax
TemplateType GatherRed(
  in  SamplerState S,
  in  float        Location,
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

## <a name="return-value"></a>Valeur de retour

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

[Méthodes GatherRed](texture2darray-gatherred.md)
</dt> </dl>

 

 
