---
description: Crée une matrice avec un lacet, un tangage et un roulis spécifiés.
ms.assetid: a3ef2b57-275f-484a-88fc-aaa5e470717c
title: D3DXMatrixRotationYawPitchRoll, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationYawPitchRoll
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d65242f49ee94394337f43555c3e154141e3b642
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953978"
---
# <a name="d3dxmatrixrotationyawpitchroll-function-d3dx10mathh"></a>D3DXMatrixRotationYawPitchRoll, fonction (D3DX10Math. h)

Crée une matrice avec un lacet, un tangage et un roulis spécifiés.

## <a name="syntax"></a>Syntaxe


```C++
D3DXMATRIX* D3DXMatrixRotationYawPitchRoll(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Yaw,
  _In_    FLOAT      Pitch,
  _In_    FLOAT      Roll
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) qui est le résultat de l’opération.

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

## <a name="return-value"></a>Valeur retournée

Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Pointeur vers une structure D3DXMATRIX avec le lacet, le tangage et le roulis spécifiés.

## <a name="remarks"></a>Notes

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue. De cette façon, la fonction D3DXMatrixRotationYawPitchRoll peut être utilisée comme paramètre pour une autre fonction.

L’ordre des transformations est le premier, puis le tangage, puis le lacet. Par rapport à l’axe de coordonnées local de l’objet, cette valeur est équivalente à la rotation autour de l’axe z, suivie d’une rotation autour de l’axe x, suivie d’une rotation autour de l’axe y, comme indiqué dans l’illustration suivante.

![illustration du rouleau, du tangage et du lacet comme rotations autour des trois axes](images/pitchyawroll.png)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
