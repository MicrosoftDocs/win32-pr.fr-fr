---
description: Obtient le gestionnaire d’état des effets.
ms.assetid: 4a09eb2a-2393-40b0-81b9-3c27998c2b77
title: 'ID3DXEffect :: GetStateManager, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.GetStateManager
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6700447485d83f2610149b809065ab02140a2e6cf068508b6571d5132844fb0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121640"
---
# <a name="id3dxeffectgetstatemanager-method"></a>ID3DXEffect :: GetStateManager, méthode

Obtient le gestionnaire d’état des effets.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetStateManager(
  [out] LPD3DXEFFECTSTATEMANAGER *ppManager
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppManager* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXEFFECTSTATEMANAGER**](id3dxeffectstatemanager.md)\***

Retourne un pointeur vers le gestionnaire d’État. Consultez [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.

## <a name="remarks"></a>Remarques

Le [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md) est une interface implémentée par l’utilisateur qui fournit des rappels dans une application pour définir l’état de l’appareil à partir d’un effet.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> <dt>

[**ID3DXEffect::SetStateManager**](id3dxeffect--setstatemanager.md)
</dt> </dl>

 

 




