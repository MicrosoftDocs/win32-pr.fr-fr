---
description: 'ID3DXKeyframedAnimationSet :: GetCallbackKeys, méthode-remplit un tableau avec les données de clé de rappel utilisées pour l’animation d’image clé.'
ms.assetid: 2a2aa04a-a889-415b-8aa2-cc5f2bed1f9a
title: 'ID3DXKeyframedAnimationSet :: GetCallbackKeys, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetCallbackKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5f3bdb7049de3b5d6aad10b5ff5100d01d05e3ee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127232704"
---
# <a name="id3dxkeyframedanimationsetgetcallbackkeys-method"></a>ID3DXKeyframedAnimationSet :: GetCallbackKeys, méthode

Remplit un tableau avec les données de clé de rappel utilisées pour l’animation d’image clé.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetCallbackKeys(
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pCallbackKeys* \[ à\]
</dt> <dd>

Type : **[ **\_ rappel LPD3DXKEY**](d3dxkey-callback.md)**

Pointeur vers un tableau alloué par l’utilisateur de structures de [**\_ rappel D3DXKEY**](d3dxkey-callback.md) que la méthode doit remplir avec les données de rappel.

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
</dt> <dt>

[**ID3DXKeyframedAnimationSet::GetNumCallbackKeys**](id3dxkeyframedanimationset--getnumcallbackkeys.md)
</dt> </dl>

 

 




