---
description: 'Structure de D3DX10_ATTRIBUTE_RANGE : stocke une entrée de table d’attributs.'
ms.assetid: 81c77dc9-e078-46a1-a435-4b241e36ec13
title: Structure D3DX10_ATTRIBUTE_RANGE (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_ATTRIBUTE_RANGE
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 3e2954483da53c77ebef57f9cf2de104734caba2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094367"
---
# <a name="d3dx10_attribute_range-structure"></a>Structure de la \_ plage d’attributs d3dx10 \_

Stocke une entrée de table d’attributs.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DX10_ATTRIBUTE_RANGE {
  UINT AttribId;
  UINT FaceStart;
  UINT FaceCount;
  UINT VertexStart;
  UINT VertexCount;
} D3DX10_ATTRIBUTE_RANGE, *LPD3DX10_ATTRIBUTE_RANGE;
```



## <a name="members"></a>Membres

<dl> <dt>

**AttribId**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Identificateur de la table d’attributs.

</dd> <dt>

**FaceStart**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Début de la face.

</dd> <dt>

**FaceCount**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre de visages.

</dd> <dt>

**VertexStart**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Sommet de départ.

</dd> <dt>

**VertexCount**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre de vertex.

</dd> </dl>

## <a name="remarks"></a>Notes 

Une table d’attributs permet d’identifier les zones de la maille qui doivent être dessinées avec différentes textures, États de rendu, matériaux, etc. En outre, l’application peut utiliser la table d’attributs pour masquer des parties d’un maillage en ne dessinant pas un identificateur d’attribut (AttribId) donné lors du dessin du frame.

Le \_ type de \_ plage d’attributs LPD3DX est défini en tant que pointeur vers la \_ structure de plage d’attributs D3DX \_ .


```
typedef D3DX_ATTRIBUTE_RANGE* LPD3DX_ATTRIBUTE_RANGE;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX10. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
