---
description: Utilise une interpolation linéaire pour créer une valeur de couleur.
ms.assetid: bf7bf2f4-5fb5-44d3-a7e5-7998640d7d49
title: D3DXColorLerp, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorLerp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3521ee9e76aecd486093f903d336c08553e0e4ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870126"
---
# <a name="d3dxcolorlerp-function"></a>D3DXColorLerp fonction)

Utilise une interpolation linéaire pour créer une valeur de couleur.

## <a name="syntax"></a>Syntaxe


```C++
D3DXCOLOR* D3DXColorLerp(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC1,
  _In_    const D3DXCOLOR *pC2,
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

*PC1* \[ dans\]
</dt> <dd>

Type : **const [**D3DXCOLOR**](d3dxcolor.md) \***

Pointeur vers une structure [**D3DXCOLOR**](d3dxcolor.md) source.

</dd> <dt>

*pC2* \[ dans\]
</dt> <dd>

Type : **const [**D3DXCOLOR**](d3dxcolor.md) \***

Pointeur vers une structure [**D3DXCOLOR**](d3dxcolor.md) source.

</dd> <dt>

 \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Paramètre qui interpole de manière linéaire entre les couleurs pC1 et pC2, en les traitant à la fois comme vecteurs 4D. La valeur de s n’est pas limitée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **D3DXCOLOR**](d3dxcolor.md)\***

Cette fonction retourne un pointeur vers une structure [**D3DXCOLOR**](d3dxcolor.md) qui est le résultat de l’interpolation linéaire.

## <a name="remarks"></a>Notes

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue. De cette façon, la fonction **D3DXColorLerp** peut être utilisée comme paramètre pour une autre fonction.

Cette fonction interpole les composants rouge, vert, bleu et alpha d’une structure [**D3DXCOLOR**](d3dxcolor.md) entre deux couleurs, comme indiqué dans l’exemple suivant.


```
   
pOut->r = pC1->r + s * (pC2->r - pC1->r);
```



Si vous effectuez une interpolation linéaire entre les couleurs A et B, et que s est égal à 0, la couleur résultante est. Si s est 1, la couleur résultante est la couleur B.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXColorModulate**](d3dxcolormodulate.md)
</dt> <dt>

[**D3DXColorNegative**](d3dxcolornegative.md)
</dt> <dt>

[**D3DXColorScale**](d3dxcolorscale.md)
</dt> </dl>

 

 
