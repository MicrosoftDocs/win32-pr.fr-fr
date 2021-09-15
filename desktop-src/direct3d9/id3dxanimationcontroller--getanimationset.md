---
description: Obtient un jeu d’animations.
ms.assetid: 61785f60-82c1-4ddc-b4cd-2e7f665cfe8c
title: 'ID3DXAnimationController :: GetAnimationSet, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c21f073b74d1ab7dac09ddd8bfb3d6be543e122a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520780"
---
# <a name="id3dxanimationcontrollergetanimationset-method"></a>ID3DXAnimationController :: GetAnimationSet, méthode

Obtient un jeu d’animations.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetAnimationSet(
  [in]  UINT               Index,
  [out] LPD3DXANIMATIONSET *ppAnimSet
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Index* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Index de l’ensemble d’animations.

</dd> <dt>

*ppAnimSet* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)\***

Pointeur vers le jeu d’animations [**ID3DXAnimationSet**](id3dxanimationset.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Notes

Le contrôleur d’animation contient un tableau d’ensembles d’animations. Cette méthode retourne l’une d’entre elles à l’index donné.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
