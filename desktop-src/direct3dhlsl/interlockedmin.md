---
title: InterlockedMin, fonction (référence HLSL)
description: Exécute un minimum atomique garanti.
ms.assetid: a6d3d81c-45d7-4e15-b8ec-fa2e30f854ce
keywords:
- InterlockedMin fonction HLSL
topic_type:
- apiref
api_name:
- InterlockedMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c84650ce8f95f9ba0aa6e3d5bf5d54f2915a1a94fdf96d9f89179598004744e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672659"
---
# <a name="interlockedmin-function-hlsl-reference"></a>InterlockedMin, fonction (référence HLSL)

Exécute un minimum atomique garanti.

## <a name="syntax"></a>Syntaxe

``` syntax
void InterlockedMin(
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

Facultatif. Valeur d’entrée d’origine.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette opération ne peut être effectuée que sur les ressources typées int et uint et les variables de mémoire partagée. Il existe deux utilisations possibles de cette fonction. La première est lorsque R est un type de variable de mémoire partagée. Dans ce cas, la fonction effectue un minimum de valeur atomique sur le registre de mémoire partagée référencé par dest. Le deuxième scénario est lorsque R est un type de variable de ressource. Dans ce scénario, la fonction effectue un minimum de valeur atomique sur l’emplacement de la ressource référencé par dest. La fonction surchargée a une variable de sortie supplémentaire qui sera définie sur la valeur d’origine de dest. Cette opération surchargée est disponible uniquement lorsque R est accessible en lecture et en écriture.

### <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                | Pris en charge |
|-----------------------------------------------------------------------------|-----------|
| [Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs | oui       |



 

Cette fonction est prise en charge dans les types de nuanceurs suivants :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
| x      |  x   |  x     |  x       | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions intrinsèques](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




