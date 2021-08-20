---
description: D3DXQuaternionMultiply, fonction (D3DX10Math. h)-multiplie deux quaternions.
ms.assetid: f549e383-9c39-47a9-84e4-82365bdf1155
title: D3DXQuaternionMultiply, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionMultiply
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 87d1b386409047eefc3e70ce5007082dda2158122ccfe4e2d3b2bea683a25a49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991089"
---
# <a name="d3dxquaternionmultiply-function-d3dx10mathh"></a>D3DXQuaternionMultiply, fonction (D3DX10Math. h)

Multiplie deux quaternions.

## <a name="syntax"></a>Syntaxe


```C++
D3DXQUATERNION* D3DXQuaternionMultiply(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXQUATERNION**](d3d10-d3dxquaternion.md)\***

Pointeur vers le [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) qui est le résultat de l’opération.

</dd> <dt>

*pQ1* \[ dans\]
</dt> <dd>

Type : **const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) \***

Pointeur vers une structure [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) source.

</dd> <dt>

*pQ2* \[ dans\]
</dt> <dd>

Type : **const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) \***

Pointeur vers une structure [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) source.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Pointeur vers une structure [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) qui est le produit de deux quaternions.

## <a name="remarks"></a>Remarques

Le résultat représente la rotation Q1 suivie de la rotation Q2 (out = 2e trimestre \* Q1). Pour ce faire, **D3DXQuaternionMultiply** conserve la même sémantique que [**D3DXMatrixMultiply**](d3d10-d3dxmatrixmultiply.md) , car les quaternions d’unité peuvent être considérés comme une autre façon de représenter des matrices de rotation.

Les transformations sont concaténées dans le même ordre pour les fonctions **D3DXQuaternionMultiply** et [**D3DXMatrixMultiply**](d3d10-d3dxmatrixmultiply.md) . Par exemple, en supposant que mX et mY représentent les mêmes rotations que qX et qY, m et q représenteront les mêmes rotations.


```
D3DXMatrixMultiply(&m, &mX, &mY);
D3DXQuaternionMultiply(&q, &qX, &qY);
```



La multiplication de quaternions n’est pas commutative.

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue. De cette façon, la fonction **D3DXQuaternionMultiply** peut être utilisée comme paramètre pour une autre fonction.

Utilisez [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
