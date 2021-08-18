---
description: Calcule le produit de deux fonctions d’harmoniques sphériques (f et g). Les deux fonctions sont de l’ordre N = 5.
ms.assetid: c72231a1-9db3-4701-b7ad-4509028ce508
title: D3DXSHMultiply5, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply5
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a022fa883a1b1e809f965ec94813741a285447e9f6935c1adca370b5aef6c061
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990769"
---
# <a name="d3dxshmultiply5-function"></a>D3DXSHMultiply5 fonction)

Calcule le produit de deux fonctions d’harmoniques sphériques (f et g). Les deux fonctions sont de l’ordre N = 5.

## <a name="syntax"></a>Syntaxe


```C++
FLOAT* D3DXSHMultiply5(
  _In_       FLOAT *pOut,
  _In_ const FLOAT *pF,
  _In_ const FLOAT *pG
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)\***

Pointeur vers les coefficients de sortie SH : la fonction de base *Y* LM est stockée à *l*² + *m* + l. L’ordre N détermine la longueur du tableau, où il doit toujours y avoir *N*-efficients ².

</dd> <dt>

*PF* \[ dans\]
</dt> <dd>

Type : **const [**float**](../winprog/windows-data-types.md) \***

Entrées SH d’entrée pour la première fonction.

</dd> <dt>

*PG* \[ dans\]
</dt> <dd>

Type : **const [**float**](../winprog/windows-data-types.md) \***

Second jeu de coefficients SH d’entrée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **float**](../winprog/windows-data-types.md)\***

Pointeur vers les coefficients de sortie SH.

## <a name="remarks"></a>Remarques

Le produit de deux fonctions SH de Order N = 5 génère une fonction SH de Order 2 × *N* -1 = 9, mais les résultats sont tronqués. Cela signifie que le produit est en mode de lancement ( *f* × *g*  =  *g* × *f* ) mais n’associe pas ( *f* × ( *g* × *h* ) ≠ ( *f* × *g* ) × *h* ).

Cette fonction utilise l’équation suivante :


```
pOut[i] = int(y_i(s) * f(s) * g(s))
```



où y \_ correspond à la fonction énième base et où f (s) et g (s) utilisent la fonction SH suivante :


```
sum_i(y_i(s)*c_i)
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
