---
description: Les applications utilisent les méthodes de l’interface ID3DXFileData pour créer ou accéder à la hiérarchie immédiate de l’objet de données. Les restrictions de modèle déterminent la hiérarchie.
ms.assetid: ce291e2b-b926-4502-8bee-55fe6d6d3267
title: Interface ID3DXFileData (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1764787864c059e9c7417525a1a5ab5ff862f7d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211844"
---
# <a name="id3dxfiledata-interface"></a>Interface ID3DXFileData

Les applications utilisent les méthodes de l’interface ID3DXFileData pour créer ou accéder à la hiérarchie immédiate de l’objet de données. Les restrictions de modèle déterminent la hiérarchie.

## <a name="members"></a>Membres

L’interface **ID3DXFileData** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXFileData** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DXFileData** possède ces méthodes.



| Méthode                                            | Description                                                                                                          |
|:--------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**GetChild**](id3dxfiledata--getchild.md)       | Récupère un objet enfant dans cet objet de données de fichier.<br/>                                                        |
| [**GetChildren**](id3dxfiledata--getchildren.md) | Récupère le nombre d’enfants dans cet objet de données de fichier.<br/>                                                |
| [**GetEnum**](id3dxfiledata--getenum.md)         | Récupère l’objet d’énumération dans cet objet de données de fichier.<br/>                                                |
| [**GetId**](id3dxfiledata--getid.md)             | Récupère le GUID de cet objet de données de fichier.<br/>                                                              |
| [**GetName**](id3dxfiledata--getname.md)         | Récupère le nom de cet objet de données de fichier.<br/>                                                              |
| [**GetType**](id3dxfiledata--gettype.md)         | Récupère l’ID de modèle dans cet objet de données de fichier.<br/>                                                       |
| [**IsReference**](id3dxfiledata--isreference.md) | Indique si cet objet de données de fichier est un objet de référence qui pointe vers un autre objet de données enfant.<br/>   |
| [**Lock**](id3dxfiledata--lock.md)               | Accède aux données du fichier. x.<br/>                                                                                |
| [**Bloquer**](id3dxfiledata--unlock.md)           | Termine la durée de vie du pointeur *ppData* retourné par [**ID3DXFileData :: Lock**](id3dxfiledata--lock.md).<br/> |



 

## <a name="remarks"></a>Notes

Les types de données autorisés par le modèle sont appelés membres facultatifs. Les membres facultatifs ne sont pas requis, mais un objet peut manquer des informations importantes sans eux. Ces membres facultatifs sont enregistrés en tant qu’enfants de l’objet de données. Un enfant peut être un autre objet de données ou une référence à un objet de données antérieur.

Le GUID de l’interface ID3DXFileData est IID \_ ID3DXFileData.

Le type LPD3DXFILEDATA est défini en tant que pointeur vers cette interface.


```
typedef interface ID3DXFileData *LPD3DXFILEDATA;
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

 

 
