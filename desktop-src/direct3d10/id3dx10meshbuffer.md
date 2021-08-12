---
description: Une mémoire tampon de maillage est une mémoire tampon qui contient les données relatives à un maillage.
ms.assetid: a9fdfa22-531d-4da0-89f0-8766c2635e20
title: Interface ID3DX10MeshBuffer (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10MeshBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a2aeabcd6dd3cc711636d0e275f76ab48537953671559e244cf341e270783fb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118540153"
---
# <a name="id3dx10meshbuffer-interface"></a>Interface ID3DX10MeshBuffer

Une mémoire tampon de maillage est une mémoire tampon qui contient les données relatives à un maillage. Il peut contenir l’un des cinq types de données suivants : les données de vertex, les données d’index, les données d’contiguïté, les données d’attribut ou les données de point Rep. La structure est utilisée pour accéder à ces cinq éléments de données par le biais des cinq API suivantes : [**ID3DX10Mesh :: GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md), [**ID3DX10Mesh :: GetIndexBuffer**](id3dx10mesh-getindexbuffer.md), [**ID3DX10Mesh :: GetAdjacencyBuffer**](id3dx10mesh-getadjacencybuffer.md), [**ID3DX10Mesh :: GetAttributeBuffer**](id3dx10mesh-getattributebuffer.md)ou [**ID3DX10Mesh :: GetPointRepBuffer**](id3dx10mesh-getpointrepbuffer.md).

## <a name="members"></a>Membres

L’interface **ID3DX10MeshBuffer** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DX10MeshBuffer** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DX10MeshBuffer** possède ces méthodes.



| Méthode                                       | Description                                                                |
|:---------------------------------------------|:---------------------------------------------------------------------------|
| [**GetSize**](id3dx10meshbuffer-getsize.md) | Obtient la taille de la mémoire tampon de maillage, en octets.<br/>                      |
| [**Canal**](id3dx10meshbuffer-map.md)         | Obtient un pointeur vers la mémoire tampon de maillage pour modifier son contenu.<br/> |
| [**Unmap**](id3dx10meshbuffer-unmap.md)     | Annuler le mappage d’une mémoire tampon.<br/>                                                 |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
