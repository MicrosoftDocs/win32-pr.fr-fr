---
description: 'D3DXMatrixLookAtRH, fonction (D3dx9math. h) : génère une matrice de droite et de gauche.'
ms.assetid: 10198bb9-a77e-4482-be6e-cc5f76eff30b
title: D3DXMatrixLookAtRH, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixLookAtRH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c9c98c0e8e0722b0b79fa12d4742cb328195d133
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107577"
---
# <a name="d3dxmatrixlookatrh-function-d3dx9mathh"></a>D3DXMatrixLookAtRH, fonction (D3dx9math. h)

Génère une matrice de droite et de gauche.

## <a name="syntax"></a>Syntaxe


```C++
D3DXMATRIX* D3DXMatrixLookAtRH(
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

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) qui est une matrice de recherche à droite.

## <a name="remarks"></a>Notes 

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* . De cette façon, la fonction **D3DXMatrixLookAtRH** peut être utilisée comme paramètre pour une autre fonction.

Cette fonction utilise la formule suivante pour calculer la matrice retournée.


```
zaxis = normal(Eye - At)
xaxis = normal(cross(Up, zaxis))
yaxis = cross(zaxis, xaxis)
    
 xaxis.x           yaxis.x           zaxis.x          0
 xaxis.y           yaxis.y           zaxis.y          0
 xaxis.z           yaxis.z           zaxis.z          0
 dot(xaxis, eye)   dot(yaxis, eye)   dot(zaxis, eye)  1
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixLookAtLH**](d3dxmatrixlookatlh.md)
</dt> </dl>

 

 




