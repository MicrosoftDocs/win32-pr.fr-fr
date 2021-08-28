---
description: Les applications utilisent les méthodes de l’interface IDirectXFileData pour créer ou accéder à la hiérarchie immédiate de l’objet de données.
ms.assetid: 8810162f-76a8-45ba-b069-7910fd611a60
title: Interface IDirectXFileData (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 72b3ffa54d9ec0362100b2e2f1ac54b417d1425d0e6e311da3f9b5b7d30a553a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118800209"
---
# <a name="idirectxfiledata-interface"></a>Interface IDirectXFileData

Les applications utilisent les méthodes de l’interface IDirectXFileData pour créer ou accéder à la hiérarchie immédiate de l’objet de données. Les restrictions de modèle déterminent la hiérarchie. Les types de données autorisés par le modèle sont appelés membres facultatifs. Les membres facultatifs ne sont pas requis, mais un objet peut manquer des informations importantes sans eux. Ces membres facultatifs sont enregistrés en tant qu’enfants de l’objet de données. Les enfants peuvent être un autre objet de données, une référence à un objet de données antérieur ou un objet binaire. Action déconseillée.

## <a name="members"></a>Membres

L’interface **IDirectXFileData** hérite de [**IDirectXFileObject**](idirectxfileobject.md). **IDirectXFileData** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IDirectXFileData** possède ces méthodes.



| Méthode                                                         | Description                                                                                                               |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------|
| [**AddBinaryObject**](idirectxfiledata--addbinaryobject.md)   | Crée un objet binaire et l’ajoute en tant qu’objet enfant. Action déconseillée.<br/>                                             |
| [**AddDataObject**](idirectxfiledata--adddataobject.md)       | Ajoute un objet de données en tant qu’objet enfant. Action déconseillée.<br/>                                                              |
| [**AddDataReference**](idirectxfiledata--adddatareference.md) | Crée et ajoute un objet de référence de données en tant qu’objet enfant. Action déconseillée.<br/>                                        |
| [**GetData**](idirectxfiledata--getdata.md)                   | Récupère les données de l’un des membres de l’objet ou les données de tous les membres. Action déconseillée.<br/>                    |
| [**GetNextObject**](idirectxfiledata--getnextobject.md)       | Récupère l’objet de données enfants, l’objet de référence de données ou l’objet binaire suivant dans le fichier DirectX. Action déconseillée.<br/> |
| [**GetType**](idirectxfiledata--gettype.md)                   | Récupère le GUID du modèle de l’objet. Action déconseillée.<br/>                                                       |



 

## <a name="remarks"></a>Remarques

Le GUID de l’interface IDirectXFileData est IID \_ IDirectXFileData.

Le type LPDIRECTXFILEDATA est défini en tant que pointeur vers cette interface.


```
typedef interface IDirectXFileData *LPDIRECTXFILEDATA;
```



## <a name="requirements"></a>Configuration requise



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

 

 




