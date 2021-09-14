---
description: Les applications utilisent les méthodes de l’interface IDirectXFileDataReference pour prendre en charge les objets de référence de données.
ms.assetid: e0f6046f-36d9-4a13-9a0c-0738ebb2e569
title: Interface IDirectXFileDataReference (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileDataReference
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: d04d2367f914c2e8d64a3c9c64fb55df1e51e47c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404039"
---
# <a name="idirectxfiledatareference-interface"></a>Interface IDirectXFileDataReference

Les applications utilisent les méthodes de l’interface IDirectXFileDataReference pour prendre en charge les objets de référence de données. Un objet de référence de données fait référence à un objet de données défini précédemment dans le fichier. Cela vous permet d’utiliser le même objet plusieurs fois sans le répéter dans le fichier. Action déconseillée.

## <a name="members"></a>Membres

L’interface **IDirectXFileDataReference** hérite de [**IDirectXFileObject**](idirectxfileobject.md). **IDirectXFileDataReference** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IDirectXFileDataReference** possède ces méthodes.



| Méthode                                                | Description                                      |
|:------------------------------------------------------|:-------------------------------------------------|
| [**Résoudre**](idirectxfiledatareference--resolve.md) | Résout les références de données. Action déconseillée.<br/> |



 

## <a name="remarks"></a>Notes

Une fois que vous avez déterminé qu’un objet est un objet de référence de données, utilisez la méthode [**IDirectXFileDataReference :: Resolve**](idirectxfiledatareference--resolve.md) pour récupérer l’objet référencé défini précédemment dans le fichier. Pour plus d’informations sur l’identification d’un objet de référence de données, consultez l’interface [**IDirectXFileData**](idirectxfiledata.md) .

Le GUID de l’interface IDirectXFileDataReference est IID \_ IDirectXFileDataReference.

Le type LPDIRECTXFILEDataReference est défini en tant que pointeur vers cette interface.


```
typedef interface IDirectXFileDataReference *LPDIRECTXFILEDATAREFERENCE;
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDirectXFileObject**](idirectxfileobject.md)
</dt> <dt>

[X, interfaces de fichiers](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 




