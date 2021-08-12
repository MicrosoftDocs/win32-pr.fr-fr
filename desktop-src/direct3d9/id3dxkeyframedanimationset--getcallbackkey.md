---
description: 'ID3DXKeyframedAnimationSet :: GetCallbackKey, méthode-obtient des informations sur un rappel spécifique dans l’ensemble d’animations.'
ms.assetid: a1d3ca96-2852-420a-aa5c-a434970e5523
title: 'ID3DXKeyframedAnimationSet :: GetCallbackKey, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetCallbackKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5036ca9e00da3231677fe41e179bb9c27d1a4bbbd145f3e15bc6e4160902e9b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118295169"
---
# <a name="id3dxkeyframedanimationsetgetcallbackkey-method"></a>ID3DXKeyframedAnimationSet :: GetCallbackKey, méthode

Obtient des informations sur un rappel spécifique dans l’ensemble d’animations.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetCallbackKey(
  [in]  UINT               Animation,
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Animation* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Index d’animation.

</dd> <dt>

*pCallbackKeys* \[ à\]
</dt> <dd>

Type : **[ **\_ rappel LPD3DXKEY**](d3dxkey-callback.md)**

Pointeur vers la [**fonction de rappel**](d3dxkey-callback.md).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

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

 

 
