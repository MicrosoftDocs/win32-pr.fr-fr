---
title: InterlockedCompareExchange, fonction (référence HLSL)
description: Compare atomiquement la destination à la valeur de comparaison. S’ils sont identiques, la destination est remplacée par la valeur d’entrée. La valeur d’origine est définie sur la valeur d’origine de la destination.
ms.assetid: 85d1ba58-8e79-41cd-abd6-7ffff59839c7
keywords:
- InterlockedCompareExchange fonction HLSL
topic_type:
- apiref
api_name:
- InterlockedCompareExchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 74bc189996752d754599bf4547e8baa4d9fb74cc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922384"
---
# <a name="interlockedcompareexchange-function-hlsl-reference"></a>InterlockedCompareExchange, fonction (référence HLSL)

Compare atomiquement la destination à la valeur de comparaison. S’ils sont identiques, la destination est remplacée par la valeur d’entrée. La valeur d’origine est définie sur la valeur d’origine de la destination.

## <a name="syntax"></a>Syntaxe

``` syntax
void InterlockedCompareExchange(
  in  R dest,
  in  T compare_value,
  in  T value,
  out T original_value
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

</dd> <dt>

*\_ valeur d’origine* \[\]
</dt> <dd>

Type : **T**

Valeur d'origine.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Compare atomiquement la valeur référencée par *dest* avec *la \_ valeur de comparaison*, stocke la *valeur* dans l’emplacement référencé par *dest* si les valeurs correspondent, retourne la valeur d’origine de *dest* dans la *\_ valeur d’origine*. Cette opération ne peut être effectuée que sur des ressources typées **int** ou **uint** et des variables de mémoire partagée. Il existe deux utilisations possibles de cette fonction. La première est lorsque R est un type de variable de mémoire partagée. Dans ce cas, la fonction effectue l’opération sur le registre de mémoire partagée référencé par *dest*. Le deuxième scénario est lorsque R est un type de variable de ressource. Dans ce scénario, la fonction effectue l’opération sur l’emplacement de la ressource référencé par *dest*. Cette opération est uniquement disponible lorsque R est accessible en lecture et en écriture.

> [!Note]  
> Si vous appelez **InterlockedCompareExchange** dans une boucle de nuanceur [**de calcul for**](dx-graphics-hlsl-for.md) ou [**while**](dx-graphics-hlsl-while.md) , pour compiler correctement, vous devez utiliser l’attribut de **\[ \_ \_ \] condition allow UAV** sur cette boucle.

 

### <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                | Prise en charge |
|-----------------------------------------------------------------------------|-----------|
| [Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs | Oui       |



 

Cette fonction est prise en charge dans les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      |  x   |  x     |  x       | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions intrinsèques](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




