---
description: Les applications utilisent les méthodes de l’interface ID3DXBaseMesh pour manipuler et interroger les objets de maillage et de maillage progressif.
ms.assetid: ec4ccd77-e370-470c-9325-3d794a8f7f16
title: Interface ID3DXBaseMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 58029639852b30f5de357bb2643583615c45485c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322989"
---
# <a name="id3dxbasemesh-interface"></a>Interface ID3DXBaseMesh

Les applications utilisent les méthodes de l’interface **ID3DXBaseMesh** pour manipuler et interroger les objets de maillage et de maillage progressif.

## <a name="members"></a>Membres

L’interface **ID3DXBaseMesh** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXBaseMesh** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DXBaseMesh** possède ces méthodes.



| Méthode                                                                            | Description                                                                                                                                                                                                           |
|:----------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CloneMesh**](id3dxbasemesh--clonemesh.md)                                     | Clone un maillage à l’aide d’un déclarateur.<br/>                                                                                                                                                                          |
| [**CloneMeshFVF**](id3dxbasemesh--clonemeshfvf.md)                               | Clone un maillage à l’aide d’un code de format de vertex flexible.<br/>                                                                                                                                                   |
| [**ConvertAdjacencyToPointReps**](id3dxbasemesh--convertadjacencytopointreps.md) | Convertit les informations d’adjacence de maillage en un tableau de représentants de point.<br/>                                                                                                                                  |
| [**ConvertPointRepsToAdjacency**](id3dxbasemesh--convertpointrepstoadjacency.md) | Convertit les données représentatives de point en informations d’adjacence de maillage.<br/>                                                                                                                                          |
| [**DrawSubset**](id3dxbasemesh--drawsubset.md)                                   | Dessine un sous-ensemble d’une maille.<br/>                                                                                                                                                                                  |
| [**GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)                     | Générez une liste de contours de maillage, ainsi qu’une liste des visages qui partagent chaque arête.<br/>                                                                                                                            |
| [**GetAttributeTable**](id3dxbasemesh--getattributetable.md)                     | Récupère une table d’attributs pour un maillage ou le nombre d’entrées stockées dans une table d’attributs pour une maille.<br/>                                                                                          |
| [**GetDeclaration**](id3dxbasemesh--getdeclaration.md)                           | Récupère une déclaration décrivant les vertex de la maille.<br/>                                                                                                                                               |
| [**GetDevice**](id3dxbasemesh--getdevice.md)                                     | Récupère l’appareil associé à la maille.<br/>                                                                                                                                                             |
| [**GetFVF**](id3dxbasemesh--getfvf.md)                                           | Obtient la valeur de vertex de fonction fixe.<br/>                                                                                                                                                                      |
| [**GetIndexBuffer**](id3dxbasemesh--getindexbuffer.md)                           | Récupère les données dans une mémoire tampon d’index.<br/>                                                                                                                                                                     |
| [**GetNumBytesPerVertex**](id3dxbasemesh--getnumbytespervertex.md)               | Obtient le nombre d’octets par vertex.<br/>                                                                                                                                                                       |
| [**GetNumFaces**](id3dxbasemesh--getnumfaces.md)                                 | Récupère le nombre de faces dans le maillage.<br/>                                                                                                                                                                 |
| [**GetNumVertices**](id3dxbasemesh--getnumvertices.md)                           | Récupère le nombre de vertex dans la maille.<br/>                                                                                                                                                              |
| [**GetOptions**](id3dxbasemesh--getoptions.md)                                   | Récupère les options de maillage activées pour ce maillage au moment de la création.<br/>                                                                                                                                         |
| [**GetVertexBuffer**](id3dxbasemesh--getvertexbuffer.md)                         | Récupère la mémoire tampon de vertex associée à la maille.<br/>                                                                                                                                                      |
| [**LockIndexBuffer**](id3dxbasemesh--lockindexbuffer.md)                         | Verrouille un tampon d’index et obtient un pointeur vers la mémoire tampon d’index.<br/>                                                                                                                                    |
| [**LockVertexBuffer**](id3dxbasemesh--lockvertexbuffer.md)                       | Verrouille une mémoire tampon de vertex et obtient un pointeur vers la mémoire tampon de vertex.<br/>                                                                                                                                   |
| [**UnlockIndexBuffer**](id3dxbasemesh--unlockindexbuffer.md)                     | Déverrouille un tampon d’index.<br/>                                                                                                                                                                                   |
| [**UnlockVertexBuffer**](id3dxbasemesh--unlockvertexbuffer.md)                   | Déverrouille une mémoire tampon de vertex.<br/>                                                                                                                                                                                   |
| [**UpdateSemantics**](id3dxbasemesh--updatesemantics.md)                         | Cette méthode permet à l’utilisateur de modifier la déclaration de maillage sans modifier la disposition des données de la mémoire tampon de vertex. L’appel est valide uniquement si l’ancien et le nouveau format de déclaration ont la même taille de vertex.<br/> |



 

## <a name="remarks"></a>Notes

Un maillage est un objet constitué d’un ensemble de visages polygones. Une maille définit un ensemble de vertex et un ensemble de faces (les faces sont définies en termes de vertex et de normales de la maille).

Le type LPD3DXBASEMESH est défini comme un pointeur vers l’interface **ID3DXBaseMesh** .


```
typedef struct ID3DXBaseMesh *LPD3DXBASEMESH;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
