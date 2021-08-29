---
description: 'D3DXMatrixAffineTransformation, fonction (D3dx9math. h) : génère une matrice de transformation affine 3D. Les arguments NULL sont traités comme des transformations d’identité.'
ms.assetid: 54eac78f-57be-4a24-8dfb-0b519e97d6ca
title: D3DXMatrixAffineTransformation, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixAffineTransformation
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 91e3a29daebcc41dbb1df022b8423a82810d5a660905474a4c6d5f14d9fc60d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791709"
---
# <a name="d3dxmatrixaffinetransformation-function-d3dx9mathh"></a>D3DXMatrixAffineTransformation, fonction (D3dx9math. h)

Crée une matrice de transformation affine 3D. Les arguments **null** sont traités comme des transformations d’identité.

## <a name="syntax"></a>Syntaxe


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation(
  _Inout_       D3DXMATRIX     *pOut,
  _In_          FLOAT          Scaling,
  _In_    const D3DXVECTOR3    *pRotationCenter,
  _In_    const D3DXQUATERNION *pRotation,
  _In_    const D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) qui est le résultat de l’opération.

</dd> <dt>

*Mise à l’échelle* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Facteur d’échelle.

</dd> <dt>

*pRotationCenter* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , point identifiant le centre de rotation. Si cet argument a la **valeur null**, une matrice Identity M <sub>RC</sub> est appliquée à la formule dans la section Notes.

</dd> <dt>

*protique* \[ dans\]
</dt> <dd>

Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) qui spécifie la rotation. Si cet argument a la **valeur null**, une matrice Identity M <sub>r</sub> est appliquée à la formule dans la section Notes.

</dd> <dt>

*pTranslation* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) représentant la traduction. Si cet argument a la **valeur null**, une matrice Identity MT est appliquée à la formule dans la section Notes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) qui est une matrice de transformation affine.

## <a name="remarks"></a>Remarques

Cette fonction calcule la matrice de transformation affine avec la formule suivante, avec la concaténation de matrice évaluée dans l’ordre de gauche à droite :

M<sub>out</sub> = MS \* (M<sub>RC</sub>) ⁻ ¹ \* m<sub>r</sub> \* m<sub>RC</sub> \* MT

où :

M <sub>out</sub> = matrice de sortie (*moue*)

MS = matrice de mise à l’échelle (*mise à l’échelle*)

M <sub>RC</sub> = Centre de rotation de la matrice (*pRotationCenter*)

M <sub>r</sub> = matrice de rotation (*protique*)

MT = matrice de translation (*pTranslation*)

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue. De cette façon, la fonction **D3DXMatrixAffineTransformation** peut être utilisée comme paramètre pour une autre fonction.

Pour les transformations affines 2D, utilisez [**D3DXMatrixAffineTransformation2D**](d3dxmatrixaffinetransformation2d.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixTransformation**](d3dxmatrixtransformation.md)
</dt> <dt>

[Transformations (Direct3D 9)](transforms.md)
</dt> </dl>

 

 
