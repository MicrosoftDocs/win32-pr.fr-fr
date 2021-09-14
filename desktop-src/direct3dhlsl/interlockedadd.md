---
title: InterlockedAdd, fonction (référence HLSL)
description: Effectue un ajout atomique de valeur garanti à la variable de ressource dest.
ms.assetid: b3b9cf5c-0da0-4c72-a83f-a0d96f1cac32
keywords:
- InterlockedAdd fonction HLSL
topic_type:
- apiref
api_name:
- InterlockedAdd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1d58965ea47fcad8452979a8c8ffe5b289392850
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922388"
---
# <a name="interlockedadd-function-hlsl-reference"></a>InterlockedAdd, fonction (référence HLSL)

Effectue un ajout atomique de valeur garanti à la variable de ressource dest.

## <a name="syntax"></a>Syntaxe

``` syntax
void InterlockedAdd(
  in  R dest,
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

Cette opération ne peut être effectuée que sur des ressources typées int ou uint et des variables de mémoire partagée. Il existe deux utilisations possibles de cette fonction. La première est lorsque R est un type de variable de mémoire partagée. Dans ce cas, la fonction effectue un ajout atomique de valeur au registre de mémoire partagée référencé par dest. Le deuxième scénario est lorsque R est un type de variable de ressource. Dans ce scénario, la fonction effectue un ajout atomique de valeur à l’emplacement de la ressource référencé par dest. La fonction surchargée a une variable de sortie supplémentaire qui sera définie sur la valeur d’origine de dest. Cette opération surchargée est disponible uniquement lorsque R est accessible en lecture et en écriture.

### <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                | Prise en charge |
|-----------------------------------------------------------------------------|-----------|
| [Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs | Oui       |



 

Cette fonction est prise en charge dans les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions intrinsèques](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




