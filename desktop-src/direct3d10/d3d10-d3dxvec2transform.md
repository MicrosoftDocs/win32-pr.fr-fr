---
description: D3DXVec2Transform, fonction (D3DX10Math. h)-transforme un vecteur 2D par une matrice donnée.
ms.assetid: 4b57eb7f-fae9-48ac-a806-510da75d25a6
title: D3DXVec2Transform, fonction (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b1d8eed447b56e6f379ffe96cbbcb4820fbdaf14
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108357"
---
# <a name="d3dxvec2transform-function-d3dx10mathh"></a>D3DXVec2Transform, fonction (D3DX10Math. h)

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

Type : **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Pointeur vers la structure [**D3DXVECTOR4**](d3d10-d3dxvector4.md) qui est le résultat de l’opération.

</dd> <dt>

*PV* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Pointeur vers le [**D3DXVECTOR2**](d3d10-d3dxvector2.md)source.

</dd> <dt>

*GCF* \[ dans\]
</dt> <dd>

Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) source.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Pointeur vers une structure D3DXVECTOR4 qui est le vecteur transformé.

## <a name="remarks"></a>Notes 

Cette fonction transforme le vecteur pV (x, y, 0, 1) par la matrice pM.

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue. De cette façon, la fonction D3DXVec2Transform peut être utilisée comme paramètre pour une autre fonction.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
