---
title: 'Texture3D :: MIPS. Operator, fonction'
description: 'Retourne une variable de ressource en lecture seule. | Texture3D :: MIPS. Operator, fonction'
ms.assetid: d5f6cb3b-4163-44c2-8379-ac8a412b1aa6
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
ms.openlocfilehash: 18ad563041c8ad0b601240f4353dad5bbc44ef418c267f72d07f0f753d12d993
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724499"
---
# <a name="texture3dmipsoperator----function"></a>Texture3D :: MIPS. Operator, fonction

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

Position d’index. Contient les coordonnées (x, y, z).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **R**

Variable de ressource en lecture seule.

## <a name="remarks"></a>Remarques

### <a name="usage-example"></a>Exemple d'utilisation


```
Texture3D<float4> tex;
uint mip = 2;
uint3 pos_xyz = {123, 456, 789};
float4 f = tex.mips[mip][pos_xyz];
        
```



Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Texture3D](sm5-object-texture3d.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




