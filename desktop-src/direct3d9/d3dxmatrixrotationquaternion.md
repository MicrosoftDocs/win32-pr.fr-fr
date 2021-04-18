---
description: Génère une matrice de rotation à partir d’un Quaternion.
ms.assetid: e590058c-772b-4eef-aab0-a12bb04c299a
title: D3DXMatrixRotationQuaternion, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationQuaternion
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 275a369da106e9f114ce47286f0f6ea9ce381ecb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106525902"
---
# <a name="d3dxmatrixrotationquaternion-function-d3dx9mathh"></a>D3DXMatrixRotationQuaternion, fonction (D3dx9math. h)

Génère une matrice de rotation à partir d’un Quaternion.

## <a name="syntax"></a>Syntaxe


```C++
D3DXMATRIX* D3DXMatrixRotationQuaternion(
  _Inout_       D3DXMATRIX     *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) qui est le résultat de l’opération.

</dd> <dt>

*PQ* \[ dans\]
</dt> <dd>

Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Pointeur vers la structure [**D3DXQUATERNION**](d3dxquaternion.md) source.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) construite à partir du Quaternion source.

## <a name="remarks"></a>Notes

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* . De cette façon, la fonction **D3DXMatrixRotationQuaternion** peut être utilisée comme paramètre pour une autre fonction.

Pour plus d’informations sur le calcul des valeurs de Quaternion à partir d’un vecteur de direction (x, y, z) et d’un angle de rotation, consultez [**D3DXQUATERNION**](d3dxquaternion.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixRotationAxis**](d3dxmatrixrotationaxis.md)
</dt> <dt>

[**D3DXMatrixRotationX**](d3dxmatrixrotationx.md)
</dt> <dt>

[**D3DXMatrixRotationY**](d3dxmatrixrotationy.md)
</dt> <dt>

[**D3DXMatrixRotationYawPitchRoll**](d3dxmatrixrotationyawpitchroll.md)
</dt> <dt>

[**D3DXMatrixRotationZ**](d3dxmatrixrotationz.md)
</dt> </dl>

 

 




