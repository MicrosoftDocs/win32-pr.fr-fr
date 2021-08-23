---
description: Calcule le produit scalaire d’un plan et d’un vecteur 4D.
ms.assetid: e6232ca8-52cc-472d-8bdb-4f8dfc520d4f
title: D3DXPlaneDot, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneDot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4895a94ad50171682a8bd5247694c3b35a56d174b5477f5bbb2a621c1e74fa96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564629"
---
# <a name="d3dxplanedot-function"></a>D3DXPlaneDot fonction)

Calcule le produit scalaire d’un plan et d’un vecteur 4D.

## <a name="syntax"></a>Syntaxe


```C++
FLOAT D3DXPlaneDot(
  _In_ const D3DXPLANE   *pP,
  _In_ const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pp* \[ dans\]
</dt> <dd>

Type : **const [**D3DXPLANE**](d3dxplane.md) \***

Pointeur vers une structure [**D3DXPLANE**](d3dxplane.md) source.

</dd> <dt>

*PV* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Pointeur vers une structure [**D3DXVECTOR4**](d3dxvector4.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **float**](../winprog/windows-data-types.md)**

Produit scalaire des vecteurs de plan et 4D.

## <a name="remarks"></a>Remarques

Avec un plan (a, b, c, d) et un vecteur 4D (x, y, z, w), la valeur de retour de cette fonction est un \* x + b \* y + c \* z + d \* w. La fonction **D3DXPlaneDot** est utile pour déterminer la relation du plan avec une coordonnée homogène. Par exemple, cette fonction peut être utilisée pour déterminer si une coordonnée particulière est sur un plan particulier, ou sur le côté d’un plan particulier qui se trouve une coordonnée particulière.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXPlaneDotCoord**](d3dxplanedotcoord.md)
</dt> <dt>

[**D3DXPlaneDotNormal**](d3dxplanedotnormal.md)
</dt> </dl>

 

 
