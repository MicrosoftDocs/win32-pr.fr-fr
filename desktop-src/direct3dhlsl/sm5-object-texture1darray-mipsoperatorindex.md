---
title: 'Texture1DArray :: MIPS. Operator, fonction'
description: 'Retourne une variable de ressource en lecture seule. | Texture1DArray :: MIPS. Operator, fonction'
ms.assetid: b8f2ef78-4b50-4051-a00f-5b81cd77d1e0
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
ms.openlocfilehash: cbe2d1116839cede8dda69f1b0b8cf9a049595e9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918195"
---
# <a name="texture1darraymipsoperator----function"></a>Texture1DArray :: MIPS. Operator, fonction

Retourne une variable de ressource en lecture seule.

## <a name="syntax"></a>Syntaxe

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint2 pos
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

Type : **uint2**

Position d’index. Le premier composant contient la coordonnée x. Le deuxième composant indique la tranche de tableau souhaitée.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **R**

Variable de ressource en lecture seule.

## <a name="remarks"></a>Notes

### <a name="usage-example"></a>Exemple d'utilisation


```
Texture1DArray<float4> tex;
uint mip = 2;
uint2 pos_x_and_array = {1234, 3};
float4 f = tex.mips[mip][pos_x_and_array];        
        
```



Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Texture1DArray](sm5-object-texture1darray.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




