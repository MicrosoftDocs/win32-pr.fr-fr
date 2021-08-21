---
description: 'D3DXPlaneFromPointNormal, fonction (D3dx9math. h) : construit un plan à partir d’un point et d’un normal.'
ms.assetid: af396bbb-09b7-492f-a25f-9c950da7e605
title: D3DXPlaneFromPointNormal, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneFromPointNormal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0acf7dd26a2eb261830dbdf1f0e1fff185184a645e469fbe02a5b0032c141e1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118524916"
---
# <a name="d3dxplanefrompointnormal-function-d3dx9mathh"></a>D3DXPlaneFromPointNormal, fonction (D3dx9math. h)

Construit un plan à partir d’un point et d’un normal.

## <a name="syntax"></a>Syntaxe


```C++
D3DXPLANE* D3DXPlaneFromPointNormal(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pPoint,
  _In_    const D3DXVECTOR3 *pNormal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXPLANE**](d3dxplane.md)\***

Pointeur vers la structure [**D3DXPLANE**](d3dxplane.md) qui est le résultat de l’opération.

</dd> <dt>

*PPoint* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , définissant le point utilisé pour construire le plan.

</dd> <dt>

*pNormal* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , définissant le normal utilisé pour construire le plan.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **D3DXPLANE**](d3dxplane.md)\***

Pointeur vers la structure [**D3DXPLANE**](d3dxplane.md) construite à partir du point et du normal.

## <a name="remarks"></a>Remarques

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* . De cette façon, la fonction **D3DXPlaneFromPointNormal** peut être utilisée comme paramètre pour une autre fonction.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXPlaneFromPoints**](d3dxplanefrompoints.md)
</dt> </dl>

 

 




