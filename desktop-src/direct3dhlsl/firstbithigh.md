---
title: firstbithigh (fonction)
description: Obtient l’emplacement du premier bit défini à partir du bit de poids le plus élevé et du travail vers le bas, par composant.
ms.assetid: 0fa89a9e-1706-44f7-8dd3-c37af5c11ddc
keywords:
- firstbithigh fonction HLSL
topic_type:
- apiref
api_name:
- firstbithigh
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1c62b6f090126887930415fc408da4f4a6c17bc4a99429db61fd298960c07e6b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949699"
---
# <a name="firstbithigh-function"></a>firstbithigh (fonction)

Obtient l’emplacement du premier bit défini à partir du bit de poids le plus élevé et du travail vers le bas, par composant.

## <a name="syntax"></a>Syntaxe

``` syntax
int firstbithigh(
  in int value
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ dans\]
</dt> <dd>

Type : **[ **int**](/windows/desktop/WinProg/windows-data-types)**

Valeur d'entrée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **int**](/windows/desktop/WinProg/windows-data-types)**

Emplacement du premier bit défini.

## <a name="remarks"></a>Remarques

Pour un entier signé, le premier bit significatif est zéro pour un nombre négatif.

Les versions surchargées suivantes sont également disponibles :

``` syntax
int2 firstbithigh(int2 value);
int3 firstbithigh(int3 value);
int4 firstbithigh(int4 value);
uint firstbithigh(uint value);
uint2 firstbithigh(uint2 value);
uint3 firstbithigh(uint3 value);
uint4 firstbithigh(uint4 value);
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

 

 