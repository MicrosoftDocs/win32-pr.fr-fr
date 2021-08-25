---
description: 'Fonction D3DXMatrixMultiplyTranspose (D3dx9math. h) : calcule le produit transposé de deux matrices.'
ms.assetid: 43927500-9413-41a4-a6ee-974d85dd1054
title: D3DXMatrixMultiplyTranspose, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixMultiplyTranspose
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a33f6e1938acb3381d1f14190d3a2e1adbc6afe32147ff793cfc7597f5c3bacc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027369"
---
# <a name="d3dxmatrixmultiplytranspose-function-d3dx9mathh"></a>D3DXMatrixMultiplyTranspose, fonction (D3dx9math. h)

Calcule le produit transposé de deux matrices.

## <a name="syntax"></a>Syntaxe


```C++
D3DXMATRIX* D3DXMatrixMultiplyTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) qui est le résultat de l’opération.

</dd> <dt>

*pM1* \[ dans\]
</dt> <dd>

Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) source.

</dd> <dt>

*pM2* \[ dans\]
</dt> <dd>

Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) source.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) qui est le produit de deux matrices.

## <a name="remarks"></a>Remarques

Le résultat est le transpose du produit de deux matrices de transformation, out = T (M1 \* m2).

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* . De cette façon, la fonction **D3DXMatrixMultiplyTranspose** peut être utilisée comme paramètre pour une autre fonction.

Cette fonction est utile pour définir des matrices en tant que constantes pour les nuanceurs de sommets et de pixels.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixMultiply**](d3dxmatrixmultiply.md)
</dt> <dt>

[**D3DXQuaternionMultiply**](d3dxquaternionmultiply.md)
</dt> </dl>

 

 




