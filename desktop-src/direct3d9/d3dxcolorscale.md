---
description: Met à l’échelle une valeur de couleur.
ms.assetid: 35e8adee-7ce5-4db5-8276-f0e408748e78
title: D3DXColorScale, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorScale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 74020f302a26162df1e42cb4c9f020af3f64e59c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106527282"
---
# <a name="d3dxcolorscale-function"></a>D3DXColorScale fonction)

Met à l’échelle une valeur de couleur.

## <a name="syntax"></a>Syntaxe


```C++
D3DXCOLOR* D3DXColorScale(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC,
  _In_          FLOAT     s
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXCOLOR**](d3dxcolor.md)\***

Pointeur vers une structure [**D3DXCOLOR**](d3dxcolor.md) qui est le résultat de l’opération.

</dd> <dt>

*ordinateur* \[ dans\]
</dt> <dd>

Type : **const [**D3DXCOLOR**](d3dxcolor.md) \***

Pointeur vers une structure [**D3DXCOLOR**](d3dxcolor.md) source.

</dd> <dt>

 \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Facteur d’échelle. Il met à l’échelle la couleur, en la traitant comme un vecteur 4D. La valeur de s n’est pas limitée. Si s est 1, la couleur résultante est la couleur d’origine.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **D3DXCOLOR**](d3dxcolor.md)\***

Cette fonction retourne un pointeur vers une structure [**D3DXCOLOR**](d3dxcolor.md) qui est la valeur de couleur mise à l’échelle.

## <a name="remarks"></a>Notes

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue. De cette façon, la fonction **D3DXColorScale** peut être utilisée comme paramètre pour une autre fonction.

Cette fonction calcule la valeur de couleur mise à l’échelle en multipliant les composants de couleur de la structure [**D3DXCOLOR**](d3dxcolor.md) par le facteur d’échelle spécifié, comme indiqué dans l’exemple suivant.


```
pOut->r = pC->r * s;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXColorLerp**](d3dxcolorlerp.md)
</dt> <dt>

[**D3DXColorModulate**](d3dxcolormodulate.md)
</dt> <dt>

[**D3DXColorNegative**](d3dxcolornegative.md)
</dt> </dl>

 

 
