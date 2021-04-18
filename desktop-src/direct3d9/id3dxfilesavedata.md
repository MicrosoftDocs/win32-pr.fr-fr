---
description: Les applications utilisent les méthodes de l’interface ID3DXFileSaveData pour ajouter des objets de données comme enfants d’un nœud de données de fichier. x.
ms.assetid: ab5bdd9a-496a-4ae1-b93a-fe5856bd97d4
title: Interface ID3DXFileSaveData (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d42f431dbb2f9108c5e503aea07ba6b11915f0ac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522589"
---
# <a name="id3dxfilesavedata-interface"></a>Interface ID3DXFileSaveData

Les applications utilisent les méthodes de l’interface ID3DXFileSaveData pour ajouter des objets de données comme enfants d’un nœud de données de fichier. x.

## <a name="members"></a>Membres

L’interface **ID3DXFileSaveData** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXFileSaveData** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DXFileSaveData** possède ces méthodes.



| Méthode                                                          | Description                                                                                                                                |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddDataObject**](id3dxfilesavedata--adddataobject.md)       | Ajoute un objet de données en tant qu’enfant du nœud de données du fichier **ID3DXFileSaveData** .<br/>                                                      |
| [**AddDataReference**](id3dxfilesavedata--adddatareference.md) | Ajoute une référence de données en tant qu’enfant de ce nœud de données de fichier **ID3DXFileSaveData** . La référence de données pointe vers un objet de données de fichier.<br/> |
| [**GetId**](id3dxfilesavedata--getid.md)                       | Récupère le GUID de ce nœud de données de fichier **ID3DXFileSaveData** .<br/>                                                                |
| [**GetName**](id3dxfilesavedata--getname.md)                   | Récupère le nom de ce nœud de données de fichier **ID3DXFileSaveData** .<br/>                                                                |
| [**GetSave**](id3dxfilesavedata--getsave.md)                   | Récupère un pointeur vers ce nœud de données de fichier [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) .<br/>                                  |
| [**GetType**](id3dxfilesavedata--gettype.md)                   | Récupère l’ID de modèle de ce nœud de données de fichier.<br/>                                                                               |



 

## <a name="remarks"></a>Notes

Le GUID de l’interface ID3DXFileSaveObject est IID \_ ID3DXFileSaveObject.

Le type LPD3DXFileSaveData est défini en tant que pointeur vers cette interface.


```
typedef interface ID3DXFileSaveData *LPD3DXFILESAVEDATA;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces de fichiers D3DX X](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
