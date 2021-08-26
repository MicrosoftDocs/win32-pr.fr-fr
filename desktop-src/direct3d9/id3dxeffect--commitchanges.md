---
description: Propage les modifications d’État qui se produisent à l’intérieur d’une passe active à l’appareil avant le rendu.
ms.assetid: 3a779b63-c106-4a81-afeb-82bd6e556de4
title: 'ID3DXEffect :: CommitChanges, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.CommitChanges
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5b81cd2674e08473358e031b827528121537264df11dba54c6a1f610ac054ee4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951759"
---
# <a name="id3dxeffectcommitchanges-method"></a>ID3DXEffect :: CommitChanges, méthode

Propage les modifications d’État qui se produisent à l’intérieur d’une passe active à l’appareil avant le rendu.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CommitChanges();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.

## <a name="remarks"></a>Remarques

Si l’application modifie un état d’effet à l’aide de l’une des méthodes [**ID3DXEffect :: setX**](id3dxeffect.md) à l’intérieur d’une paire de correspondances [**ID3DXEffect :: BeginPass**](id3dxeffect--beginpass.md) / [**ID3DXEffect :: EndPass**](id3dxeffect--endpass.md) , l’application doit appeler **ID3DXEffect :: CommitChanges** avant tout appel DrawxPrimitive pour propager les modifications d’État à l’appareil avant le rendu. Si aucun changement d’État ne se produit dans une paire de correspondances **ID3DXEffect :: BeginPass** et **ID3DXEffect :: EndPass** , il n’est pas nécessaire d’appeler **ID3DXEffect :: CommitChanges**.

Cela est légèrement différent pour tous les paramètres partagés dans un effet cloné. Quand une technique est active sur un effet cloné (autrement dit, quand [**ID3DXEffect :: Begin**](id3dxeffect--begin.md) a été appelé mais et que [**ID3DXEffect :: end**](id3dxeffect--end.md) n’a pas été appelé), **ID3DXEffect :: CommitChanges** met à jour les paramètres qui ne sont pas partagés comme prévu. Pour mettre à jour un paramètre partagé (uniquement pour un effet cloné dont la technique est active), appelez **ID3DXEffect :: end** pour désactiver la technique et **ID3DXEffect :: Begin** pour réactiver la technique avant d’appeler **ID3DXEffect :: CommitChanges**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 




