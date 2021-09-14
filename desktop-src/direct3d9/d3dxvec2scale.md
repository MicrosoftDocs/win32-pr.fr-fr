---
description: Met à l’échelle un vecteur 2D.
ms.assetid: 1887bc48-3766-42d7-840b-1e29d78db4ce
title: D3DXVec2Scale, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Scale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 941e85763b15724e3c810c0416b5b142c9d95913
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126998679"
---
# <a name="d3dxvec2scale-function"></a>D3DXVec2Scale fonction)

Met à l’échelle un vecteur 2D.

## <a name="syntax"></a>Syntaxe


```C++
D3DXVECTOR2* D3DXVec2Scale(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Pointeur vers la structure [**D3DXVECTOR2**](d3dxvector2.md) qui est le résultat de l’opération.

</dd> <dt>

*PV* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Pointeur vers la structure [**D3DXVECTOR2**](d3dxvector2.md) source.

</dd> <dt>

 \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Valeur de mise à l’échelle.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Pointeur vers une structure [**D3DXVECTOR2**](d3dxvector2.md) qui est le vecteur mis à l’échelle.

## <a name="remarks"></a>Notes

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* . De cette façon, la fonction **D3DXVec2Scale** peut être utilisée comme paramètre pour une autre fonction.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec2Add**](d3dxvec2add.md)
</dt> <dt>

[**D3DXVec2Subtract**](d3dxvec2subtract.md)
</dt> </dl>

 

 
