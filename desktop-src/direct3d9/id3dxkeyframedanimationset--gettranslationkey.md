---
description: Obtenir des informations de traduction pour une image clé spécifique dans l’ensemble d’animations.
ms.assetid: 757af408-8a9c-4294-9343-91f52d4cc1ab
title: 'ID3DXKeyframedAnimationSet :: GetTranslationKey, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetTranslationKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f61d1caecb46477d16be4367588ab5609bfd6224
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106545312"
---
# <a name="id3dxkeyframedanimationsetgettranslationkey-method"></a>ID3DXKeyframedAnimationSet :: GetTranslationKey, méthode

Obtenir des informations de traduction pour une image clé spécifique dans l’ensemble d’animations.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetTranslationKey(
  [in]  UINT              Animation,
  [in]  UINT              Key,
  [out] LPD3DXKEY_VECTOR3 pTranslationKey
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Animation* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Index d’animation.

</dd> <dt>

*Clé* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Image clé.

</dd> <dt>

*pTranslationKey* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**

Pointeur vers les informations de rotation. Consultez [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
