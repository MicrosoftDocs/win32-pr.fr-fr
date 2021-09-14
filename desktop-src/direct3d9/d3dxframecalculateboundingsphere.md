---
description: Calcule la sphère englobante de tous les maillages dans la hiérarchie d’images.
ms.assetid: 8c3f5a9e-73ff-4d83-8f85-a3fc2a9a53f7
title: D3DXFrameCalculateBoundingSphere, fonction (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameCalculateBoundingSphere
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f10043d2c897bf6ab24c442b8e134f31221c498e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012786"
---
# <a name="d3dxframecalculateboundingsphere-function"></a>D3DXFrameCalculateBoundingSphere fonction)

Calcule la sphère englobante de tous les maillages dans la hiérarchie d’images.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXFrameCalculateBoundingSphere(
  _In_  const D3DXFRAME     *pFrameRoot,
  _Out_       LPD3DXVECTOR3 pObjectCenter,
  _Out_       FLOAT         *pObjectRadius
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFrameRoot* \[ dans\]
</dt> <dd>

Type : **const [**D3DXFRAME**](d3dxframe.md) \***

Pointeur vers le nœud racine.

</dd> <dt>

*pObjectCenter* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXVECTOR3**](d3dxvector3.md)**

Retourne le centre du cercle englobant.

</dd> <dt>

*pObjectRadius* \[ à\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)\***

Retourne le rayon du cercle englobant.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions d’animation](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
