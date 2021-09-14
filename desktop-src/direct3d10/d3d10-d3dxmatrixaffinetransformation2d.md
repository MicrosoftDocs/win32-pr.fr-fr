---
description: Crée une matrice de transformation affine 2D dans le plan x-y. Les arguments NULL sont traités comme des transformations d’identité.
ms.assetid: f46a307c-4566-42c8-8def-fb189116144e
title: D3DXMatrixAffineTransformation2D, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixAffineTransformation2D
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 223ef5d2d9a68c993553d52f5d4cf63e8b95dd3b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126855363"
---
# <a name="d3dxmatrixaffinetransformation2d-function-d3dx10mathh"></a>D3DXMatrixAffineTransformation2D, fonction (D3DX10Math. h)

Crée une matrice de transformation affine 2D dans le plan x-y. Les arguments **null** sont traités comme des transformations d’identité.

## <a name="syntax"></a>Syntaxe


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation2D(
  _In_       D3DXMATRIX  *pOut,
  _In_       FLOAT       Scaling,
  _In_ const D3DXVECTOR2 *pRotationCenter,
  _In_       FLOAT       Rotation,
  _In_ const D3DXVECTOR2 *pTranslation
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ dans\]
</dt> <dd>

Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Pointeur vers le [**D3DXMATRIX**](d3d10-d3dxmatrix.md) qui est le résultat de l’opération.

</dd> <dt>

*Mise à l’échelle* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Facteur d’échelle.

</dd> <dt>

*pRotationCenter* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Pointeur vers un [**D3DXVECTOR2**](d3d10-d3dxvector2.md), point identifiant le centre de rotation. Si cet argument a la **valeur null**, une matrice Identity M <sub>RC</sub> est appliquée à la formule dans la section Notes.

</dd> <dt>

*Rotation* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Angle de rotation.

</dd> <dt>

*pTranslation* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Pointeur vers un [**D3DXVECTOR2**](d3d10-d3dxvector2.md)qui représente la translation. Si cet argument a la **valeur null**, une matrice Identity MT est appliquée à la formule dans la section Notes.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Pointeur vers une structure D3DXMATRIX qui est une matrice de transformation affine.

## <a name="remarks"></a>Notes

Cette fonction calcule la matrice de transformation affine avec la formule suivante, avec la concaténation de matrice évaluée dans l’ordre de gauche à droite :

M<sub>out</sub> = MS \* (m<sub>RC</sub>)-1 \* M<sub>r</sub> \* m<sub>RC</sub> \* MT

où :

M<sub>out</sub> = matrice de sortie (moue)

MS = matrice de mise à l’échelle (mise à l’échelle)

M<sub>RC</sub> = Centre de rotation de la matrice (pRotationCenter)

M<sub>r</sub> = matrice de rotation (rotation)

MT = matrice de translation (pTranslation)

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue. De cette façon, la fonction D3DXMatrixAffineTransformation2D peut être utilisée comme paramètre pour une autre fonction.

Pour les transformations affines 3D, utilisez D3DXMatrixAffineTransformation.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
