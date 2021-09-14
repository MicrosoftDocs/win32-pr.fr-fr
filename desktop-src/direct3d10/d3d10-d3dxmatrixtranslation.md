---
description: Créez une matrice de traduction.
ms.assetid: a3565a06-22af-4ded-8835-da4c7ae81805
title: D3DXMatrixTranslation, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTranslation
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7abf55e5b51091de5d823ba837cdc8ad51e3940b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126921707"
---
# <a name="d3dxmatrixtranslation-function-d3dx10mathh"></a>D3DXMatrixTranslation, fonction (D3DX10Math. h)

Créez une matrice de traduction.

## <a name="syntax"></a>Syntaxe


```C++
D3DXMATRIX* D3DXMatrixTranslation(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      x,
  _In_    FLOAT      y,
  _In_    FLOAT      z
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Matrice qui va devenir une matrice de translation. Consultez [**D3DXMATRIX**](d3d10-d3dxmatrix.md).

</dd> <dt>

*x* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Composant x de la traduction.

</dd> <dt>

*y* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Composant y de la traduction.

</dd> <dt>

*z* \[\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Composant z de la traduction.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Matrice de translation.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
