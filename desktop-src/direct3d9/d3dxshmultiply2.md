---
description: Calcule le produit de deux fonctions représentées à l’aide de SH (f et g).
ms.assetid: 632400a4-2ac9-438d-85f7-869101f350c8
title: D3DXSHMultiply2, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply2
- D3DXSHMultiply3
- D3DXSHMultiply4
- D3DXSHMultiply5
- D3DXSHMultiply6
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: f7b9adaf5caf7b4b2d35035fd5c2a916298b0c8c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106543025"
---
# <a name="d3dxshmultiply2-function-d3dx9mathh"></a>D3DXSHMultiply2, fonction (D3dx9math. h)

Calcule le produit de deux fonctions représentées à l’aide de SH (f et g).

## <a name="syntax"></a>Syntaxe


```C++
FLOAT* D3DXSHMultiply2(
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

Le pointeur vers la fonction de base Ylms de sortie est stocké à l \* l + m + l.

</dd> <dt>

*PF* \[ dans\]
</dt> <dd>

Type : **const [**float**](../winprog/windows-data-types.md) \***

Entrée SH coeffs pour la fonction First.

</dd> <dt>

*PG* \[ dans\]
</dt> <dd>

Type : **const [**float**](../winprog/windows-data-types.md) \***

Second jeu d’entrées SH coeffs.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **float**](../winprog/windows-data-types.md)\***

Pointeur vers les coefficients de sortie SH.

## <a name="remarks"></a>Notes

L’ordre est un nombre compris entre 2 et 6 inclus. En fait, cette page documente plusieurs fonctions : D3DXSHMultiply2, D3DXSHMultiply3,... D3DXSHMultiply6.

Calcule le produit de deux fonctions représentées à l’aide de SH (f et g), où *moue* \[ i \] = int (y \_ i (s) \* f (s) \* g (s)), où y \_ i (s) est la fonction énième base, f (s) et g (s) sont des fonctions SH (Sum \_ i (y \_ i) \* c \_ ). L’ordre O détermine les longueurs des tableaux, où il doit toujours y avoir un coefficient O ^ 2. En général, le produit de deux fonctions SH de Order O génère une fonction SH de Order 2 \* O-1, mais les résultats sont tronqués. Cela signifie que le produit est en mode muet (f \* g = = g \* f) mais n’associe pas (f \* (g \* h) ! = (f \* g) \* h.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
