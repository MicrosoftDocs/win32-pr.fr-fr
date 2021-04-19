---
description: Remplit un tableau avec les données de clé de rappel utilisées pour l’animation d’image clé.
ms.assetid: 0dc30c1f-9ffb-42ec-8074-84293f16c344
title: 'ID3DXCompressedAnimationSet :: GetCallbackKeys, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXCompressedAnimationSet.GetCallbackKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fe56a3dbdd7d019deb5d7111fa592470bffd244d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535181"
---
# <a name="id3dxcompressedanimationsetgetcallbackkeys-method"></a>ID3DXCompressedAnimationSet :: GetCallbackKeys, méthode

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

[ID3DXCompressedAnimationSet](id3dxcompressedanimationset.md)
</dt> <dt>

[**ID3DXCompressedAnimationSet::GetNumCallbackKeys**](id3dxcompressedanimationset--getnumcallbackkeys.md)
</dt> </dl>

 

 




