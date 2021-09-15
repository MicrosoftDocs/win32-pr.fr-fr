---
description: Les applications utilisent les méthodes de l’interface IDirectXFileSaveObject pour créer des objets de données et enregistrer des modèles et des objets de données.
ms.assetid: 7948a7d2-b150-45cf-a1fc-5dca21d74770
title: Interface IDirectXFileSaveObject (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 4be69b10037381d4b06466d52483427b6d40499a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520509"
---
# <a name="idirectxfilesaveobject-interface"></a>Interface IDirectXFileSaveObject

Les applications utilisent les méthodes de l’interface IDirectXFileSaveObject pour créer des objets de données et enregistrer des modèles et des objets de données. Notez que les modèles ne sont pas requis dans chaque fichier. Par exemple, vous pouvez placer tous les modèles dans un seul fichier Microsoft DirectX au lieu de les dupliquer dans chaque fichier DirectX. Action déconseillée.

## <a name="members"></a>Membres

L’interface **IDirectXFileSaveObject** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IDirectXFileSaveObject** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IDirectXFileSaveObject** possède ces méthodes.



| Méthode                                                               | Description                                                                    |
|:---------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**CreateDataObject**](idirectxfilesaveobject--createdataobject.md) | Crée un objet de données. Action déconseillée.<br/>                                  |
| [**SaveData**](idirectxfilesaveobject--savedata.md)                 | Enregistre un objet de données et ses enfants dans un fichier DirectX. Action déconseillée.<br/> |
| [**SaveTemplates**](idirectxfilesaveobject--savetemplates.md)       | Enregistre les modèles dans un fichier DirectX. Action déconseillée.<br/>                      |



 

## <a name="remarks"></a>Notes

L’identificateur global unique (GUID) de l’interface IDirectXFileSaveObject est **IID \_ IDirectXFileSaveObject**.

L’interface **IDirectXFileSaveObject** est obtenue en appelant la méthode [**IDirectXFile :: CreateSaveObject**](idirectxfile--createsaveobject.md) .

Le type **LPDIRECTXFILESAVEOBJECT** est défini en tant que pointeur vers cette interface.


```
typedef interface IDirectXFileSaveObject *LPDIRECTXFILESAVEOBJECT;
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

 

 
