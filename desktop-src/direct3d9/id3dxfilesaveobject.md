---
description: Les applications utilisent les méthodes de l’interface ID3DXFileSaveObject pour écrire un fichier. x sur le disque, ainsi que pour ajouter et enregistrer des objets et des modèles de données.
ms.assetid: 1131c151-fa21-4654-9776-484922d58487
title: Interface ID3DXFileSaveObject (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b6efb87f92a81ec40fe919d76d18a9746e0d88c45f19616933f1b014402aa3e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121183"
---
# <a name="id3dxfilesaveobject-interface"></a>Interface ID3DXFileSaveObject

Les applications utilisent les méthodes de l’interface ID3DXFileSaveObject pour écrire un fichier. x sur le disque, ainsi que pour ajouter et enregistrer des objets et des modèles de données.

## <a name="members"></a>Membres

L’interface **ID3DXFileSaveObject** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXFileSaveObject** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DXFileSaveObject** possède ces méthodes.



| Méthode                                                      | Description                                                                                                                  |
|:------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [**AddDataObject**](id3dxfilesaveobject--adddataobject.md) | Ajoute un objet de données en tant qu’enfant de l’objet [**ID3DXFileSaveData**](id3dxfilesavedata.md) .<br/>                       |
| [**GetFile**](id3dxfilesaveobject--getfile.md)             | Obtient l’interface [**ID3DXFile**](id3dxfile.md) de l’objet qui a créé cet objet **ID3DXFileSaveObject** .<br/> |
| [**Enregistrer**](id3dxfilesaveobject--save.md)                   | Enregistre un objet de données et ses enfants dans un fichier. x sur le disque.<br/>                                                        |



 

## <a name="remarks"></a>Remarques

Les modèles ne sont pas requis dans chaque fichier. Par exemple, vous pouvez placer tous les modèles dans un seul fichier. x plutôt que de les dupliquer dans chaque fichier. x.

L’interface ID3DXFileSaveObject est obtenue en appelant la méthode [**ID3DXFile :: CreateSaveObject**](id3dxfile--createsaveobject.md) .

L’identificateur global unique (GUID) de l’interface ID3DXFileSaveObject est IID \_ ID3DXFileSaveObject.

Le type LPD3DXFILESAVEOBJECT est défini en tant que pointeur vers cette interface.


```
typedef interface ID3DXFileSaveObject *LPD3DXFILESAVEOBJECT;
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

 

 
