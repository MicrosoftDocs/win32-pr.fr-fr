---
description: 'D3DXFloat16To32Array, fonction (D3dx9math. h) : convertit un tableau de valeurs float de 16 bits en valeurs float 32 bits.'
ms.assetid: cabb2888-76e4-403b-99ab-f7d62478bf43
title: D3DXFloat16To32Array, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFloat16To32Array
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 171b148b112cf2064d0d9a3f89451ab0fc8c2d75
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107597"
---
# <a name="d3dxfloat16to32array-function-d3dx9mathh"></a>D3DXFloat16To32Array, fonction (D3dx9math. h)

Convertit un tableau de valeurs float de 16 bits en valeurs float 32 bits.

## <a name="syntax"></a>Syntaxe


```C++
FLOAT* D3DXFloat16To32Array(
  _Inout_       FLOAT       *pOut,
  _In_    const D3DXFLOAT16 *pIn,
  _In_          UINT        n
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ in, out\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)\***

Pointeur vers le tableau de valeurs float 32 bits.

</dd> <dt>

*code confidentiel* \[ dans\]
</dt> <dd>

Type : **const [**D3DXFLOAT16**](d3dxfloat16.md) \***

Pointeur vers un tableau de valeurs float 16 bits.

</dd> <dt>

*n* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre d’éléments dans le tableau.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **float**](../winprog/windows-data-types.md)\***

Pointeur vers un tableau de valeurs float 32 bits.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
