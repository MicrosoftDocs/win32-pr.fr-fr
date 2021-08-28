---
title: reversebits (fonction)
description: Inverse l’ordre des bits, par composant.
ms.assetid: dad46e25-9980-4645-98eb-d834db704fc8
keywords:
- reversebits fonction HLSL
topic_type:
- apiref
api_name:
- reversebits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b9f055764c04f552fe9d7afda2adf1e401352cf3fc3dd3ead16c4ca6377bd4fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853719"
---
# <a name="reversebits-function"></a>reversebits (fonction)

Inverse l’ordre des bits, par composant.

## <a name="syntax"></a>Syntaxe

``` syntax
uint reversebits(
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

Valeur d’entrée, avec l’ordre de bits inversé.

## <a name="remarks"></a>Remarques

Les versions surchargées suivantes sont également disponibles :

``` syntax
uint2 reversebits(uint2 value);
uint3 reversebits(uint3 value);
uint4 reversebits(uint4 value);
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

 

 




