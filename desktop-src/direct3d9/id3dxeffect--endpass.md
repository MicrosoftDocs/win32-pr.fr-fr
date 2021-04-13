---
description: Terminer une passe active.
ms.assetid: e20b3e0f-db9f-48e8-ab4e-761a5861f3ce
title: 'ID3DXEffect :: EndPass, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.EndPass
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5cdba799f282e56bbe4565a4792906fd835e5c6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322981"
---
# <a name="id3dxeffectendpass-method"></a>ID3DXEffect :: EndPass, méthode

Terminer une passe active.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT EndPass();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Cette méthode retourne toujours la valeur \_ OK.

## <a name="remarks"></a>Notes

Une application signale la fin du rendu d’une passe active en appelant **ID3DXEffect :: EndPass**. Chaque **ID3DXEffect :: EndPass** doit faire partie d’une paire correspondante d’appels [**ID3DXEffect :: BeginPass**](id3dxeffect--beginpass.md) et **ID3DXEffect :: EndPass** .

Chaque paire correspondante d’appels [**ID3DXEffect :: BeginPass**](id3dxeffect--beginpass.md) et **ID3DXEffect :: EndPass** doit se trouver dans une paire correspondante d’appels [**ID3DXEffect :: Begin**](id3dxeffect--begin.md) et [**ID3DXEffect :: end**](id3dxeffect--end.md) .

Si l’application modifie un état d’effet à l’aide de l’une des méthodes [**Effect :: setX**](id3dxeffect.md) à l’intérieur d’une paire de correspondances [**ID3DXEffect :: BeginPass**](id3dxeffect--beginpass.md) / **ID3DXEffect :: EndPass** , l’application doit appeler [**ID3DXEffect :: CommitChanges**](id3dxeffect--commitchanges.md) avant tout appel DrawxPrimitive pour propager les modifications d’État à l’appareil avant le rendu.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 




