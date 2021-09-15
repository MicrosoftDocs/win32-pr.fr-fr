---
description: 'D3DXMatrixLookAtLH, fonction (D3dx9math. h) : génère une matrice de gauche et de droite.'
ms.assetid: bf34d3d8-725d-4fc1-b4c8-6c98f9dac329
title: D3DXMatrixLookAtLH, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixLookAtLH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 94a423e700c4a42e2ae7f7e522d83a5a4bd9bf3a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404319"
---
# <a name="d3dxmatrixlookatlh-function-d3dx9mathh"></a>D3DXMatrixLookAtLH, fonction (D3dx9math. h)

Crée une matrice de gauche et de droite.

## <a name="syntax"></a>Syntaxe


```C++
D3DXMATRIX* D3DXMatrixLookAtLH(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pEye,
  _In_    const D3DXVECTOR3 *pAt,
  _In_    const D3DXVECTOR3 *pUp
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) qui est le résultat de l’opération.

</dd> <dt>

*pEye* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Pointeur vers la structure [**D3DXVECTOR3**](d3dxvector3.md) qui définit le point oculaire. Cette valeur est utilisée dans la traduction.

</dd> <dt>

*pAt* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Pointeur vers la structure [**D3DXVECTOR3**](d3dxvector3.md) qui définit la cible de l’apparence de la caméra.

</dd> <dt>

*pUp* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Pointeur vers la structure [**D3DXVECTOR3**](d3dxvector3.md) qui définit le monde actuel, généralement \[ 0, 1, 0 \] .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) qui est une matrice de recherche gauche.

## <a name="remarks"></a>Notes

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* . De cette façon, la fonction **D3DXMatrixLookAtLH** peut être utilisée comme paramètre pour une autre fonction.

Cette fonction utilise la formule suivante pour calculer la matrice retournée.


```
zaxis = normal(At - Eye)
xaxis = normal(cross(Up, zaxis))
yaxis = cross(zaxis, xaxis)
    
 xaxis.x           yaxis.x           zaxis.x          0
 xaxis.y           yaxis.y           zaxis.y          0
 xaxis.z           yaxis.z           zaxis.z          0
-dot(xaxis, eye)  -dot(yaxis, eye)  -dot(zaxis, eye)  1
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixLookAtRH**](d3dxmatrixlookatrh.md)
</dt> </dl>

 

 




