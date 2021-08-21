---
description: 'D3DXMatrixTransformation, fonction (D3dx9math. h) : génère une matrice de transformation. Les arguments NULL sont traités comme des transformations d’identité.'
ms.assetid: 39042fc6-f489-4e44-ad3f-858ca395575d
title: D3DXMatrixTransformation, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTransformation
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 59656e1716dcf3fbc7844c8369de032f5e6e69776e5b89452a35d71512aea87c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044807"
---
# <a name="d3dxmatrixtransformation-function-d3dx9mathh"></a>D3DXMatrixTransformation, fonction (D3dx9math. h)

Crée une matrice de transformation. Les arguments **null** sont traités comme des transformations d’identité.

## <a name="syntax"></a>Syntaxe


```C++
D3DXMATRIX* D3DXMatrixTransformation(
  _Inout_       D3DXMATRIX     *pOut,
  _In_    const D3DXVECTOR3    *pScalingCenter,
  _In_    const D3DXQUATERNION *pScalingRotation,
  _In_    const D3DXVECTOR3    *pScaling,
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

*pScalingCenter* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , identifiant le point central du redimensionnement. Si cet argument a la **valeur null**, une matrice Identity M <sub>SC</sub> est appliquée à la formule dans la section Notes.

</dd> <dt>

*pScalingRotation* \[ dans\]
</dt> <dd>

Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) qui spécifie la rotation de la mise à l’échelle. Si cet argument a la **valeur null**, une matrice Identity M <sub>SR</sub> est appliquée à la formule dans la section Notes.

</dd> <dt>

*pScaling* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , le vecteur de mise à l’échelle. Si cet argument a la **valeur null**, une matrice d’identité MS est appliquée à la formule dans les notes.

</dd> <dt>

*pRotationCenter* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , un point qui identifie le centre de rotation. Si cet argument a la **valeur null**, une matrice Identity M <sub>RC</sub> est appliquée à la formule dans la section Notes.

</dd> <dt>

*protique* \[ dans\]
</dt> <dd>

Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) qui spécifie la rotation. Si cet argument a la **valeur null**, une matrice Identity M <sub>r</sub> est appliquée à la formule dans la section Notes.

</dd> <dt>

*pTranslation* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) représentant la translation. Si cet argument a la **valeur null**, une matrice Identity MT est appliquée à la formule dans la section Notes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) qui est la matrice de transformation.

## <a name="remarks"></a>Remarques

Cette fonction calcule la matrice de transformation avec la formule suivante, avec la concaténation de matrice évaluée dans l’ordre de gauche à droite :

M<sub>out</sub> = (m<sub>SC</sub>) ⁻ ¹ \* (m<sub>SR</sub>) ⁻ ¹ \* MS \* m<sub>SR</sub> \* m<sub>SC</sub> \* (m<sub>RC</sub>) ⁻ ¹ \* m<sub>r</sub> \* m<sub>RC</sub> \* MT

où :

M <sub>out</sub> = matrice de sortie (*moue*)

M <sub>SC</sub> = matrice du centre de mise à l’échelle (*pScalingCenter*)

M <sub>SR</sub> = matrice de rotation de la mise à l’échelle (*pScalingRotation*)

MS = matrice de mise à l’échelle (*pScaling*)

M <sub>RC</sub> = Centre de rotation de la matrice (*pRotationCenter*)

M <sub>r</sub> = matrice de rotation (*protique*)

MT = matrice de translation (*pTranslation*)

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* . De cette façon, la fonction **D3DXMatrixTransformation** peut être utilisée comme paramètre pour une autre fonction.

Pour les transformations 2D, utilisez [**D3DXMatrixTransformation2D**](d3dxmatrixtransformation2d.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixAffineTransformation**](d3dxmatrixaffinetransformation.md)
</dt> <dt>

[Transformations (Direct3D 9)](transforms.md)
</dt> </dl>

 

 




