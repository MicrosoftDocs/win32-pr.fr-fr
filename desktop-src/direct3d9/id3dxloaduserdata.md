---
description: Cette interface est implémentée par l’application pour enregistrer toutes les données utilisateur supplémentaires incorporées dans les fichiers. x.
ms.assetid: 0d656f99-c24c-4326-bc6f-c0e7874c0fb2
title: Interface ID3DXLoadUserData (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fcb07ba9351e5f6c23dd86c8147151932b3972ea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538497"
---
# <a name="id3dxloaduserdata-interface"></a>Interface ID3DXLoadUserData

Cette interface est implémentée par l’application pour enregistrer toutes les données utilisateur supplémentaires incorporées dans les fichiers. x. Une instance de cette interface est passée à [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md), et D3DX appelle la méthode appropriée sur cette interface chaque fois que les données appropriées sont rencontrées. Par exemple, pour chaque objet frame du fichier. x, [**ID3DXLoadUserData :: LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) est appelé et reçoit les données enfants.

## <a name="members"></a>Membres

L’interface **ID3DXLoadUserData** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXLoadUserData** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DXLoadUserData** possède ces méthodes.



| Méthode                                                              | Description                                      |
|:--------------------------------------------------------------------|:-------------------------------------------------|
| [**LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) | Charger les données enfants d’un frame à partir d’un fichier. x.<br/> |
| [**LoadMeshChildData**](id3dxloaduserdata--loadmeshchilddata.md)   | Charger les données enfants de maillage à partir d’un fichier. x.<br/>  |
| [**LoadTopLevelData**](id3dxloaduserdata--loadtopleveldata.md)     | Charger les données de niveau supérieur à partir d’un fichier. x.<br/>   |



 

## <a name="remarks"></a>Notes

Le type LPD3DXLOADUSERDATA est défini en tant que pointeur vers cette interface.


```
typedef interface ID3DXLoadUserData ID3DXLoadUserData;
typedef interface ID3DXLoadUserData *LPD3DXLOADUSERDATA;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
