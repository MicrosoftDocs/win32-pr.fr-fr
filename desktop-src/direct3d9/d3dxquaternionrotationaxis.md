---
description: 'D3DXQuaternionRotationAxis, fonction (D3dx9math. h) : fait pivoter un Quaternion à propos d’un axe arbitraire.'
ms.assetid: 9ff0fe2c-54d6-482c-84e1-f38e3c57d8dd
title: D3DXQuaternionRotationAxis, fonction (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a5cbbdc3603b5e2eb7a03f592d44fa88f07ef015
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118017"
---
# <a name="d3dxquaternionrotationaxis-function-d3dx9mathh"></a>D3DXQuaternionRotationAxis, fonction (D3dx9math. h)

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

Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Pointeur vers la structure [**D3DXQUATERNION**](d3dxquaternion.md) qui est le résultat de l’opération.

</dd> <dt>

*PV* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Pointeur vers la structure [**D3DXVECTOR3**](d3dxvector3.md) qui identifie l’axe sur lequel pivoter le Quaternion.

</dd> <dt>

*Angle* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Angle de rotation, en radians. Les angles sont mesurés dans le sens des aiguilles d’une montre sur l’axe de rotation vers l’origine.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) pivotée autour de l’axe spécifié.

## <a name="remarks"></a>Notes 

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* . De cette façon, la fonction **D3DXQuaternionRotationAxis** peut être utilisée comme paramètre pour une autre fonction.

Utilisez [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXQuaternionRotationMatrix**](d3dxquaternionrotationmatrix.md)
</dt> <dt>

[**D3DXQuaternionRotationYawPitchRoll**](d3dxquaternionrotationyawpitchroll.md)
</dt> </dl>

 

 
