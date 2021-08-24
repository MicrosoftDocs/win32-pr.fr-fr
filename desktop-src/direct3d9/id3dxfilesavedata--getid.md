---
description: Récupère le GUID de ce nœud de données de fichier ID3DXFileSaveData.
ms.assetid: 79413eb4-4889-4148-b1a1-58a0b780403c
title: 'ID3DXFileSaveData :: GetId, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetId
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 4e6f502357510cc1c8fc51e9ada844a988a79b1571435639586380929b121c43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748499"
---
# <a name="id3dxfilesavedatagetid-method"></a>ID3DXFileSaveData :: GetId, méthode

Récupère le GUID de ce nœud de données de fichier [**ID3DXFileSaveData**](id3dxfilesavedata.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetId(
  [out] 
            LPGUID pId
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PID* \[ à\]
</dt> <dd>

Type : **LPGUID**

Pointeur vers un GUID pour recevoir l’ID de ce nœud de données de fichier. Si l’objet n’a pas d’ID, la valeur de paramètre retournée est le GUID \_ null.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur suivante est retournée : D3DXFERR \_ BADVALUE.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXFileSaveData](id3dxfilesavedata.md)
</dt> </dl>

 

 




