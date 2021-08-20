---
description: Mettre à l’échelle le plan avec le facteur d’échelle donné.
ms.assetid: 3a0454ef-2821-472f-b7a4-5e49bb5f556e
title: D3DXPlaneScale, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneScale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 248236bd4b1952a8a53b25087f9acf2ce952e99ff7f39d0d9d20a49d314fa22f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118095447"
---
# <a name="d3dxplanescale-function"></a>D3DXPlaneScale fonction)

Mettre à l’échelle le plan avec le facteur d’échelle donné.

## <a name="syntax"></a>Syntaxe


```C++
D3DXPLANE* D3DXPlaneScale(
  _Inout_       D3DXPLANE *pOut,
  _In_    const D3DXPLANE *pP,
  _In_          FLOAT     s
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

</dd> <dt>

 \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Facteur d’échelle.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **D3DXPLANE**](d3dxplane.md)\***

Pointeur vers une structure [**D3DXPLANE**](d3dxplane.md) qui représente le plan mis à l’échelle.

## <a name="remarks"></a>Remarques

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* . Par conséquent, cette fonction peut être utilisée comme paramètre pour une autre fonction.

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
