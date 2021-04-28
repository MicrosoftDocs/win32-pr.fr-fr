---
description: 'D3DXMatrixOrthoLH, fonction (D3DX10Math. h) : génère une matrice de projection orthographique de gauche.'
ms.assetid: 67bec4a3-2126-4f5a-9301-97faa6dc6e84
title: D3DXMatrixOrthoLH, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoLH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 73cd5d9b809a0eb442db57e91c3788d2548a8c33
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113097"
---
# <a name="d3dxmatrixortholh-function-d3dx10mathh"></a>D3DXMatrixOrthoLH, fonction (D3DX10Math. h)

Génère une matrice de projection orthographique de gauche.

## <a name="syntax"></a>Syntaxe


```C++
D3DXMATRIX* D3DXMatrixOrthoLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Pointeur vers le [**D3DXMATRIX**](d3d10-d3dxmatrix.md)résultant.

</dd> <dt>

*w* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Largeur du volume de la vue.

</dd> <dt>

*h* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Hauteur du volume de la vue.

</dd> <dt>

*Zn* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Valeur z minimale du volume de la vue, appelée z-near.

</dd> <dt>

*ZF* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Valeur z maximale du volume de la vue, appelée z-Far.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Pointeur vers le [**D3DXMATRIX**](d3d10-d3dxmatrix.md)résultant.

## <a name="remarks"></a>Notes 

Tous les paramètres de la fonction D3DXMatrixOrthoLH sont des distances dans l’espace de l’appareil photo. Les paramètres décrivent les dimensions du volume de la vue.

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue. De cette façon, la fonction D3DXMatrixOrthoLH peut être utilisée comme paramètre pour une autre fonction.

Cette fonction utilise la formule suivante pour calculer la matrice retournée.


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zf-zn)   0
0    0    zn/(zn-zf)  1
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
