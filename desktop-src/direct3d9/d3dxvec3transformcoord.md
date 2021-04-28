---
description: D3DXVec3TransformCoord, fonction (D3dx9math. h)-transforme un vecteur 3D en une matrice donnée, en reprojetant le résultat dans w = 1.
ms.assetid: 4075b067-1e64-46c9-be73-5fa765c9cb9d
title: D3DXVec3TransformCoord, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformCoord
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e4e3514d4717262a7afab7ae808d747de3a1b635
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115627"
---
# <a name="d3dxvec3transformcoord-function-d3dx9mathh"></a>D3DXVec3TransformCoord, fonction (D3dx9math. h)

Transforme un vecteur 3D par une matrice donnée, en reprojetant le résultat dans w = 1.

## <a name="syntax"></a>Syntaxe


```C++
D3DXVECTOR3* D3DXVec3TransformCoord(
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

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) qui est le vecteur transformé.

## <a name="remarks"></a>Notes 

Cette fonction transforme le vecteur, *PV* (x, y, z, 1), par la matrice, *PM*, en projetant le résultat dans w = 1.

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* . De cette façon, la fonction **D3DXVec3TransformCoord** peut être utilisée comme paramètre pour une autre fonction.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec3Transform**](d3dxvec3transform.md)
</dt> <dt>

[**D3DXVec3TransformNormal**](d3dxvec3transformnormal.md)
</dt> </dl>

 

 




