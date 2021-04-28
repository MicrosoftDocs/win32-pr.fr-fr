---
description: 'D3DXQuaternionRotationYawPitchRoll, fonction (D3dx9math. h) : génère un Quaternion avec le lacet, le tangage et le roulis donnés.'
ms.assetid: be4a3bd5-114b-4652-8e0a-e51338317c16
title: D3DXQuaternionRotationYawPitchRoll, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionRotationYawPitchRoll
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 541e181425782662c6d40affc22c829b4ba343ab
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117997"
---
# <a name="d3dxquaternionrotationyawpitchroll-function-d3dx9mathh"></a>D3DXQuaternionRotationYawPitchRoll, fonction (D3dx9math. h)

Génère un Quaternion avec le lacet, le tangage et le roulis donnés.

## <a name="syntax"></a>Syntaxe


```C++
D3DXQUATERNION* D3DXQuaternionRotationYawPitchRoll(
  _Inout_ D3DXQUATERNION *pOut,
  _In_    FLOAT          Yaw,
  _In_    FLOAT          Pitch,
  _In_    FLOAT          Roll
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Pointeur vers la structure [**D3DXQUATERNION**](d3dxquaternion.md) qui est le résultat de l’opération.

</dd> <dt>

*Lacet* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Lacet autour de l’axe y, en radians.

</dd> <dt>

*Espacement* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Hauteur autour de l’axe x, en radians.

</dd> <dt>

*Roll* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Tourner autour de l’axe z, en radians.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) avec le lacet, le tangage et le roulis spécifiés.

## <a name="remarks"></a>Notes 

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* . De cette façon, la fonction **D3DXQuaternionRotationYawPitchRoll** peut être utilisée comme paramètre pour une autre fonction.

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

[**D3DXQuaternionRotationAxis**](d3dxquaternionrotationaxis.md)
</dt> <dt>

[**D3DXQuaternionRotationMatrix**](d3dxquaternionrotationmatrix.md)
</dt> </dl>

 

 
