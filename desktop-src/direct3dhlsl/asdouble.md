---
title: AsDouble fonction)
description: Réinterprète une valeur de cast (valeurs 2 32 bits) dans un double.
ms.assetid: 55e5276d-81e1-4e7e-8cb4-0beb57d2fb7f
keywords:
- AsDouble fonction HLSL
topic_type:
- apiref
api_name:
- asdouble
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0e191a2bf9ee7fb46337c3c7dfef7f8dea3525acf936ab745c07e7720f1ac509
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626639"
---
# <a name="asdouble-function"></a>AsDouble fonction)

Réinterprète une valeur de cast (valeurs 2 32 bits) dans un double.

## <a name="syntax"></a>Syntaxe

``` syntax
double asdouble(
  in uint lowbits,
  in uint highbits
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*lowbits* \[ dans\]
</dt> <dd>

Type : **uint**

Modèle de faible bit 32 de la valeur d’entrée.

</dd> <dt>

*highbits* \[ dans\]
</dt> <dd>

Type : **uint**

Modèle 32 bits élevé de la valeur d’entrée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **double**

Entrée (valeurs 2 32 bits) recastées en deux.

## <a name="remarks"></a>Remarques

La version surchargée suivante est également disponible :

``` syntax
double2 asdouble(uint2 lowbits, uint2 highbits);
```

Si la valeur d’entrée est de composants 2 32 bits, le type de retour contient un double. Si la valeur d’entrée est de composants 4 32 bits, le type de retour contient deux doubles. Si la valeur d’entrée est un type 64 bits, la valeur retournée aura le même nombre de composants que la valeur d’entrée.

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

 

 




