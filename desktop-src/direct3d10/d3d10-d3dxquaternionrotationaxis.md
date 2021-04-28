---
description: 'D3DXQuaternionRotationAxis, fonction (D3DX10Math. h) : fait pivoter un Quaternion à propos d’un axe arbitraire.'
ms.assetid: 9673ef89-458f-4a25-960e-8f03179e78ba
title: D3DXQuaternionRotationAxis, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionRotationAxis
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 509df80023427a20125e1b5603e85424851a640e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108767"
---
# <a name="d3dxquaternionrotationaxis-function-d3dx10mathh"></a>D3DXQuaternionRotationAxis, fonction (D3DX10Math. h)

Fait pivoter un Quaternion à propos d’un axe arbitraire.

## <a name="syntax"></a>Syntaxe


```C++
D3DXQUATERNION* D3DXQuaternionRotationAxis(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXVECTOR3    *pV,
  _In_          FLOAT          Angle
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Pointeur vers le [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) qui est le résultat de l’opération.

</dd> <dt>

*PV* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Pointeur vers le [**D3DXVECTOR3**](d3d10-d3dxvector3.md) qui identifie l’axe sur lequel pivoter le Quaternion.

</dd> <dt>

*Angle* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Angle de rotation, en radians. Les angles sont mesurés dans le sens des aiguilles d’une montre sur l’axe de rotation vers l’origine.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Pointeur vers une structure D3DXQUATERNION pivotée autour de l’axe spécifié.

## <a name="remarks"></a>Notes 

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue. De cette façon, la fonction D3DXQuaternionRotationAxis peut être utilisée comme paramètre pour une autre fonction.

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

 

 
