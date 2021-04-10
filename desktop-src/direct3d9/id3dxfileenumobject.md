---
description: Les applications utilisent les méthodes de l’interface ID3DXFileEnumObject pour parcourir les objets de données de fichier enfant dans le fichier et pour récupérer un objet enfant par son identificateur global unique (GUID) ou par son nom.
ms.assetid: 23b28f07-5832-4163-953b-615d20e781f6
title: Interface ID3DXFileEnumObject (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f9b28f94c8d514f81aaa51426557c825da91c4bf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953905"
---
# <a name="id3dxfileenumobject-interface"></a>Interface ID3DXFileEnumObject

Les applications utilisent les méthodes de l’interface ID3DXFileEnumObject pour parcourir les objets de données de fichier enfant dans le fichier et pour récupérer un objet enfant par son identificateur global unique (GUID) ou par son nom.

## <a name="members"></a>Membres

L’interface **ID3DXFileEnumObject** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXFileEnumObject** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DXFileEnumObject** possède ces méthodes.



| Méthode                                                                  | Description                                                                |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------|
| [**GetChild**](id3dxfileenumobject--getchild.md)                       | Récupère un objet enfant dans cet objet de données de fichier.<br/>              |
| [**GetChildren**](id3dxfileenumobject--getchildren.md)                 | Récupère le nombre d’objets enfants dans cet objet de données de fichier.<br/> |
| [**GetDataObjectById**](id3dxfileenumobject--getdataobjectbyid.md)     | Récupère l’objet de données qui a le GUID spécifié.<br/>          |
| [**GetDataObjectByName**](id3dxfileenumobject--getdataobjectbyname.md) | Récupère l’objet de données qui porte le nom spécifié.<br/>          |
| [**GetFile**](id3dxfileenumobject--getfile.md)                         | Récupère l’objet [**ID3DXFile**](id3dxfile.md) .<br/>            |



 

## <a name="remarks"></a>Notes

Le GUID de l’interface ID3DXFileEnumObject est IID \_ ID3DXFileEnumObject.

Le type LPD3DXFILEENUMOBJECT est défini en tant que pointeur vers cette interface.


```
typedef interface ID3DXFileEnumObject *LPD3DXFILEENUMOBJECT;
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

 

 
