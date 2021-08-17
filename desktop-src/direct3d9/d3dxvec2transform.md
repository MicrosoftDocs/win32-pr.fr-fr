---
description: D3DXVec2Transform, fonction (D3dx9math. h)-transforme un vecteur 2D par une matrice donnée.
ms.assetid: ccde9e34-2d99-4112-a8ed-3820d018b547
title: D3DXVec2Transform, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Transform
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2115b804dfda537508247785d897757a3f25263e8ee528fdacfb1a91b0515045
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117730798"
---
# <a name="d3dxvec2transform-function-d3dx9mathh"></a>D3DXVec2Transform, fonction (D3dx9math. h)

Transforme un vecteur 2D par une matrice donnée.

## <a name="syntax"></a>Syntaxe


```C++
D3DXVECTOR4* D3DXVec2Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Pointeur vers la structure [**D3DXVECTOR4**](d3dxvector4.md) qui est le résultat de l’opération.

</dd> <dt>

*PV* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Pointeur vers la structure [**D3DXVECTOR2**](d3dxvector2.md) source.

</dd> <dt>

*GCF* \[ dans\]
</dt> <dd>

Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) source.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Pointeur vers une structure [**D3DXVECTOR4**](d3dxvector4.md) qui est le vecteur transformé.

## <a name="remarks"></a>Remarques

Cette fonction transforme le vecteur *PV* (x, y, 0, 1) par la matrice *PM*.

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* . De cette façon, la fonction **D3DXVec2Transform** peut être utilisée comme paramètre pour une autre fonction.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec2TransformCoord**](d3dxvec2transformcoord.md)
</dt> <dt>

[**D3DXVec2TransformNormal**](d3dxvec2transformnormal.md)
</dt> </dl>

 

 




