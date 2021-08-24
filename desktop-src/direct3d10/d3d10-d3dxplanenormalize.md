---
description: 'Fonction D3DXPlaneNormalize (D3DX10Math. h) : normalise les coefficients de plan afin que la normale du plan ait une longueur d’unité.'
ms.assetid: 52ae36a7-e37b-457a-9832-e62900a85bde
title: D3DXPlaneNormalize, fonction (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cf4429e324a5ce1554c5c37c929625153c74764cb9d03618f633f35ecd416748
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754149"
---
# <a name="d3dxplanenormalize-function-d3dx10mathh"></a>D3DXPlaneNormalize, fonction (D3DX10Math. h)

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

Type : **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Pointeur vers le [**D3DXPLANE**](d3d10-d3dxplane.md) qui est le résultat de l’opération.

</dd> <dt>

*pp* \[ dans\]
</dt> <dd>

Type : **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***

Pointeur vers la structure D3DXPLANE source.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Pointeur vers une structure D3DXPLANE qui représente la normale du plan.

## <a name="remarks"></a>Remarques

Cette fonction normalise un plan afin que \| a, b, c \| = = 1.

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue. De cette façon, cette fonction peut être utilisée comme paramètre pour une autre fonction.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
