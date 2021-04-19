---
description: Les applications utilisent les méthodes de l’interface ID3DX10Mesh pour manipuler les objets de maillage.
ms.assetid: 1734b8fd-e1a6-4aa4-96a0-8693019a9dac
title: Interface ID3DX10Mesh (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2ddf0876928f85debded1645b9a22de790917017
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531374"
---
# <a name="id3dx10mesh-interface"></a>Interface ID3DX10Mesh

Les applications utilisent les méthodes de l’interface ID3DX10Mesh pour manipuler les objets de maillage.

## <a name="members"></a>Membres

L’interface **ID3DX10Mesh** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DX10Mesh** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DX10Mesh** possède ces méthodes.



| Méthode                                                                                   | Description                                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CloneMesh**](id3dx10mesh-clonemesh.md)                                               | Crée un nouveau maillage et le remplit avec les données d’un maillage précédemment chargé.<br/>                                                                                                                                                                                                                                                |
| [**CommitToDevice**](id3dx10mesh-committodevice.md)                                     | Validez toutes les modifications apportées à un maillage sur l’appareil afin que les modifications puissent être rendues. Cela doit être appelé après la modification des données d’un maillage et avant son rendu. Un maillage ne peut pas être rendu, sauf s’il est validé sur l’appareil. Consultez la section Remarques.<br/>                                                                         |
| [**Abandonner**](id3dx10mesh-discard.md)                                                   | Supprime les données de maillage de l’appareil qui a été validé sur l’appareil (avec [**ID3DX10Mesh :: CommitToDevice**](id3dx10mesh-committodevice.md)).<br/>                                                                                                                                                                         |
| [**DrawSubset**](id3dx10mesh-drawsubset.md)                                             | Dessine un sous-ensemble d’une maille.<br/>                                                                                                                                                                                                                                                                                                 |
| [**DrawSubsetInstanced**](id3dx10mesh-drawsubsetinstanced.md)                           | Dessinez plusieurs instances du même sous-ensemble d’une maille.<br/>                                                                                                                                                                                                                                                                      |
| [**GenerateAdjacencyAndPointReps**](id3dx10mesh-generateadjacencyandpointreps.md)       | Générez une liste de contours de maillage, ainsi qu’une liste des visages qui partagent chaque arête.<br/>                                                                                                                                                                                                                                           |
| [**GenerateAttributeBufferFromTable**](id3dx10mesh-generateattributebufferfromtable.md) | Générez une mémoire tampon d’attribut à partir des données de la table d’attributs du maillage. Une mémoire tampon d’attributs est un autre format de stockage des données dans la table d’attributs. La mémoire tampon d’attribut et la table d’attributs sont des structures de données internes dans la maille.<br/>                                                                  |
| [**GenerateGSAdjacency**](id3dx10mesh-generategsadjacency.md)                           | Ajoute des données d’adjacence à la mémoire tampon d’index du maillage. Lorsque la maille doit être envoyée à un nuanceur Geometry qui accepte les données d’contiguïté, il est nécessaire que le tampon d’index du maillage contienne les données d’contiguïté.<br/>                                                                                                                       |
| [**GetAdjacencyBuffer**](id3dx10mesh-getadjacencybuffer.md)                             | Accédez à la mémoire tampon d’adjacence du maillage.<br/>                                                                                                                                                                                                                                                                                       |
| [**GetAttributeBuffer**](id3dx10mesh-getattributebuffer.md)                             | Accédez à la mémoire tampon d’attribut du maillage.<br/>                                                                                                                                                                                                                                                                                       |
| [**GetAttributeTable**](id3dx10mesh-getattributetable.md)                               | Récupère une table d’attributs pour un maillage ou le nombre d’entrées stockées dans une table d’attributs pour une maille.<br/>                                                                                                                                                                                                         |
| [**GetDeviceIndexBuffer**](id3dx10mesh-getdeviceindexbuffer.md)                         | Accédez à la mémoire tampon d’index du maillage une fois qu’elle a été validée sur l’appareil avec [**ID3DX10Mesh :: CommitToDevice**](id3dx10mesh-committodevice.md). Cela diffère de [**ID3DX10Mesh :: GetIndexBuffer**](id3dx10mesh-getindexbuffer.md), qui retourne la mémoire tampon d’index avant qu’elle ait été validée sur l’appareil.<br/>     |
| [**GetDeviceVertexBuffer**](id3dx10mesh-getdevicevertexbuffer.md)                       | Accédez à la mémoire tampon de vertex du maillage une fois qu’elle a été validée sur l’appareil avec [**ID3DX10Mesh :: CommitToDevice**](id3dx10mesh-committodevice.md). Cela diffère de [**ID3DX10Mesh :: GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md), qui retourne la mémoire tampon de vertex avant qu’elle n’ait été validée sur l’appareil.<br/> |
| [**GetFaceCount**](id3dx10mesh-getfacecount.md)                                         | Récupère le nombre de faces dans le maillage.<br/>                                                                                                                                                                                                                                                                                |
| [**GetFlags**](id3dx10mesh-getflags.md)                                                 | Accédez aux indicateurs de création du maillage.<br/>                                                                                                                                                                                                                                                                                         |
| [**GetIndexBuffer**](id3dx10mesh-getindexbuffer.md)                                     | Récupère les données dans une mémoire tampon d’index.<br/>                                                                                                                                                                                                                                                                                    |
| [**GetPointRepBuffer**](id3dx10mesh-getpointrepbuffer.md)                               | Obtient la mémoire tampon du REP du point de la maille.<br/>                                                                                                                                                                                                                                                                                          |
| [**GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md)                                   | Récupère la mémoire tampon de vertex associée à la maille.<br/>                                                                                                                                                                                                                                                                     |
| [**GetVertexBufferCount**](id3dx10mesh-getvertexbuffercount.md)                         | Obtient le nombre de mémoires tampons de vertex dans la maille.<br/>                                                                                                                                                                                                                                                                             |
| [**GetVertexCount**](id3dx10mesh-getvertexcount.md)                                     | Obtient le nombre de vertex dans la maille. Un maillage peut contenir plusieurs mémoires tampons de vertex (c’est-à-dire qu’une mémoire tampon de vertex peut contenir toutes les données de position, une autre peut contenir toutes les données de coordonnée de texture, etc.), mais chaque mémoire tampon de vertex contiendra le même nombre d’éléments.<br/>                                                   |
| [**GetVertexDescription**](id3dx10mesh-getvertexdescription.md)                         | Accédez à la description du vertex passée dans [**D3DX10CreateMesh**](d3d10-d3dx10createmesh.md). La description du vertex décrit la disposition des mémoires tampons de vertex du maillage.<br/>                                                                                                                                                   |
| [**Coupe**](id3dx10mesh-intersect.md)                                               | Détermine si un rayon croise ce maillage.<br/>                                                                                                                                                                                                                                                                            |
| [**IntersectSubset**](id3dx10mesh-intersectsubset.md)                                   | Détermine si un rayon entre en intersection avec un sous-ensemble de ce maillage.<br/>                                                                                                                                                                                                                                                                |
| [**Optimiser**](id3dx10mesh-optimize.md)                                                 | Génère un nouveau maillage avec des faces et des sommets réorganisés pour optimiser les performances du dessin.<br/>                                                                                                                                                                                                                                   |
| [**SetAdjacencyData**](id3dx10mesh-setadjacencydata.md)                                 | Définissez les données d’adjacence du maillage.<br/>                                                                                                                                                                                                                                                                                            |
| [**SetAttributeData**](id3dx10mesh-setattributedata.md)                                 | Définissez les données d’attribut du maillage.<br/>                                                                                                                                                                                                                                                                                            |
| [**SetAttributeTable**](id3dx10mesh-setattributetable.md)                               | Définit la table d’attributs pour un maillage et le nombre d’entrées stockées dans la table.<br/>                                                                                                                                                                                                                                        |
| [**SetIndexData**](id3dx10mesh-setindexdata.md)                                         | Définissez les données d’index du maillage.<br/>                                                                                                                                                                                                                                                                                                |
| [**SetPointRepData**](id3dx10mesh-setpointrepdata.md)                                   | Définissez les données du point de représentation du maillage.<br/>                                                                                                                                                                                                                                                                                      |
| [**SetVertexData**](id3dx10mesh-setvertexdata.md)                                       | Définissez les données de vertex dans l’une des mémoires tampons de vertex du maillage.<br/>                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Notes

Pour obtenir l’interface ID3DX10Mesh, appelez [**D3DX10CreateMesh**](d3d10-d3dx10createmesh.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
