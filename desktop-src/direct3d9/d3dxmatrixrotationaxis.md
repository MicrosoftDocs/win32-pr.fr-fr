---
description: 'D3DXMatrixRotationAxis, fonction (D3dx9math. h) : crée une matrice qui pivote autour d’un axe arbitraire.'
ms.assetid: 368c8f64-7709-4200-94d3-3dbc92a960c1
title: D3DXMatrixRotationAxis, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationAxis
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0ae47bf75a8f2a1f0b5e75ceadabff5a1ea7c6845617012a00a2bb115470e43c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750209"
---
# <a name="d3dxmatrixrotationaxis-function-d3dx9mathh"></a>D3DXMatrixRotationAxis, fonction (D3dx9math. h)

Crée une matrice qui pivote autour d’un axe arbitraire.

## <a name="syntax"></a>Syntaxe


```C++
D3DXMATRIX* D3DXMatrixRotationAxis(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_          FLOAT       Angle
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) qui est le résultat de l’opération.

</dd> <dt>

*PV* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Pointeur vers l’axe arbitraire. Consultez [**D3DXVECTOR3**](d3dxvector3.md).

</dd> <dt>

*Angle* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Angle de rotation en radians. Les angles sont mesurés dans le sens des aiguilles d’une montre sur l’axe de rotation vers l’origine.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) pivotée autour de l’axe spécifié.

## <a name="remarks"></a>Remarques

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* . De cette façon, la fonction **D3DXMatrixRotationAxis** peut être utilisée comme paramètre pour une autre fonction.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixRotationQuaternion**](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[**D3DXMatrixRotationX**](d3dxmatrixrotationx.md)
</dt> <dt>

[**D3DXMatrixRotationY**](d3dxmatrixrotationy.md)
</dt> <dt>

[**D3DXMatrixRotationYawPitchRoll**](d3dxmatrixrotationyawpitchroll.md)
</dt> <dt>

[**D3DXMatrixRotationZ**](d3dxmatrixrotationz.md)
</dt> </dl>

 

 
