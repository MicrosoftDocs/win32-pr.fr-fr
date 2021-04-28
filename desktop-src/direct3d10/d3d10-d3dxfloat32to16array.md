---
description: 'D3DXFloat32To16Array, fonction (D3DX10Math. h) : convertit un tableau de valeurs float 32 bits en valeurs float 16 bits.'
ms.assetid: 2114cf25-cc83-4c4a-9db5-ecc0f8ff1e85
title: D3DXFloat32To16Array, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFloat32To16Array
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 600cc2cd333aaea08b38c252c206c1a74c1ca059
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103517"
---
# <a name="d3dxfloat32to16array-function-d3dx10mathh"></a>D3DXFloat32To16Array, fonction (D3DX10Math. h)

Convertit un tableau de valeurs float 32 bits en valeurs float 16 bits.

## <a name="syntax"></a>Syntaxe


```C++
D3DXFLOAT16* D3DXFloat32To16Array(
  _In_       D3DXFLOAT16 *pOut,
  _In_ const FLOAT       *pIn,
  _In_       UINT        n
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ dans\]
</dt> <dd>

Type : **[ **D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***

Pointeur vers le tableau de valeurs float de 16 bits.

</dd> <dt>

*code confidentiel* \[ dans\]
</dt> <dd>

Type : **const [**float**](../winprog/windows-data-types.md) \***

Pointeur vers un tableau de valeurs float 32 bits.

</dd> <dt>

*n* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre d’éléments dans le tableau.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***

Pointeur vers un tableau de valeurs float 16 bits.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
