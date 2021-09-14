---
description: Calcule le produit scalaire d’un plan et d’un vecteur 3D. Le paramètre w du vecteur est supposé être 0.
ms.assetid: 7aba1e94-6531-4c07-83b0-6100805e8bbd
title: D3DXPlaneDotNormal, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneDotNormal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 28903fc8ce0073e4014ae6ce75df636222ce32f0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922508"
---
# <a name="d3dxplanedotnormal-function"></a>D3DXPlaneDotNormal fonction)

Calcule le produit scalaire d’un plan et d’un vecteur 3D. Le paramètre w du vecteur est supposé être 0.

## <a name="syntax"></a>Syntaxe


```C++
FLOAT D3DXPlaneDotNormal(
  _In_ const D3DXPLANE   *pP,
  _In_ const D3DXVECTOR3 *pV
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

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) source.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **float**](../winprog/windows-data-types.md)**

Produit scalaire du plan et du vecteur 3D.

## <a name="remarks"></a>Notes

Avec un plan (a, b, c, d) et un vecteur 3D (x, y, z), la valeur de retour de cette fonction est un \* x + b \* y + c \* z + d \* 0. La fonction **D3DXPlaneDotNormal** est utile pour calculer l’angle entre la normale du plan et une autre normale.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXPlaneDot**](d3dxplanedot.md)
</dt> <dt>

[**D3DXPlaneDotCoord**](d3dxplanedotcoord.md)
</dt> </dl>

 

 
