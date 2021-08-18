---
description: 'Fonction D3DXQuaternionToAxisAngle (D3dx9math. h) : calcule l’axe et l’angle de rotation d’un Quaternion.'
ms.assetid: 6efd0a68-7641-403e-8ae2-c715b705b36e
title: D3DXQuaternionToAxisAngle, fonction (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8b22b0a4c094a47e412172807c42cf25dc3c89342cf8e7e4ece9e731d9014bd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117731287"
---
# <a name="d3dxquaterniontoaxisangle-function-d3dx9mathh"></a>D3DXQuaternionToAxisAngle, fonction (D3dx9math. h)

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

Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Pointeur vers la structure [**D3DXQUATERNION**](d3dxquaternion.md) source.

</dd> <dt>

*pAxis* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Cette fonction retourne un pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) qui identifie l’axe de rotation du Quaternion.

</dd> <dt>

*pAngle* \[ in, out\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)\***

Cette fonction retourne un pointeur vers une valeur FLOAT qui identifie l’angle de rotation du quaternion en radians.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

Utilisez [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
