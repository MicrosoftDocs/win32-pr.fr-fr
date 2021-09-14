---
description: Met à l’échelle un vecteur 4D.
ms.assetid: b185a9b9-f768-4b50-aa6c-667c71eac39a
title: D3DXVec4Scale, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Scale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a29ee7b8519c802deb0542b6b7ba3ea22692f36d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126921364"
---
# <a name="d3dxvec4scale-function"></a>D3DXVec4Scale fonction)

Met à l’échelle un vecteur 4D.

## <a name="syntax"></a>Syntaxe


```C++
D3DXVECTOR4* D3DXVec4Scale(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Pointeur vers la structure [**D3DXVECTOR4**](d3dxvector4.md) qui est le résultat de l’opération.

</dd> <dt>

*PV* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Pointeur vers la structure [**D3DXVECTOR4**](d3dxvector4.md) source.

</dd> <dt>

 \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Valeur de mise à l’échelle.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Pointeur vers la structure [**D3DXVECTOR4**](d3dxvector4.md) qui est le vecteur mis à l’échelle.

## <a name="remarks"></a>Notes

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* . De cette façon, la fonction **D3DXVec4Scale** peut être utilisée comme paramètre pour une autre fonction.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec4Add**](d3dxvec4add.md)
</dt> <dt>

[**D3DXVec4Subtract**](d3dxvec4subtract.md)
</dt> </dl>

 

 
