---
description: D3DXVec2TransformCoord, fonction (D3DX10Math. h)-transforme un vecteur 2D en une matrice donnée, en reprojetant le résultat dans w = 1.
ms.assetid: bb24204f-0c8e-4dc5-bcae-12e3033d1a39
title: D3DXVec2TransformCoord, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformCoord
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 67cdde2ba057f41d8a1929e6f641b22d05919b698fee61fd8351deb64b27f5ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990679"
---
# <a name="d3dxvec2transformcoord-function-d3dx10mathh"></a>D3DXVec2TransformCoord, fonction (D3DX10Math. h)

Transforme un vecteur 2D par une matrice donnée, en reprojetant le résultat dans w = 1.

## <a name="syntax"></a>Syntaxe


```C++
D3DXVECTOR2* D3DXVec2TransformCoord(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***

Pointeur vers le [**D3DXVECTOR2**](d3d10-d3dxvector2.md) qui est le résultat de l’opération.

</dd> <dt>

*PV* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Pointeur vers la structure D3DXVECTOR2 source.

</dd> <dt>

*GCF* \[ dans\]
</dt> <dd>

Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) source.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***

Pointeur vers une structure D3DXVECTOR2 qui est le vecteur transformé.

## <a name="remarks"></a>Remarques

Cette fonction transforme le vecteur, pV (x, y, 0, 1), par la matrice, pM, en projetant le résultat dans w = 1.

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue. De cette façon, la fonction D3DXVec2TransformCoord peut être utilisée comme paramètre pour une autre fonction.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
