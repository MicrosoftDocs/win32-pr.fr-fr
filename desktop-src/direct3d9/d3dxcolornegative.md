---
description: Crée la valeur de couleur négative d’une valeur de couleur.
ms.assetid: 74143126-93f8-49fa-abe3-fd730b644d87
title: D3DXColorNegative, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorNegative
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a6d4d8559e64580897aec5261c450dc739496e75
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106542165"
---
# <a name="d3dxcolornegative-function"></a>D3DXColorNegative fonction)

Crée la valeur de couleur négative d’une valeur de couleur.

## <a name="syntax"></a>Syntaxe


```C++
D3DXCOLOR* D3DXColorNegative(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC
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

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **D3DXCOLOR**](d3dxcolor.md)\***

Cette fonction retourne un pointeur vers une structure [**D3DXCOLOR**](d3dxcolor.md) qui est la valeur de couleur négative de la valeur de couleur.

## <a name="remarks"></a>Notes

Le canal alpha d’entrée est copié, sans modification, sur le canal alpha de sortie.

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue. De cette façon, la fonction **D3DXColorNegative** peut être utilisée comme paramètre pour une autre fonction.

Cette fonction retourne la valeur de couleur négative en soustrayant 1,0 des composants de couleur de la structure [**D3DXCOLOR**](d3dxcolor.md) , comme indiqué dans l’exemple suivant.


```
pOut->r = 1.0f - pC->r;
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

[**D3DXColorScale**](d3dxcolorscale.md)
</dt> </dl>

 

 




