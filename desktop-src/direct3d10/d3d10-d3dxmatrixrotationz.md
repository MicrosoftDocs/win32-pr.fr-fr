---
description: 'D3DXMatrixRotationZ, fonction (D3DX10Math. h) : crée une matrice qui pivote autour de l’axe z.'
ms.assetid: a168ea24-0cec-4e1b-a128-e9dadedf190b
title: D3DXMatrixRotationZ, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationZ
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ee87285765ccecd6a31e6a5ee8ae68bf59a45cea0ffc4fc52e11351e20b62388
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118541258"
---
# <a name="d3dxmatrixrotationz-function-d3dx10mathh"></a>D3DXMatrixRotationZ, fonction (D3DX10Math. h)

Crée une matrice qui pivote autour de l’axe z.

## <a name="syntax"></a>Syntaxe


```C++
D3DXMATRIX* D3DXMatrixRotationZ(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) qui est le résultat de l’opération.

</dd> <dt>

*Angle* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Angle de rotation, en radians. Les angles sont mesurés dans le sens des aiguilles d’une montre à partir de l’axe de rotation (côté positif) vers l’origine.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Pointeur vers une structure D3DXMATRIX pivotée autour de l’axe z.

## <a name="remarks"></a>Remarques

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue. De cette façon, la fonction D3DXMatrixRotationZ peut être utilisée comme paramètre pour une autre fonction.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
