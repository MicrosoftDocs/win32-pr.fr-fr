---
description: Transforme un plan par une matrice. La matrice d’entrée est la permutation inverse de la transformation réelle.
ms.assetid: ded06eac-4086-47e8-bc55-c37959afc22d
title: D3DXPlaneTransform, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneTransform
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1b3c3390d84cd0d9c876afac6243ab90ca515e11
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323214"
---
# <a name="d3dxplanetransform-function-d3dx10mathh"></a>D3DXPlaneTransform, fonction (D3DX10Math. h)

Transforme un plan par une matrice. La matrice d’entrée est la permutation inverse de la transformation réelle.

## <a name="syntax"></a>Syntaxe


```C++
D3DXPLANE* D3DXPlaneTransform(
  _Inout_       D3DXPLANE  *pOut,
  _In_    const D3DXPLANE  *pP,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Pointeur vers le [**D3DXPLANE**](d3d10-d3dxplane.md) qui contient le plan transformé résultant. Consultez les exemples.

</dd> <dt>

*pp* \[ dans\]
</dt> <dd>

Type : **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***

Pointeur vers la structure D3DXPLANE d’entrée, qui contient le plan qui sera transformé. Le vecteur (a, b, c) qui décrit le plan doit être normalisé avant l’appel de cette fonction. Consultez les exemples.

</dd> <dt>

*GCF* \[ dans\]
</dt> <dd>

Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Pointeur vers la structure source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , qui contient les valeurs de transformation. Cette matrice doit contenir la transposer inverse des valeurs de transformation.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Pointeur vers une structure D3DXPLANE représentant le plan transformé. Il s’agit de la même valeur retournée dans le paramètre moue pour que cette fonction puisse être utilisée en tant que paramètre pour une autre fonction.

## <a name="remarks"></a>Notes

### <a name="examples"></a>Exemples

Cet exemple transforme un plan en appliquant une échelle non uniforme.


```
D3DXPLANE   planeNew;
D3DXPLANE   plane(0,1,1,0);
D3DXPlaneNormalize(&plane, &plane);

D3DXMATRIX  matrix;
D3DXMatrixScaling(&matrix, 1.0f,2.0f,3.0f); 
D3DXMatrixInverse(&matrix, NULL, &matrix);
D3DXMatrixTranspose(&matrix, &matrix);
D3DXPlaneTransform(&planeNew, &plane, &matrix);
```



Un plan est décrit par ax + by + CZ + DW = 0. Le premier plan est créé avec (a, b, c, d) = (0, 1, 1, 0), qui est un plan décrit par y + z = 0. Après la mise à l’échelle, le nouveau plan contient (a, b, c, d) = (0, 0.353 f, 0.235 f, 0), qui affiche le nouveau plan à décrire par 0.353 y + 0.235 z = 0.

Le paramètre pM contient la transposer inverse de la matrice de transformation. La permutation inverse est requise par cette méthode afin que le vecteur normal du plan transformé puisse également être correctement transformé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
