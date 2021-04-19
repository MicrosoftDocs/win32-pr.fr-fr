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
ms.openlocfilehash: e03f4a80c0cff25fa9416d35c20f2d60d17b206b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539439"
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



 

## <a name="remarks"></a>Notes

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

 

 
