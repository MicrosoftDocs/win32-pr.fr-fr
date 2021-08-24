---
description: 'D3DXFloat16To32Array, fonction (D3DX10Math. h) : convertit un tableau de valeurs float de 16 bits en valeurs float 32 bits.'
ms.assetid: cf07a21d-9ea3-4fbe-ab8f-564e2bbb8d60
title: D3DXFloat16To32Array, fonction (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 00e5b7847e89687cf0b9414d3845652c0943661a2fc801fd4016eb54a8677c91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677749"
---
# <a name="d3dxfloat16to32array-function-d3dx10mathh"></a>D3DXFloat16To32Array, fonction (D3DX10Math. h)

Convertit un tableau de valeurs float de 16 bits en valeurs float 32 bits.

## <a name="syntax"></a>Syntaxe


```C++
FLOAT* D3DXFloat16To32Array(
  _In_       FLOAT       *pOut,
  _In_ const D3DXFLOAT16 *pIn,
  _In_       UINT        n
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)\***

Pointeur vers le tableau de valeurs float 32 bits.

</dd> <dt>

*code confidentiel* \[ dans\]
</dt> <dd>

Type : **const [**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md) \***

Pointeur vers un tableau de valeurs float 16 bits.

</dd> <dt>

*n* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre d’éléments dans le tableau.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **float**](../winprog/windows-data-types.md)\***

Pointeur vers un tableau de valeurs float 32 bits.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
