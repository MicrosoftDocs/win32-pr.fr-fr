---
description: Les applications utilisent les méthodes de l’interface IDirectXFile pour créer des instances des interfaces IDirectXFileEnumObject et IDirectXFileSaveObject, et pour inscrire des modèles. Action déconseillée.
ms.assetid: c4e800dc-72a9-4b91-9c89-ee76764b1bb9
title: Interface IDirectXFile (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 0a1e084108580277432aaeb61086b43a97dbd9f7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118434"
---
# <a name="idirectxfile-interface"></a>Interface IDirectXFile

Les applications utilisent les méthodes de l’interface IDirectXFile pour créer des instances des interfaces [**IDirectXFileEnumObject**](idirectxfileenumobject.md) et [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) , et pour inscrire des modèles. Action déconseillée.

## <a name="members"></a>Membres

L’interface **IDirectXFile** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IDirectXFile** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IDirectXFile** possède ces méthodes.



| Méthode                                                       | Description                                          |
|:-------------------------------------------------------------|:-----------------------------------------------------|
| [**CreateEnumObject**](idirectxfile--createenumobject.md)   | Crée un objet énumérateur. Action déconseillée.<br/> |
| [**CreateSaveObject**](idirectxfile--createsaveobject.md)   | Crée un objet Save. Action déconseillée.<br/>        |
| [**RegisterTemplates**](idirectxfile--registertemplates.md) | Inscrit des modèles personnalisés. Action déconseillée.<br/>   |



 

## <a name="remarks"></a>Notes

L’identificateur global unique (GUID) de l’interface IDirectXFile est IID \_ IDirectXFile.

L’interface IDirectXFile est obtenue en appelant la fonction [**DirectXFileCreate**](directxfilecreate.md) .

Le type LPDIRECTXFILE est défini en tant que pointeur vers cette interface.


```
typedef interface IDirectXFile *LPDIRECTXFILE;
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

 

 
