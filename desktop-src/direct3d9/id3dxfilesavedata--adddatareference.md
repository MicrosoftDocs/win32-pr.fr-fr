---
description: Ajoute une référence de données en tant qu’enfant de ce nœud de données de fichier ID3DXFileSaveData. La référence de données pointe vers un objet de données de fichier.
ms.assetid: 75bfe91e-15ea-41f3-b1f7-071fb7f0093f
title: 'ID3DXFileSaveData :: AddDataReference, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.AddDataReference
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 862df88701cffd1059ca67e086cd49d05174bc66e9fa13807df2d2aeb0c9ff1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121348"
---
# <a name="id3dxfilesavedataadddatareference-method"></a>ID3DXFileSaveData :: AddDataReference, méthode

Ajoute une référence de données en tant qu’enfant de ce nœud de données de fichier [**ID3DXFileSaveData**](id3dxfilesavedata.md) . La référence de données pointe vers un objet de données de fichier.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AddDataReference(
  [in]       LPCSTR szName,
  [in] const GUID   *pId
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*szName* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Pointeur vers le nom de l’objet de données à ajouter par référence. Spécifiez **null** si l’objet de données n’a pas de nom.

</dd> <dt>

*PID* \[ dans\]
</dt> <dd>

Type : **const [**GUID**](guid.md) \***

Pointeur vers un GUID représentant l’objet de données à ajouter par référence. Si la **valeur est null**, une référence qui pointe vers l’objet de données avec le nom donné par szName est ajoutée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DXFERR \_ BADOBJECT, D3DXFERR \_ BADVALUE, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarques

L’objet de données de fichier référencé doit avoir un nom ou un GUID. L’objet de données de fichier doit également dériver d’un objet [**ID3DXFileSaveData**](id3dxfilesavedata.md) parent différent.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXFileSaveData](id3dxfilesavedata.md)
</dt> </dl>

 

 
