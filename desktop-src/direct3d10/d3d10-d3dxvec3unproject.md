---
description: D3DXVec3Unproject, fonction (D3DX10Math. h)-projette un vecteur de l’espace à l’écran dans l’espace de l’objet.
ms.assetid: c96d732d-0594-42b4-bc54-458a313f153e
title: D3DXVec3Unproject, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Unproject
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 14f8bb3d75d1a949919d401babb47987fbb88a7cac82f017947f069df4b99e6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497862"
---
# <a name="d3dxvec3unproject-function-d3dx10mathh"></a>D3DXVec3Unproject, fonction (D3DX10Math. h)

Projette un vecteur de l’espace à l’écran dans l’espace de l’objet.

## <a name="syntax"></a>Syntaxe


```C++
D3DXVECTOR3* D3DXVec3Unproject(
  _Inout_       D3DXVECTOR3    *pOut,
  _In_    const D3DXVECTOR3    *pV,
  _In_    const D3D10_VIEWPORT *pViewport,
  _In_    const D3DXMATRIX     *pProjection,
  _In_    const D3DXMATRIX     *pView,
  _In_    const D3DXMATRIX     *pWorld
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Pointeur vers le [**D3DXVECTOR3**](d3d10-d3dxvector3.md) qui est le résultat de l’opération.

</dd> <dt>

*PV* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Pointeur vers la structure D3DXVECTOR3 source.

</dd> <dt>

*pViewport* \[ dans\]
</dt> <dd>

Type : **const [**D3D10 \_ VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport) \***

Pointeur vers une [**\_ fenêtre d’affichage D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)représentant la fenêtre d’affichage.

</dd> <dt>

*pProjection* \[ dans\]
</dt> <dd>

Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Pointeur vers une structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) représentant la matrice de projection.

</dd> <dt>

*pview* \[ dans\]
</dt> <dd>

Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Pointeur vers une structure D3DXMATRIX, représentant la matrice de vue.

</dd> <dt>

*pWorld* \[ dans\]
</dt> <dd>

Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Pointeur vers une structure D3DXMATRIX représentant la matrice universelle.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Pointeur vers une structure D3DXVECTOR3 qui est le vecteur projeté de l’espace à l’écran jusqu’à l’espace de l’objet.

## <a name="remarks"></a>Remarques

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue. De cette façon, la fonction D3DXVec3Unproject peut être utilisée comme paramètre pour une autre fonction.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
