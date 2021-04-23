---
title: countbits (fonction)
description: Compte le nombre de bits (par composant) défini dans l’entier d’entrée.
ms.assetid: c4fafbc8-e21c-48cb-b433-8241a989ec85
keywords:
- countbits fonction HLSL
topic_type:
- apiref
api_name:
- countbits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 357aceca6e2aea261a9e94212b58ff6308c99560
ms.sourcegitcommit: 435ea8f5bf06808ffa7dce39afb0ee6de842ba2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2021
ms.locfileid: "107925622"
---
# <a name="countbits-function"></a>countbits (fonction)

Compte le nombre de bits (par composant) défini dans l’entier d’entrée.

## <a name="syntax"></a>Syntaxe

``` syntax
uint countbits(
  in uint value
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ dans\]
</dt> <dd>

Type : **uint**

Valeur d'entrée.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **uint**

Nombre de bits.

## <a name="remarks"></a>Remarques

Les versions surchargées suivantes sont également disponibles :

``` syntax
uint count_bits(uint value);
uint2 count_bits(uint2 value);
uint3 count_bits(uint3 value);
uint4 count_bits(uint4 value);
```

### <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                | Pris en charge |
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

 

 




