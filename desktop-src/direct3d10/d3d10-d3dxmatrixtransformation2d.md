---
description: 'D3DXMatrixTransformation2D, fonction (D3DX10Math. h) : crée une matrice de transformation 2D qui représente des transformations dans le plan XY. Les arguments NULL sont traités comme des transformations d’identité.'
ms.assetid: 5b894c3b-a532-458a-bcbc-48fcd5c73c34
title: D3DXMatrixTransformation2D, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTransformation2D
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 754e755b0ee6e03692bf7eabeb4e751284478621f47c912d399eb101adfd98e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754289"
---
# <a name="d3dxmatrixtransformation2d-function-d3dx10mathh"></a>D3DXMatrixTransformation2D, fonction (D3DX10Math. h)

Crée une matrice de transformation 2D qui représente des transformations dans le plan XY. Les arguments **null** sont traités comme des transformations d’identité.

## <a name="syntax"></a>Syntaxe


```C++
D3DXMATRIX* D3DXMatrixTransformation2D(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR2 *pScalingCenter,
  _In_          FLOAT       ScalingRotation,
  _In_    const D3DXVECTOR2 *pScaling,
  _In_    const D3DXVECTOR2 *pRotationCenter,
  _In_          FLOAT       Rotation,
  _In_    const D3DXVECTOR2 *pTranslation
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) qui contient le résultat des transformations.

</dd> <dt>

*pScalingCenter* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Pointeur vers un [**D3DXVECTOR2**](d3d10-d3dxvector2.md), point identifiant le centre de mise à l’échelle. Si cet argument a la **valeur null**, une matrice Identity M <sub>SC</sub> est appliquée à la formule dans la section Notes.

</dd> <dt>

*ScalingRotation* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Pointeur vers le facteur de rotation de mise à l’échelle.

</dd> <dt>

*pScaling* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Pointeur vers une structure D3DXVECTOR2, point identifiant l’échelle. Si cet argument a la **valeur null**, une matrice d’identité MS est appliquée à la formule dans les notes.

</dd> <dt>

*pRotationCenter* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Pointeur vers une structure D3DXVECTOR2, point identifiant le centre de rotation. Si cet argument a la **valeur null**, une matrice Identity M <sub>RC</sub> est appliquée à la formule dans la section Notes.

</dd> <dt>

*Rotation* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Angle de rotation en radians.

</dd> <dt>

*pTranslation* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Pointeur vers une structure D3DXVECTOR2, identifiant la traduction. Si cet argument a la **valeur null**, une matrice Identity MT est appliquée à la formule dans la section Notes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Pointeur vers une structure D3DXMATRIX qui contient la matrice de transformation.

## <a name="remarks"></a>Remarques

Cette fonction calcule la matrice de transformation avec la formule suivante, avec la concaténation de matrice évaluée dans l’ordre de gauche à droite :

M<sub>out</sub> = (m<sub>SC</sub>) ⁻ ¹ \* (m<sub>SR</sub>) ⁻ ¹ \* MS \* m<sub>SR</sub> \* m<sub>SC</sub> \* (m<sub>RC</sub>) ⁻ ¹ \* m<sub>r</sub> \* m<sub>RC</sub> \* MT

où :

M<sub>out</sub> = matrice de sortie (moue)

M<sub>SC</sub> = matrice du centre de mise à l’échelle (pScalingCenter)

M<sub>SR</sub> = matrice de rotation de la mise à l’échelle (pScalingRotation)

MS = matrice de mise à l’échelle (pScaling)

M<sub>RC</sub> = Centre de rotation de la matrice (pRotationCenter)

M<sub>r</sub> = matrice de rotation (rotation)

MT = matrice de translation (pTranslation)

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue. De cette façon, la fonction D3DXMatrixTransformation2D peut être utilisée comme paramètre pour une autre fonction.

Pour les transformations 3D, utilisez [**D3DXMatrixTransformation**](d3d10-d3dxmatrixtransformation.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
