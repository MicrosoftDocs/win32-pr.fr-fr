---
title: 'Texture1D :: MIPS. Operator, fonction'
description: Retourne une variable de ressource en lecture seule ou un Texture1D.
ms.assetid: 0b64f0d3-f9a1-474b-b229-d91d18922d5c
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
ms.openlocfilehash: 4713fe20fa52e948113a220969229c413c5dc4d1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104317069"
---
# <a name="texture1dmipsoperator----function"></a>Texture1D :: MIPS. Operator, fonction

Retourne une variable de ressource en lecture seule ou un [**Texture1D**](sm5-object-texture1d.md).

## <a name="syntax"></a>Syntaxe

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint pos
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

Type : **uint**

Position d’index. Contient la coordonnée x.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **R**

Variable de ressource en lecture seule.

## <a name="remarks"></a>Notes

### <a name="usage-example"></a>Exemple d'utilisation


```
Texture1D<float4> tex;
uint mip = 2;
uint pos = 1234;
float4 f = tex.mips[mip][pos];
      
```



Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Texture1D](sm5-object-texture1d.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




