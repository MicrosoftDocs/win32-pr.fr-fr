---
title: 'Texture2DArray :: MIPS. Operator, fonction'
description: 'Retourne une variable de ressource en lecture seule. | Texture2DArray :: MIPS. Operator, fonction'
ms.assetid: 66639bf6-74dd-4c69-9cc1-74cc9314de57
keywords:
- mips. Fonction d’opérateur HLSL
topic_type:
- apiref
api_name:
- mips.Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f5dff48f721e45ef7853c125b1d7d0d32d5cb311a3dbc3b31d4100f3038a8fdc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724590"
---
# <a name="texture2darraymipsoperator----function"></a>Texture2DArray :: MIPS. Operator, fonction

Retourne une variable de ressource en lecture seule.

## <a name="syntax"></a>Syntaxe

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint3 pos
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*mipSlice* \[ dans\]
</dt> <dd>

Type : **uint**

Index de la tranche MIP.

</dd> <dt>

*pos* \[ dans\]
</dt> <dd>

Type : **uint3**

Position d’index. Le premier et le deuxième composant contiennent les coordonnées (x, y). Le troisième composant indique la tranche de tableau souhaitée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **R**

Variable de ressource en lecture seule.

## <a name="remarks"></a>Remarques

### <a name="usage-example"></a>Exemple d'utilisation


```
Texture2DArray<float4> tex;
uint mip = 2;
uint2 pos_xy_and_array = {123, 456, 3};
float4 f = tex.mips[mip][pos_xy_and_array];
        
```



Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Texture2DArray](sm5-object-texture2darray.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




