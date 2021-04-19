---
description: Indicateurs utilisés pour spécifier les options de création d’une maille.
ms.assetid: 1a5a6b3f-34f4-4338-9ffe-8f95f6f0c385
title: Énumération D3DX10_MESH (D3DX10Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_MESH
api_type:
- HeaderDef
api_location:
- D3DX10Mesh.h
ms.openlocfilehash: c2387024512a42c0a9e06ac1818b0282121cd0eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535835"
---
# <a name="d3dx10_mesh-enumeration"></a>D3DX10 \_ , énumération

Indicateurs utilisés pour spécifier les options de création d’une maille.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DX10_MESH { 
  D3DX10_MESH_32_BIT        = 0x001,
  D3DX10_MESH_GS_ADJACENCY  = 0x004
} D3DX10_MESH, *LPD3DX10_MESH;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DX10_MESH_32_BIT"></span><span id="d3dx10_mesh_32_bit"></span>**D3DX10 \_ maille \_ 32 \_ bits**
</dt> <dd>

Le maillage a des index 32 bits plutôt que des index 16 bits. Consultez la section Notes.

</dd> <dt>

<span id="D3DX10_MESH_GS_ADJACENCY"></span><span id="d3dx10_mesh_gs_adjacency"></span>**D3DX10 \_ maille \_ GS \_**
</dt> <dd>

Signale que le maillage contient des données d’adjacence de nuanceur Geometry.

</dd> </dl>

## <a name="remarks"></a>Notes

Une maille 32 bits (D3DXMESH \_ 32 bits) peut théoriquement prendre en charge (2 ³ ²)-1 face et vertex. Toutefois, l’allocation de mémoire pour une maille qui est importante sur un système d’exploitation 32 bits n’est pas pratique.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX10Mesh. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




