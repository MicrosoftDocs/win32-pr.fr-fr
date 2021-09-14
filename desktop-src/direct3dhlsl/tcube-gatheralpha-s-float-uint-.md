---
title: 'TextureCube :: GatherAlpha (S, float, uint), fonction'
description: 'Retourne les composants alpha des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, ainsi que l’état du mappage de mosaïque. | TextureCube :: GatherAlpha (S, float, uint), fonction'
ms.assetid: 19BD3024-D3E5-4AEA-8C8E-510A4EB527B5
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
ms.openlocfilehash: b915cde61309a64b77309e375284a4e5d9343724
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007982"
---
# <a name="texturecubegatheralphasfloatuint-function"></a>TextureCube :: GatherAlpha (S, float, uint), fonction

Retourne les composants alpha des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, ainsi que l’état du mappage de mosaïque.

## <a name="syntax"></a>Syntaxe


``` syntax
TemplateType GatherAlpha(
  in  SamplerState S,
  in  float        Location,
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



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Méthodes GatherAlpha](texturecube-gatheralpha.md)
</dt> <dt>

[**TextureCube**](texturecube.md)
</dt> </dl>

 

 
