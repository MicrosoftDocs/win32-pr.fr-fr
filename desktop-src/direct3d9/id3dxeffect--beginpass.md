---
description: Commence une passe, dans la technique active.
ms.assetid: fbb2bf1c-e37a-4117-8c3c-5f5b6a267301
title: 'ID3DXEffect :: BeginPass, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.BeginPass
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 9013a67c2d4e0e9760167bc979ac05edd4879c5414ce5c9b9c55528baf3f6a18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987543"
---
# <a name="id3dxeffectbeginpass-method"></a>ID3DXEffect :: BeginPass, méthode

Commence une passe, dans la technique active.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT BeginPass(
  [in] UINT Pass
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Passer* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Index entier de base zéro dans la technique.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.

## <a name="remarks"></a>Remarques

Une application définit une passe active (au sein d’une technique active) dans le système d’effet en appelant **ID3DXEffect :: BeginPass**. Une application signale la fin de la passe active en appelant [**ID3DXEffect :: EndPass**](id3dxeffect--endpass.md). **ID3DXEffect :: BeginPass** et **ID3DXEffect :: EndPass** doivent se produire dans une paire correspondante, dans une paire correspondante d' [**ID3DXEffect :: Begin**](id3dxeffect--begin.md) et [**ID3DXEffect :: end**](id3dxeffect--end.md) .

Si l’application modifie un état d’effet à l’aide de l’une des méthodes [**Effect :: setX**](id3dxeffect.md) à l’intérieur d’une paire de correspondances **ID3DXEffect :: BeginPass** / [**ID3DXEffect :: EndPass**](id3dxeffect--endpass.md) , l’application doit appeler [**ID3DXEffect :: CommitChanges**](id3dxeffect--commitchanges.md) pour définir la mise à jour de l’appareil avec les changements d’État. Si aucun changement d’État ne se produit dans une paire de correspondances **ID3DXEffect :: BeginPass** et **ID3DXEffect :: EndPass** , il n’est pas nécessaire d’appeler **ID3DXEffect :: CommitChanges**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 
