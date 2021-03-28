---
title: countbits (fonction)
description: Compte le nombre de bits (par composant) dans l’entier d’entrée.
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
ms.openlocfilehash: 60d3cd63502c6217e6fb0b0ff17685b2d2b5bf25
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030372"
---
# <a name="countbits-function"></a>countbits (fonction)

Compte le nombre de bits (par composant) dans l’entier d’entrée.

## <a name="syntax"></a>Syntaxe

``` syntax
uint countbits(
  in uint value
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ dans\]
</dt> <dd>

Type : **uint**

Valeur d'entrée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **uint**

Nombre de bits.

## <a name="remarks"></a>Notes

Les versions surchargées suivantes sont également disponibles :

``` syntax
uint count_bits(uint value);
uint2 count_bits(uint2 value);
uint3 count_bits(uint3 value);
uint4 count_bits(uint4 value);
```

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

 

 




