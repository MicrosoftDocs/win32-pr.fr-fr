---
description: Définissez les informations de traduction pour une image clé spécifique dans l’ensemble d’animations.
ms.assetid: 4a926c0f-6d57-48d4-bb3b-60766fc78e40
title: 'ID3DXKeyframedAnimationSet :: SetTranslationKey, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.SetTranslationKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5bdfb8fb02a2b06dc797317d35cc14e75bd6f221
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127517445"
---
# <a name="id3dxkeyframedanimationsetsettranslationkey-method"></a>ID3DXKeyframedAnimationSet :: SetTranslationKey, méthode

Définissez les informations de traduction pour une image clé spécifique dans l’ensemble d’animations.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetTranslationKey(
  [in] UINT              Animation,
  [in] UINT              Key,
  [in] LPD3DXKEY_VECTOR3 pTranslationKey
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

*pTranslationKey* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**

Pointeur vers les données de traduction. Consultez [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md).

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
