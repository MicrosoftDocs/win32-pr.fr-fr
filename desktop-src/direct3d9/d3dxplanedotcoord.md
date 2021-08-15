---
description: Calcule le produit scalaire d’un plan et d’un vecteur 3D. Le paramètre w du vecteur est supposé être 1.
ms.assetid: 634de6bc-b631-493d-a7a6-292a3c3253d6
title: D3DXPlaneDotCoord, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneDotCoord
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 30f04ec310ce66dc43073e724b08c358cd8fc6f24f0b3840475a1abc61544503
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118524926"
---
# <a name="d3dxplanedotcoord-function"></a>D3DXPlaneDotCoord fonction)

Calcule le produit scalaire d’un plan et d’un vecteur 3D. Le paramètre w du vecteur est supposé être 1.

## <a name="syntax"></a>Syntaxe


```C++
FLOAT D3DXPlaneDotCoord(
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

## <a name="return-value"></a>Valeur retournée

Type : **[ **float**](../winprog/windows-data-types.md)**

Produit scalaire du plan et du vecteur 3D.

## <a name="remarks"></a>Remarques

Avec un plan (a, b, c, d) et un vecteur 3D (x, y, z), la valeur de retour de cette fonction est un \* x + b \* y + c \* z + d \* 1. La fonction **D3DXPlaneDotCoord** est utile pour déterminer la relation du plan avec une coordonnée dans l’espace 3D.

## <a name="requirements"></a>Configuration requise



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

[**D3DXPlaneDotNormal**](d3dxplanedotnormal.md)
</dt> </dl>

 

 
