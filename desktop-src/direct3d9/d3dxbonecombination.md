---
description: Décrit un sous-ensemble de la maille qui a la même combinaison d’attributs et de segments.
ms.assetid: e6a4b3bb-d28d-44c2-a6df-f60f0412a70e
title: D3DXBONECOMBINATION, structure (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXBONECOMBINATION
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 72d60b5c87d43763be4700ba7931c61c41cf0101d80390afb737c7f4afda83a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952489"
---
# <a name="d3dxbonecombination-structure"></a>D3DXBONECOMBINATION, structure

Décrit un sous-ensemble de la maille qui a la même combinaison d’attributs et de segments.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DXBONECOMBINATION {
  DWORD AttribId;
  DWORD FaceStart;
  DWORD FaceCount;
  DWORD VertexStart;
  DWORD VertexCount;
  DWORD *BoneId;
} D3DXBONECOMBINATION, *LPD3DXBONECOMBINATION;
```



## <a name="members"></a>Membres

<dl> <dt>

**AttribId**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Identificateur de la table d’attributs.

</dd> <dt>

**FaceStart**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Début de la face.

</dd> <dt>

**FaceCount**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre de visages.

</dd> <dt>

**VertexStart**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Sommet de départ.

</dd> <dt>

**VertexCount**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre de vertex.

</dd> <dt>

**BoneId**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)\***

</dd> <dd>

Pointeur vers un tableau de valeurs qui identifient chacun des segments qui peuvent être dessinés dans un appel de dessin unique. Notez que le tableau peut être de longueur variable pour prendre en charge les combinaisons de longueur variable des segments de [**ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md).

La taille du tableau varie en fonction du type de maillage généré. Une taille de tableau de maillage non indexée est égale au nombre de poids par vertex (pMaxVertexInfl dans [**ConvertToBlendedMesh**](id3dxskininfo--converttoblendedmesh.md)). La taille d’un tableau de maillage indexé est égale au nombre d’entrées de palette de matrices osseuses (paletteSize dans [**ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md)).

</dd> </dl>

## <a name="remarks"></a>Remarques

Le sous-ensemble de la maille décrit par **D3DXBONECOMBINATION** peut être rendu dans un appel de dessin unique.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
