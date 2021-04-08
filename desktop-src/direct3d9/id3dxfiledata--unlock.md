---
description: 'Termine la durée de vie du pointeur ppData retourné par ID3DXFileData :: Lock.'
ms.assetid: 6032ea1f-3c73-4157-ba3f-41ce9e73d64c
title: 'ID3DXFileData :: Unlock, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.Unlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 8371b87152a6184f34a225b24d2de1b0fd21248f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762140"
---
# <a name="id3dxfiledataunlock-method"></a>ID3DXFileData :: Unlock, méthode

Termine la durée de vie du pointeur *ppData* retourné par [**ID3DXFileData :: Lock**](id3dxfiledata--lock.md).

## <a name="syntax"></a>Syntaxe


```C++
BOOL Unlock();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **[ **bool**](../winprog/windows-data-types.md)**

La valeur de retour est \_ OK.

## <a name="remarks"></a>Notes

Vous devez vous assurer que le nombre d’appels [**ID3DXFileData :: Lock**](id3dxfiledata--lock.md) correspond au nombre d’appels **ID3DXFileData :: Unlock** . Après l’appel de Unlock, le pointeur ppData retourné par **ID3DXFileData :: Lock** ne doit plus être utilisé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 
