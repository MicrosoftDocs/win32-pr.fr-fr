---
description: 'D3DXMatrixDeterminant, fonction (D3DX10Math. h) : retourne le déterminant d’une matrice.'
ms.assetid: b0155c91-1554-42ef-b219-c6cdd2a905b5
title: D3DXMatrixDeterminant, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixDeterminant
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 894db23a3079c1344c97cab00642cbbc0953450d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103457"
---
# <a name="d3dxmatrixdeterminant-function-d3dx10mathh"></a>D3DXMatrixDeterminant, fonction (D3DX10Math. h)

Retourne le déterminant d’une matrice.

## <a name="syntax"></a>Syntaxe


```C++
FLOAT D3DXMatrixDeterminant(
  _In_ const D3DXMATRIX *pM
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*GCF* \[ dans\]
</dt> <dd>

Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Pointeur vers la structure D3DXMATRIX source.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **float**](../winprog/windows-data-types.md)**

Retourne le déterminant de la matrice.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
