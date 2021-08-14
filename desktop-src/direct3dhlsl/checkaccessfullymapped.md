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
ms.openlocfilehash: 8e7241fa5546edffb2b7c5ff36d2e43919e6d0b6fef9ff617c0fb63a674ffee5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118516672"
---
# <a name="checkaccessfullymapped-function"></a>CheckAccessFullyMapped fonction)

Détermine si toutes les valeurs d’un **échantillon**, d’un **regroupement** ou d’une opération de **chargement** ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).

## <a name="syntax"></a>Syntaxe

``` syntax
bool CheckAccessFullyMapped(
  in uint_only status
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

## <a name="remarks"></a>Remarques

### <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                | Pris en charge |
|-----------------------------------------------------------------------------|-----------|
| [Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs | oui       |



 

Cette fonction est prise en charge dans les types de nuanceurs suivants :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions intrinsèques](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 