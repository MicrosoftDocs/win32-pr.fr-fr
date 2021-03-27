---
title: CheckAccessFullyMapped fonction)
description: Détermine si toutes les valeurs d’un échantillon, d’un regroupement ou d’une opération de chargement ont accédé à des vignettes mappées dans une ressource en mosaïque.
ms.assetid: 2CAB7770-143E-4E29-A57F-96C27021AC5F
keywords:
- CheckAccessFullyMapped fonction HLSL
topic_type:
- apiref
api_name:
- CheckAccessFullyMapped
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c7310e0ebac496fc8f5a56ba3843b7496b8ce7c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729372"
---
# <a name="checkaccessfullymapped-function"></a>CheckAccessFullyMapped fonction)

Détermine si toutes les valeurs d’un **échantillon**, d’un **regroupement** ou d’une opération de **chargement** ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).

## <a name="syntax"></a>Syntaxe

``` syntax
bool CheckAccessFullyMapped(
  in uint_only status
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*État* \[ dans\]
</dt> <dd>

Type : **uint \_ uniquement**

Valeur d’État retournée à partir d’un **échantillon**, d’un **regroupement** ou d’une opération de **chargement** . Étant donné que vous ne pouvez pas accéder directement à cette valeur d’État, vous devez la passer à **CheckAccessFullyMapped**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **bool**

Retourne une valeur **booléenne** qui indique si toutes les valeurs d’un **échantillon**, d’un **regroupement** ou d’une opération de **chargement** ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features). Retourne la **valeur true** si toutes les valeurs de l’opération ont accédé à des vignettes mappées ; Sinon, retourne **false** si des valeurs ont été extraites d’une vignette non mappée.

## <a name="remarks"></a>Notes

### <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                | Prise en charge |
|-----------------------------------------------------------------------------|-----------|
| [Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs | Oui       |



 

Cette fonction est prise en charge dans les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions intrinsèques](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 