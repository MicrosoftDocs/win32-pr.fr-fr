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
ms.openlocfilehash: 5f3816152b91fd03348e64c7a36dd41e8b620bd5e5ef8f4463538c44ef974485
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118793967"
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

## <a name="return-value"></a>Valeur retournée

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
| [Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs | oui       |



 

Cette fonction est prise en charge dans les types de nuanceurs suivants :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions intrinsèques](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




