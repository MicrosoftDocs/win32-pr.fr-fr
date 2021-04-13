---
description: Transforme un tableau (x, y, z, 1) en une matrice donnée.
ms.assetid: fd7ab674-5e42-4265-afad-ae5a00dabcdb
title: D3DXVec3TransformArray, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0b515c98be82aa47801b333c4b25680e0e464b2e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322726"
---
# <a name="d3dxvec3transformarray-function-d3dx9mathh"></a>D3DXVec3TransformArray, fonction (D3dx9math. h)

Transforme un tableau (x, y, z, 1) en une matrice donnée.

## <a name="syntax"></a>Syntaxe


```C++
D3DXVECTOR4* D3DXVec3TransformArray(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR3 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Pointeur vers le tableau [**D3DXVECTOR4**](d3dxvector4.md) qui est le résultat de l’opération.

</dd> <dt>

En *Progress* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

STRIDE entre les vecteurs dans le flux de données de sortie.

</dd> <dt>

*PV* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Pointeur vers le tableau [**D3DXVECTOR3**](d3dxvector3.md) source.

</dd> <dt>

*VStride* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

STRIDE entre les vecteurs dans le flux de données d’entrée.

</dd> <dt>

*GCF* \[ dans\]
</dt> <dd>

Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) source.

</dd> <dt>

*n* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre d’éléments dans le tableau.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Pointeur vers un tableau transformé [**D3DXVECTOR4**](d3dxvector4.md) .

## <a name="remarks"></a>Notes

Cette fonction transforme *le tableau (* x, y, z, 1) par la matrice *PM*.

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* . De cette façon, la fonction **D3DXVec3TransformArray** peut être utilisée comme paramètre pour une autre fonction.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
