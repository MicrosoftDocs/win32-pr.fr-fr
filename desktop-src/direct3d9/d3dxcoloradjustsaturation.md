---
description: 'Fonction D3DXColorAdjustSaturation (D3dx9math. h) : ajuste la valeur de saturation d’une couleur.'
ms.assetid: 1f66c3b4-2f02-4993-80c6-c484180c2459
title: D3DXColorAdjustSaturation, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorAdjustSaturation
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 71ed9b6ebdefe41b466bb790cc4d0226991ce2866aee9fed765c19c87f6085b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119495839"
---
# <a name="d3dxcoloradjustsaturation-function-d3dx9mathh"></a>D3DXColorAdjustSaturation, fonction (D3dx9math. h)

Ajuste la valeur de saturation d’une couleur.

## <a name="syntax"></a>Syntaxe


```C++
D3DXCOLOR* D3DXColorAdjustSaturation(
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

Valeur de saturation. Ce paramètre interpole de manière linéaire entre la couleur convertie en nuances de gris et la couleur d’origine, pC. La valeur de s n’est pas limitée. Si s est égal à 0, la couleur retournée est la couleur de nuances de gris. Si s est 1, la couleur retournée est la couleur d’origine.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **D3DXCOLOR**](d3dxcolor.md)\***

Cette fonction retourne un pointeur vers une structure [**D3DXCOLOR**](d3dxcolor.md) qui est le résultat de l’ajustement de saturation.

## <a name="remarks"></a>Remarques

Le canal alpha d’entrée est copié, sans modification, sur le canal alpha de sortie.

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue. De cette façon, cette fonction peut être utilisée comme paramètre pour une autre fonction.

Cette fonction interpole les composants de couleur rouge, vert et bleu d’une structure [**D3DXCOLOR**](d3dxcolor.md) entre une couleur insaturée et une couleur, comme illustré dans l’exemple suivant.


```
    // Approximate values for each component's contribution to luminance.
    // Based upon the NTSC standard described in ITU-R Recommendation BT.709.
    FLOAT grey = pC->r * 0.2125f + pC->g * 0.7154f + pC->b * 0.0721f;
    
    pOut->r = grey + s * (pC->r - grey);
```



Si s est supérieur à 0 et inférieur à 1, la saturation est réduite. Si s est supérieur à 1, la saturation est augmentée.

La couleur de nuances de gris est calculée comme suit :


```
r = g = b = 0.2125*r + 0.7154*g + 0.0721*b
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

[**D3DXColorAdjustContrast**](d3dxcoloradjustcontrast.md)
</dt> </dl>

 

 
