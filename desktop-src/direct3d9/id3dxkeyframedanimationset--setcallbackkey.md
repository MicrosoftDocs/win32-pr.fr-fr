---
description: Définit des informations sur un rappel spécifique dans l’ensemble d’animations.
ms.assetid: 899f3a85-c878-4eeb-8bda-fc4e9083bd1f
title: 'ID3DXKeyframedAnimationSet :: SetCallbackKey, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.SetCallbackKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5998842927019868249278465eaf7bf9bd4ab62c3bfe83537a0eba420f87aeb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847759"
---
# <a name="id3dxkeyframedanimationsetsetcallbackkey-method"></a>ID3DXKeyframedAnimationSet :: SetCallbackKey, méthode

Définit des informations sur un rappel spécifique dans l’ensemble d’animations.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetCallbackKey(
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

 

 
