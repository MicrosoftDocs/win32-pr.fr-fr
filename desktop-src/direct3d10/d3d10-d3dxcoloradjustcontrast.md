---
description: 'D3DXColorAdjustContrast, fonction (D3DX10Math. h) : ajuste la valeur de contraste d’une couleur.'
ms.assetid: c111d3c7-19c6-4a6b-af0d-a9e1bc0bb7d9
title: D3DXColorAdjustContrast, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorAdjustContrast
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 90c36ee9c414b6ae34058b255ad2e7a642f13ef49ee91b586ca974009d4e6b7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498489"
---
# <a name="d3dxcoloradjustcontrast-function-d3dx10mathh"></a>D3DXColorAdjustContrast, fonction (D3DX10Math. h)

Ajuste la valeur de contraste d’une couleur.

## <a name="syntax"></a>Syntaxe


```C++
D3DXCOLOR* D3DXColorAdjustContrast(
  _In_       D3DXCOLOR *pOut,
  _In_ const D3DXCOLOR *pC,
  _In_       FLOAT     c
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ dans\]
</dt> <dd>

Type : **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***

\[dans, pointeur de sortie \] vers un [**D3DXCOLOR**](d3d10-d3dxcolor.md) qui est le résultat de l’opération.

</dd> <dt>

*ordinateur* \[ dans\]
</dt> <dd>

Type : **const [**D3DXCOLOR**](../direct3d9/d3dxcolor.md) \***

Pointeur vers une structure D3DXCOLOR source.

</dd> <dt>

*c* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Valeur de contraste. Ce paramètre interpole de manière linéaire entre 50% de gris et la couleur, le pC. Il n’existe aucune limite quant à la valeur de c. Si ce paramètre est égal à zéro, la couleur retournée est 50% de gris. Si ce paramètre est 1, la couleur retournée est la couleur d’origine.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***

Cette fonction retourne un pointeur vers une structure D3DXCOLOR qui est le résultat de l’ajustement du contraste.

## <a name="remarks"></a>Remarques

Le canal alpha d’entrée est copié, sans modification, sur le canal alpha de sortie.

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue. De cette façon, cette fonction peut être utilisée comme paramètre pour une autre fonction.

Cette fonction interpole les composants de couleur rouge, vert et bleu d’une structure D3DXCOLOR entre 50% de gris et une valeur de contraste spécifiée, comme illustré dans l’exemple suivant.


```
pOut->r = 0.5f + c * (pC->r - 0.5f);
```



Si c est supérieur à 0 et inférieur à 1, le contraste est réduit. Si c est supérieur à 1, le contraste est augmenté.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
