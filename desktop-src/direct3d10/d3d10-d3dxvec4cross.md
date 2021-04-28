---
description: 'Fonction D3DXVec4Cross (D3DX10Math. h) : détermine le produit croisé en quatre dimensions.'
ms.assetid: 4f728fbd-cf5a-4d2e-ba4f-487616d83f6d
title: D3DXVec4Cross, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Cross
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: e52cc1adb1e48f65599b1bf7179f7953823f1e1c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102947"
---
# <a name="d3dxvec4cross-function-d3dx10mathh"></a>D3DXVec4Cross, fonction (D3DX10Math. h)

Détermine le produit croisé en quatre dimensions.

## <a name="syntax"></a>Syntaxe


```C++
D3DXVECTOR4* D3DXVec4Cross(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pV3
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Pointeur vers le [**D3DXVECTOR4**](d3d10-d3dxvector4.md) qui est le résultat de l’opération.

</dd> <dt>

*pV1* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Pointeur vers une structure D3DXVECTOR4 source.

</dd> <dt>

*pV2* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Pointeur vers une structure D3DXVECTOR4 source.

</dd> <dt>

*pV3* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Pointeur vers une structure D3DXVECTOR4 source.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Pointeur vers une structure D3DXVECTOR4 qui est le produit croisé.

## <a name="remarks"></a>Notes 

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue. De cette façon, la fonction D3DXVec4Cross peut être utilisée comme paramètre pour une autre fonction.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
