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
ms.openlocfilehash: caa2c83ee01739a2e2ee9595d0a26e1bdb80fef1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030389"
---
# <a name="asdouble-function"></a>AsDouble fonction)

Réinterprète une valeur de cast (valeurs 2 32 bits) dans un double.

## <a name="syntax"></a>Syntaxe

``` syntax
double asdouble(
  in uint lowbits,
  in uint highbits
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

## <a name="remarks"></a>Notes

La version surchargée suivante est également disponible :

``` syntax
double2 asdouble(uint2 lowbits, uint2 highbits);
```

Si la valeur d’entrée est de composants 2 32 bits, le type de retour contient un double. Si la valeur d’entrée est de composants 4 32 bits, le type de retour contient deux doubles. Si la valeur d’entrée est un type 64 bits, la valeur retournée aura le même nombre de composants que la valeur d’entrée.

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

 

 




