---
description: 'Fonction D3DXPlaneNormalize (D3dx9math. h) : normalise les coefficients de plan afin que la normale du plan ait une longueur d’unité.'
ms.assetid: 9c595986-e1f8-4153-ba23-1fa6e583a050
title: D3DXPlaneNormalize, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneNormalize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d38ccbc3f688ed61779cf48a77e97dfb544c686e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094147"
---
# <a name="d3dxplanenormalize-function-d3dx9mathh"></a>D3DXPlaneNormalize, fonction (D3dx9math. h)

Normalise les coefficients de plan afin que la normale du plan ait une longueur d’unité.

## <a name="syntax"></a>Syntaxe


```C++
D3DXPLANE* D3DXPlaneNormalize(
  _Inout_       D3DXPLANE *pOut,
  _In_    const D3DXPLANE *pP
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXPLANE**](d3dxplane.md)\***

Pointeur vers la structure [**D3DXPLANE**](d3dxplane.md) qui est le résultat de l’opération.

</dd> <dt>

*pp* \[ dans\]
</dt> <dd>

Type : **const [**D3DXPLANE**](d3dxplane.md) \***

Pointeur vers la structure [**D3DXPLANE**](d3dxplane.md) source.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **D3DXPLANE**](d3dxplane.md)\***

Pointeur vers une structure [**D3DXPLANE**](d3dxplane.md) qui représente la normale du plan.

## <a name="remarks"></a>Notes 

Cette fonction normalise un plan afin que \| a, b, c \| = = 1.

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* . De cette façon, cette fonction peut être utilisée comme paramètre pour une autre fonction.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




