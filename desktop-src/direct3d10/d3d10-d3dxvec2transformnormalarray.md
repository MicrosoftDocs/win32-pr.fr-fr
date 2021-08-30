---
description: D3DXVec2TransformNormalArray, fonction (D3DX10Math. h)-transforme un tableau (x, y, 0, 0) en une matrice donnée.
ms.assetid: a53f998a-f2a5-4e4b-bc1c-c1f46284d78b
title: D3DXVec2TransformNormalArray, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformNormalArray
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b28c80d20297e0ff0d4c3027424940067e4c447b388a5294d7a40bd52a290af9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989669"
---
# <a name="d3dxvec2transformnormalarray-function-d3dx10mathh"></a>D3DXVec2TransformNormalArray, fonction (D3DX10Math. h)

Transforme un tableau (x, y, 0, 0) en une matrice donnée.

## <a name="syntax"></a>Syntaxe


```C++
D3DXVECTOR2* D3DXVec2TransformNormalArray(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR2 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***

Pointeur vers le [**D3DXVECTOR2**](d3d10-d3dxvector2.md) qui est le résultat de l’opération.

</dd> <dt>

En *Progress* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

STRIDE entre les vecteurs dans le flux de données de sortie.

</dd> <dt>

*PV* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Pointeur vers le tableau D3DXVECTOR2 source.

</dd> <dt>

*VStride* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

STRIDE entre les vecteurs dans le flux de données d’entrée.

</dd> <dt>

*GCF* \[ dans\]
</dt> <dd>

Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) source.

</dd> <dt>

*n* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre d’éléments dans le tableau.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***

Pointeur vers une structure D3DXVECTOR2 qui est le tableau transformé.

## <a name="remarks"></a>Remarques

Cette fonction transforme le vecteur (pV->x, pV->y, 0, 0) par la matrice désignée par pM.

Si vous souhaitez transformer un normal, la matrice que vous transmettez à cette fonction doit être la transposer de l’inverse de la matrice que vous utiliseriez pour transformer un point.

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue. De cette façon, la fonction **D3DXVec2TransformNormalArray** peut être utilisée comme paramètre pour une autre fonction.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
