---
description: Les applications utilisent les méthodes de l’interface IDirectXFileObject pour récupérer des informations sur les objets fichiers Microsoft DirectX. Action déconseillée.
ms.assetid: 015d2c4e-4a25-40da-b88a-bad0c4e20e09
title: Interface IDirectXFileObject (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileObject
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 3aa0ffffb8766707841fa0a4a5ec54fe0db9caf1d86b885afc36bffa5f8352d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951299"
---
# <a name="idirectxfileobject-interface"></a>Interface IDirectXFileObject

Les applications utilisent les méthodes de l’interface IDirectXFileObject pour récupérer des informations sur les objets fichiers Microsoft DirectX. Action déconseillée.

## <a name="members"></a>Membres

L’interface **IDirectXFileObject** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IDirectXFileObject** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IDirectXFileObject** possède ces méthodes.



| Méthode                                         | Description                                                                                   |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------|
| [**GetId**](idirectxfileobject--getid.md)     | Récupère un pointeur vers le GUID qui identifie un objet fichier DirectX. Action déconseillée.<br/> |
| [**GetName**](idirectxfileobject--getname.md) | Récupère un pointeur vers le nom d’un objet de fichier DirectX. Action déconseillée.<br/>                   |



 

## <a name="remarks"></a>Remarques

Le GUID de l’interface IDirectXFileObject est IID \_ IDirectXFileObject.

Le type LPDIRECTXFILEOBJECT est défini en tant que pointeur vers cette interface.


```
typedef interface IDirectXFileObject *LPDIRECTXFILEOBJECT;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[X, interfaces de fichiers](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
