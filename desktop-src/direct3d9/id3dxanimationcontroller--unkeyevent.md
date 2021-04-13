---
description: Supprime un événement spécifié d’une piste d’animation, empêchant ainsi l’exécution de l’événement.
ms.assetid: 658ffe91-44ba-4bde-b78c-c545dff27ab1
title: 'ID3DXAnimationController :: UnkeyEvent, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.UnkeyEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ac0c9d6a643337c43a5cadd5bcfe0b090cd39a00
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323354"
---
# <a name="id3dxanimationcontrollerunkeyevent-method"></a>ID3DXAnimationController :: UnkeyEvent, méthode

Supprime un événement spécifié d’une piste d’animation, empêchant ainsi l’exécution de l’événement.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT UnkeyEvent(
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hEvent* \[ dans\]
</dt> <dd>

Type : **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Handle d’événement de l’événement à supprimer de la piste d’animation.

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

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




