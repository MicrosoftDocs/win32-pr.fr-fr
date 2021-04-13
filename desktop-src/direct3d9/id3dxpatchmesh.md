---
description: Cette interface encapsule la fonctionnalité de maillage des correctifs.
ms.assetid: c70c0fe0-b695-4ad9-b0c6-7854cf8f7593
title: Interface ID3DXPatchMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f1f13e6abe3a164e8027ddcb6bb33e9f0ca618fb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323061"
---
# <a name="id3dxpatchmesh-interface"></a>Interface ID3DXPatchMesh

Cette interface encapsule la fonctionnalité de maillage des correctifs.

## <a name="members"></a>Membres

L’interface **ID3DXPatchMesh** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXPatchMesh** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DXPatchMesh** possède ces méthodes.



| Méthode                                                                           | Description                                                                                     |
|:---------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**CloneMesh**](id3dxpatchmesh--clonemesh.md)                                   | Crée un maillage de correctifs avec la déclaration de vertex spécifiée.<br/>                      |
| [**GenerateAdjacency**](id3dxpatchmesh--generateadjacency.md)                   | Générez une liste de bords de maillage et les correctifs qui partagent chaque périphérie.<br/>                  |
| [**GetControlVerticesPerPatch**](id3dxpatchmesh--getcontrolverticesperpatch.md) | Obtient le nombre de vertex de contrôle par correctif.<br/>                                       |
| [**GetDeclaration**](id3dxpatchmesh--getdeclaration.md)                         | Obtient la déclaration de vertex.<br/>                                                         |
| [**GetDevice**](id3dxpatchmesh--getdevice.md)                                   | Obtient l’appareil qui a créé le maillage.<br/>                                               |
| [**GetDisplaceParam**](id3dxpatchmesh--getdisplaceparam.md)                     | Obtient les paramètres de déplacement de la géométrie de maillage.<br/>                                          |
| [**GetIndexBuffer**](id3dxpatchmesh--getindexbuffer.md)                         | Obtient la mémoire tampon d’index de maillage.<br/>                                                          |
| [**GetNumPatches**](id3dxpatchmesh--getnumpatches.md)                           | Obtient le nombre de correctifs dans la maille.<br/>                                              |
| [**GetNumVertices**](id3dxpatchmesh--getnumvertices.md)                         | Obtient le nombre de vertex dans le maillage.<br/>                                             |
| [**GetOptions**](id3dxpatchmesh--getoptions.md)                                 | Obtient le type de correctif.<br/>                                                              |
| [**GetPatchInfo**](id3dxpatchmesh--getpatchinfo.md)                             | Obtient les attributs du correctif.<br/>                                                    |
| [**GetTessSize**](id3dxpatchmesh--gettesssize.md)                               | Obtient la taille du maillage fractionné, en fonction d’un niveau de pavage.<br/>                   |
| [**GetVertexBuffer**](id3dxpatchmesh--getvertexbuffer.md)                       | Obtient la mémoire tampon de vertex de maillage.<br/>                                                         |
| [**LockAttributeBuffer**](id3dxpatchmesh--lockattributebuffer.md)               | Verrouille la mémoire tampon d’attribut.<br/>                                                          |
| [**LockIndexBuffer**](id3dxpatchmesh--lockindexbuffer.md)                       | Verrouillez le tampon d’index.<br/>                                                               |
| [**LockVertexBuffer**](id3dxpatchmesh--lockvertexbuffer.md)                     | Verrouille la mémoire tampon de vertex.<br/>                                                              |
| [**Optimiser**](id3dxpatchmesh--optimize.md)                                     | Optimise le maillage des correctifs pour une polygonalisation efficace.<br/>                                 |
| [**SetDisplaceParam**](id3dxpatchmesh--setdisplaceparam.md)                     | Définit les paramètres de déplacement de la géométrie du maillage.<br/>                                          |
| [**Paver**](id3dxpatchmesh--tessellate.md)                                 | Effectue un pavage uniforme basé sur le niveau de pavage.<br/>                       |
| [**TessellateAdaptive**](id3dxpatchmesh--tessellateadaptive.md)                 | Effectue un pavage adaptatif basé sur le critère de pavage adaptative basé sur z.<br/> |
| [**UnlockAttributeBuffer**](id3dxpatchmesh--unlockattributebuffer.md)           | Déverrouillez la mémoire tampon d’attribut.<br/>                                                         |
| [**UnlockIndexBuffer**](id3dxpatchmesh--unlockindexbuffer.md)                   | Déverrouillez la mémoire tampon d’index.<br/>                                                             |
| [**UnlockVertexBuffer**](id3dxpatchmesh--unlockvertexbuffer.md)                 | Déverrouillez la mémoire tampon de vertex.<br/>                                                            |



 

## <a name="remarks"></a>Notes

Une maille de correctif est une maille qui se compose d’une série de correctifs.

Pour obtenir l’interface **ID3DXPatchMesh** , appelez la fonction [**D3DXCreatePatchMesh**](d3dxcreatepatchmesh.md) .

Le type LPD3DXPATCHMESH est défini comme un pointeur vers l’interface **ID3DXPatchMesh** , comme suit :


```
typedef struct ID3DXPatchMesh *LPD3DXPATCHMESH;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[Fonctions de maillage](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
