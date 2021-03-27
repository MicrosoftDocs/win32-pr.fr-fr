---
title: InterlockedXor, fonction (référence HLSL)
description: Exécute un XOR atomique garanti.
ms.assetid: 844ca31f-d051-4713-b9e1-dd6712ad36ca
keywords:
- InterlockedXor fonction HLSL
topic_type:
- apiref
api_name:
- InterlockedXor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b8ecaf0aa78a3bd2c1d79d10bea1e97299605398
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2020
ms.locfileid: "103679581"
---
# <a name="interlockedxor-function-hlsl-reference"></a>InterlockedXor, fonction (référence HLSL)

Exécute un XOR atomique garanti.

## <a name="syntax"></a>Syntaxe

``` syntax
void InterlockedXor(
  in  R dest,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*dest* \[ . dans\]
</dt> <dd>

Type : **R**

Adresse de destination.

</dd> <dt>

*valeur* \[ dans\]
</dt> <dd>

Type : **T**

Valeur d'entrée.

</dd> <dt>

*\_ valeur d’origine* \[\]
</dt> <dd>

Type : **T**

facultatif. Valeur d’entrée d’origine.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette opération ne peut être effectuée que sur des ressources typées int ou uint et des variables de mémoire partagée. Il existe deux utilisations possibles de cette fonction. La première est lorsque R est un type de variable de mémoire partagée. Dans ce cas, la fonction effectue un XOR atomique de value sur le registre de mémoire partagée référencé par dest. Le deuxième scénario est lorsque R est un type de variable de ressource. Dans ce scénario, la fonction effectue une valeur Atomic XORof à l’emplacement de la ressource référencé par dest. La fonction surchargée a une variable de sortie supplémentaire qui sera définie sur la valeur d’origine de dest. Cette opération surchargée est disponible uniquement lorsque R est accessible en lecture et en écriture.

### <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                | Prise en charge |
|-----------------------------------------------------------------------------|-----------|
| [Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs | Oui       |



 

Cette fonction est prise en charge dans les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|  x     |  x   | x      |  x       | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions intrinsèques](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




