---
description: Définissez le gestionnaire d’état des effets.
ms.assetid: 87409687-03f1-4593-ae58-3a8ba08e592b
title: 'ID3DXEffect :: SetStateManager, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.SetStateManager
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: bb32e3f668884a6f51bd5c5058a4f27e141f0aa3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394075"
---
# <a name="id3dxeffectsetstatemanager-method"></a>ID3DXEffect :: SetStateManager, méthode

Définissez le gestionnaire d’état des effets.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetStateManager(
  [in] LPD3DXEFFECTSTATEMANAGER pManager
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pManager* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXEFFECTSTATEMANAGER**](id3dxeffectstatemanager.md)**

Pointeur vers le gestionnaire d’État. Consultez [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.

## <a name="remarks"></a>Notes

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

[**ID3DXEffect::GetStateManager**](id3dxeffect--getstatemanager.md)
</dt> </dl>

 

 




