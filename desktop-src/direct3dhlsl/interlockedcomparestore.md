---
title: InterlockedCompareStore, fonction (référence HLSL)
description: Compare atomiquement la destination à la valeur de comparaison. S’ils sont identiques, la destination est remplacée par la valeur d’entrée.
ms.assetid: eaf7e669-5240-40c9-9840-f4e7916e51b4
keywords:
- InterlockedCompareStore fonction HLSL
topic_type:
- apiref
api_name:
- InterlockedCompareStore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df3ffb51bbe8fe8150d19a390e62640e64ded5c9
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2020
ms.locfileid: "104381400"
---
# <a name="interlockedcomparestore-function-hlsl-reference"></a>InterlockedCompareStore, fonction (référence HLSL)

Compare atomiquement la destination à la valeur de comparaison. S’ils sont identiques, la destination est remplacée par la valeur d’entrée.

## <a name="syntax"></a>Syntaxe

``` syntax
void InterlockedCompareStore(
  in R dest,
  in T compare_value,
  in T value
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*dest* \[ . dans\]
</dt> <dd>

Type : **R**

Adresse de destination.

</dd> <dt>

*comparer la \_ valeur* \[ dans\]
</dt> <dd>

Type : **T**

Valeur de comparaison.

</dd> <dt>

*valeur* \[ dans\]
</dt> <dd>

Type : **T**

Valeur d'entrée.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Compare atomiquement la valeur référencée par *dest* avec *la \_ valeur de comparaison* et stocke la *valeur* dans l’emplacement référencé par *dest* si les valeurs correspondent. Cette opération ne peut être effectuée que sur des ressources typées **int** ou **uint** et des variables de mémoire partagée. Il existe deux utilisations possibles de cette fonction. La première est lorsque R est un type de variable de mémoire partagée. Dans ce cas, la fonction effectue l’opération sur le registre de mémoire partagée référencé par *dest*. Le deuxième scénario est lorsque R est un type de variable de ressource. Dans ce scénario, la fonction effectue l’opération sur l’emplacement de la ressource référencé par *dest*.

### <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                | Prise en charge |
|-----------------------------------------------------------------------------|-----------|
| [Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs | Oui       |



 

Cette fonction est prise en charge dans les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|  x     | x    |  x     |  x       | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions intrinsèques](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




