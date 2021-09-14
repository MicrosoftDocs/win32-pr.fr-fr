---
description: Les applications utilisent les méthodes de l’interface IDirectXFileEnumObject pour parcourir les objets de données dans le fichier et pour récupérer un objet de données par son identificateur global unique (GUID) ou par son nom. Action déconseillée.
ms.assetid: 9eefda2a-5b17-4330-8245-63a38c1b1469
title: Interface IDirectXFileEnumObject (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: f9220f6e0a406cb4143798787276d7aa6cb5f5d1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127124430"
---
# <a name="idirectxfileenumobject-interface"></a>Interface IDirectXFileEnumObject

Les applications utilisent les méthodes de l’interface IDirectXFileEnumObject pour parcourir les objets de données dans le fichier et pour récupérer un objet de données par son identificateur global unique (GUID) ou par son nom. Action déconseillée.

## <a name="members"></a>Membres

L’interface **IDirectXFileEnumObject** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IDirectXFileEnumObject** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IDirectXFileEnumObject** possède ces méthodes.



| Méthode                                                                     | Description                                                                     |
|:---------------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [**GetDataObjectById**](idirectxfileenumobject--getdataobjectbyid.md)     | Récupère l’objet de données qui a le GUID spécifié. Action déconseillée.<br/>   |
| [**GetDataObjectByName**](idirectxfileenumobject--getdataobjectbyname.md) | Récupère l’objet de données qui porte le nom spécifié. Action déconseillée.<br/>   |
| [**GetNextDataObject**](idirectxfileenumobject--getnextdataobject.md)     | Récupère l’objet de niveau supérieur suivant dans le fichier DirectX. Action déconseillée.<br/> |



 

## <a name="remarks"></a>Notes

Le GUID de l’interface IDirectXFileEnumObject est IID \_ IDirectXFileEnumObject.

Le type LPDIRECTXFILEENUMOBJECT est défini en tant que pointeur vers cette interface.


```
typedef interface IDirectXFileEnumObject *LPDIRECTXFILEENUMOBJECT;
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[X, interfaces de fichiers](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
