---
description: Les applications utilisent les méthodes de l’interface IDirectXFileBinary pour lire et récupérer des informations sur les données binaires. Action déconseillée.
ms.assetid: 43b20ab3-67b2-4717-ad90-0bf4ddb3207e
title: Interface IDirectXFileBinary (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 46e0da3a0cb03d3769e7888706a48fbf00786471afed285ce54c629285ac158c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118292408"
---
# <a name="idirectxfilebinary-interface"></a>Interface IDirectXFileBinary

Les applications utilisent les méthodes de l’interface IDirectXFileBinary pour lire et récupérer des informations sur les données binaires. Action déconseillée.

## <a name="members"></a>Membres

L’interface **IDirectXFileBinary** hérite de [**IDirectXFileObject**](idirectxfileobject.md). **IDirectXFileBinary** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IDirectXFileBinary** possède ces méthodes.



| Méthode                                                 | Description                                                                                                 |
|:-------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**GetMimeType**](idirectxfilebinary--getmimetype.md) | Récupère le type MIME (Multipurpose Internet Mail Extensions) pour les données binaires. Action déconseillée.<br/> |
| [**GetSize**](idirectxfilebinary--getsize.md)         | Récupère la taille des données binaires. Action déconseillée.<br/>                                               |
| [**Lire**](idirectxfilebinary--read.md)               | Lit les données binaires. Action déconseillée.<br/>                                                               |



 

## <a name="remarks"></a>Notes

Le GUID de l’interface IDirectXFileBinary est IID \_ IDirectXFileBinary.

Le type LPDIRECTXFileBinary est défini en tant que pointeur vers cette interface.


```
typedef interface IDirectXFileBinary *LPDIRECTXFILEBINARY;
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

 

 




