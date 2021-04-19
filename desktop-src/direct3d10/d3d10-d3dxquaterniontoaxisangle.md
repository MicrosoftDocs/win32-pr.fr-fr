---
description: Calcule l’axe et l’angle de rotation d’un Quaternion.
ms.assetid: 1e81b88b-071d-46f1-b640-c70d063a14d1
title: D3DXQuaternionToAxisAngle, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionToAxisAngle
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0fabba670bbfe83a3032e5a6fa78f5db16c89b3c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106529626"
---
# <a name="d3dxquaterniontoaxisangle-function-d3dx10mathh"></a>D3DXQuaternionToAxisAngle, fonction (D3DX10Math. h)

Calcule l’axe et l’angle de rotation d’un Quaternion.

## <a name="syntax"></a>Syntaxe


```C++
void D3DXQuaternionToAxisAngle(
  _In_    const D3DXQUATERNION *pQ,
  _Inout_       D3DXVECTOR3    *pAxis,
  _Inout_       FLOAT          *pAngle
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PQ* \[ dans\]
</dt> <dd>

Type : **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Pointeur vers le [**D3DXQUATERNION**](d3d10-d3dxquaternion.md)source.

</dd> <dt>

*pAxis* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Cette fonction retourne un pointeur vers un [**D3DXVECTOR3**](d3d10-d3dxvector3.md) qui identifie l’axe de rotation du Quaternion.

</dd> <dt>

*pAngle* \[ in, out\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)\***

Cette fonction retourne un pointeur vers une valeur FLOAT qui identifie l’angle de rotation du quaternion en radians.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

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

 

 
