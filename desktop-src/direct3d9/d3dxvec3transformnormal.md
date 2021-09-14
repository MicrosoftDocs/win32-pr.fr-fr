---
description: D3DXVec3TransformNormal, fonction (D3dx9math. h)-transforme le vecteur 3D normal par la matrice donnée.
ms.assetid: aa9531e1-b77a-4aad-8d59-2677908cb978
title: D3DXVec3TransformNormal, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformNormal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 50fb09a4619be9c3dbcff98bc939d6f99ad33bd4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008018"
---
# <a name="d3dxvec3transformnormal-function-d3dx9mathh"></a>D3DXVec3TransformNormal, fonction (D3dx9math. h)

Transforme le vecteur 3D normal par la matrice donnée.

## <a name="syntax"></a>Syntaxe


```C++
D3DXVECTOR3* D3DXVec3TransformNormal(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Pointeur vers la structure [**D3DXVECTOR3**](d3dxvector3.md) qui est le résultat de l’opération.

</dd> <dt>

*PV* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Pointeur vers la structure [**D3DXVECTOR3**](d3dxvector3.md) source.

</dd> <dt>

*GCF* \[ dans\]
</dt> <dd>

Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) source.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) qui est le vecteur transformé.

## <a name="remarks"></a>Notes

Cette fonction transforme le vecteur (*PV*->x, *PV*->y, *PV*->z, 0) par la matrice vers laquelle pointe *PM*.

Si vous souhaitez transformer un normal, la matrice que vous transmettez à cette fonction doit être la transposer de l’inverse de la matrice que vous utiliseriez pour transformer un point.

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* . De cette façon, la fonction **D3DXVec3TransformNormal** peut être utilisée comme paramètre pour une autre fonction.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




