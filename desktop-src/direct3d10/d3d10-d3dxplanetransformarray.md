---
description: Transforme un tableau de plans par une matrice. Les vecteurs qui décrivent chaque plan doivent être normalisés.
ms.assetid: 9529b06a-0575-4115-8d35-fc35a7bfb0bd
title: D3DXPlaneTransformArray, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneTransformArray
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 128b9c8c73db81faa877295e993504a7a510cd4a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043142"
---
# <a name="d3dxplanetransformarray-function-d3dx10mathh"></a>D3DXPlaneTransformArray, fonction (D3DX10Math. h)

Transforme un tableau de plans par une matrice. Les vecteurs qui décrivent chaque plan doivent être normalisés.

## <a name="syntax"></a>Syntaxe


```C++
D3DXPLANE* D3DXPlaneTransformArray(
  _Inout_       D3DXPLANE  *pOut,
  _In_          UINT       OutStride,
  _In_    const D3DXPLANE  *pP,
  _In_          UINT       PStride,
  _In_    const D3DXMATRIX *pM,
  _In_          UINT       n
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Pointeur vers la structure [**D3DXPLANE**](d3d10-d3dxplane.md) qui contient le plan transformé résultant. Consultez l’exemple.

</dd> <dt>

En *Progress* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

STRIDE de chaque plan transformé.

</dd> <dt>

*pp* \[ dans\]
</dt> <dd>

Type : **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***

Pointeur vers la structure D3DXPLANE d’entrée, qui contient le tableau de plans à transformer. Le vecteur (a, b, c) qui décrit le plan doit être normalisé avant l’appel de cette fonction. Consultez l’exemple.

</dd> <dt>

*PStride* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

STRIDE de chaque plan non transformé.

</dd> <dt>

*GCF* \[ dans\]
</dt> <dd>

Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Pointeur vers la structure source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , qui contient la permutation inverse des valeurs de transformation.

</dd> <dt>

*n* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de plans à transformer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Pointeur vers une structure D3DXPLANE représentant le plan transformé. Il s’agit de la même valeur retournée dans le paramètre moue pour que cette fonction puisse être utilisée en tant que paramètre pour une autre fonction.

## <a name="remarks"></a>Notes

Cet exemple transforme un plan en appliquant une échelle non uniforme.


```
#define ARRAYSIZE 4
D3DXPLANE planeNew[ARRAYSIZE];
D3DXPLANE plane[ARRAYSIZE];

for(int i = 0; i < ARRAYSIZE; i++)
{
    plane = D3DXPLANE( 0.0f, 1.0f, 1.0f, 0.0f );
    D3DXPlaneNormalize( &plane[i], &plane[i] );
}

D3DXMATRIX  matrix;
D3DXMatrixScaling( &matrix, 1.0f, 2.0f, 3.0f ); 
D3DXMatrixInverse( &matrix, NULL, &matrix );
D3DXMatrixTranspose( &matrix, &matrix );
D3DXPlaneTransformArray( &planeNew, sizeof (D3DXPLANE), &plane, 
                         sizeof (D3DXPLANE), &matrix, ARRAYSIZE );
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

 

 
