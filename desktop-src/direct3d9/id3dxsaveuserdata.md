---
description: 'Interface ID3DXSaveUserData : cette interface est implémentée par l’application pour enregistrer toutes les données utilisateur supplémentaires incorporées dans les fichiers. x.'
ms.assetid: 6294f942-9c14-4eed-92a8-af2821fd7e13
title: Interface ID3DXSaveUserData (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e5b0f02a4fb114f46930076f46ea7c416850a0e81f7369d4aab63a2de5ed6d95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118801135"
---
# <a name="id3dxsaveuserdata-interface"></a>Interface ID3DXSaveUserData

Cette interface est implémentée par l’application pour enregistrer toutes les données utilisateur supplémentaires incorporées dans les fichiers. x. Une instance de cette interface est passée à [**D3DXSaveMeshHierarchyToFile**](d3dxsavemeshhierarchytofile.md), et D3DX appelle la méthode appropriée sur cette interface chaque fois que les données appropriées sont rencontrées. Par exemple, pour chaque objet frame du fichier. x, [**ID3DXSaveUserData :: AddFrameChildData**](id3dxsaveuserdata--addframechilddata.md) est appelé et reçoit les données enfants.

## <a name="members"></a>Membres

L’interface **ID3DXSaveUserData** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXSaveUserData** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DXSaveUserData** possède ces méthodes.



| Méthode                                                                              | Description                                                        |
|:------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [**AddFrameChildData**](id3dxsaveuserdata--addframechilddata.md)                   | Ajoutez des données enfants au frame.<br/>                            |
| [**AddMeshChildData**](id3dxsaveuserdata--addmeshchilddata.md)                     | Ajoutez des données enfants à la maille.<br/>                             |
| [**AddTopLevelDataObjectsPost**](id3dxsaveuserdata--addtopleveldataobjectspost.md) | Ajoutez un objet de niveau supérieur après la hiérarchie de frames.<br/>       |
| [**AddTopLevelDataObjectsPre**](id3dxsaveuserdata--addtopleveldataobjectspre.md)   | Ajoutez un objet de niveau supérieur avant la hiérarchie des frames.<br/>      |
| [**RegisterTemplates**](id3dxsaveuserdata--registertemplates.md)                   | Rappel permettant à l’utilisateur d’inscrire un modèle de fichier. x.<br/> |
| [**SaveTemplates**](id3dxsaveuserdata--savetemplates.md)                           | Rappel permettant à l’utilisateur d’enregistrer un modèle de fichier. x.<br/>     |



 

## <a name="remarks"></a>Remarques

Le type LPD3DXSAVEUSERDATA est défini en tant que pointeur vers cette interface.


```
typedef interface ID3DXSaveUserData ID3DXSaveUserData;
typedef interface ID3DXSaveUserData *LPD3DXSAVEUSERDATA;
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

 

 
