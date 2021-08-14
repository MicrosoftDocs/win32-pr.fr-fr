---
description: 'D3DXMatrixReflect, fonction (D3DX10Math. h) : crée une matrice qui reflète le système de coordonnées d’un plan.'
ms.assetid: bd2c5905-780e-4fac-a848-d7dbcfc390c6
title: D3DXMatrixReflect, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixReflect
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c744c529025e0bfa1a619d41cc3e564c2be3203887b1ebbbbe047542ccce3370
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118810034"
---
# <a name="d3dxmatrixreflect-function-d3dx10mathh"></a>D3DXMatrixReflect, fonction (D3DX10Math. h)

Crée une matrice qui reflète le système de coordonnées d’un plan.

## <a name="syntax"></a>Syntaxe


```C++
D3DXMATRIX* D3DXMatrixReflect(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXPLANE  *pPlane
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) qui est le résultat de l’opération.

</dd> <dt>

*pPlane* \[ dans\]
</dt> <dd>

Type : **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***

Pointeur vers le [**D3DXPLANE**](d3d10-d3dxplane.md)source.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Pointeur vers une structure D3DXMATRIX qui reflète le système de coordonnées du plan source.

## <a name="remarks"></a>Remarques

Cette fonction normalise l’équation plan avant de créer la matrice réfléchie.

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue. De cette façon, la fonction D3DXMatrixReflect peut être utilisée comme paramètre pour une autre fonction.

Cette fonction utilise la formule suivante pour calculer la matrice retournée.


```
P = normalize(Plane);
    
-2 * P.a * P.a + 1  -2 * P.b * P.a      -2 * P.c * P.a        0
-2 * P.a * P.b      -2 * P.b * P.b + 1  -2 * P.c * P.b        0
-2 * P.a * P.c      -2 * P.b * P.c      -2 * P.c * P.c + 1    0
-2 * P.a * P.d      -2 * P.b * P.d      -2 * P.c * P.d        1
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

 

 
