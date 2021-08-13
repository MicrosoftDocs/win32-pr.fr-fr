---
title: Interlockedexchang, fonction (référence HLSL)
description: Affecte la valeur à dest et retourne la valeur d’origine.
ms.assetid: 1e7ce7ff-9e23-47fa-8e76-713f6bf57abf
keywords:
- Interlockedexchang fonction HLSL
topic_type:
- apiref
api_name:
- InterlockedExchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3880a85af5658d0d50eb079c2dd1fc300e6a4de4b7f606688ab9d7a317cf321c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118511319"
---
# <a name="interlockedexchange-function-hlsl-reference"></a>Interlockedexchang, fonction (référence HLSL)

Affecte la valeur à dest et retourne la valeur d’origine.

## <a name="syntax"></a>Syntaxe

``` syntax
void InterlockedExchange(
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

Valeur d'origine.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette opération ne peut être effectuée que sur des ressources de type scalaire et des variables de mémoire partagée. Il existe deux utilisations possibles de cette fonction. La première est lorsque R est un type de variable de mémoire partagée. Dans ce cas, la fonction effectue l’opération sur le registre de mémoire partagée référencé par dest. Le deuxième scénario est lorsque R est un type de variable de ressource. Dans ce scénario, la fonction effectue l’opération sur l’emplacement de la ressource référencé par dest. Cette opération est uniquement disponible lorsque R est accessible en lecture et en écriture.

### <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                | Pris en charge |
|-----------------------------------------------------------------------------|-----------|
| [Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs | oui       |



 

Cette fonction est prise en charge dans les types de nuanceurs suivants :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
| x      |  x   | x      |  x       | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions intrinsèques](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




