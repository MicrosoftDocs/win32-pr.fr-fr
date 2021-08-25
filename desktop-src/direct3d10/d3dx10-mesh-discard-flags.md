---
description: Spécifie les éléments de données de maillage à ignorer de l’appareil. Utilisé avec ID3DX10Mesh ::D iscard.
ms.assetid: 8b3c22ab-1337-4a66-ae32-17bd1b73f624
title: Énumération D3DX10_MESH_DISCARD_FLAGS (D3DX10Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_MESH_DISCARD_FLAGS
api_type:
- HeaderDef
api_location:
- D3DX10Mesh.h
ms.openlocfilehash: d4b98550a2f3a896ed7b99f3e16f33a399a58035497e44420709ee8a0726901b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989469"
---
# <a name="d3dx10_mesh_discard_flags-enumeration"></a>\_ \_ Énumération d’indicateurs d3dx10 Mesh ignore \_

Spécifie les éléments de données de maillage à ignorer de l’appareil. Utilisé avec [**ID3DX10Mesh ::D iscard**](id3dx10mesh-discard.md).

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DX10_MESH_DISCARD_FLAGS { 
  D3DX10_MESH_DISCARD_ATTRIBUTE_BUFFER  = 0x01,
  D3DX10_MESH_DISCARD_ATTRIBUTE_TABLE   = 0x02,
  D3DX10_MESH_DISCARD_POINTREPS         = 0x04,
  D3DX10_MESH_DISCARD_ADJACENCY         = 0x08,
  D3DX10_MESH_DISCARD_DEVICE_BUFFERS    = 0x10
} D3DX10_MESH_DISCARD_FLAGS, *LPD3DX10_MESH_DISCARD_FLAGS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DX10_MESH_DISCARD_ATTRIBUTE_BUFFER"></span><span id="d3dx10_mesh_discard_attribute_buffer"></span>**\_Tampon d' \_ attribut de rejet de maillage d3dx10 \_ \_**
</dt> <dd>

Ignorer la mémoire tampon d’attribut.

</dd> <dt>

<span id="D3DX10_MESH_DISCARD_ATTRIBUTE_TABLE"></span><span id="d3dx10_mesh_discard_attribute_table"></span>**\_Table d' \_ attributs de rejet de maillage d3dx10 \_ \_**
</dt> <dd>

Ignorez la table d’attributs.

</dd> <dt>

<span id="D3DX10_MESH_DISCARD_POINTREPS"></span><span id="d3dx10_mesh_discard_pointreps"></span>**D3DX10 \_ Mesh \_ Discard \_ POINTREPS**
</dt> <dd>

Ignore la mémoire tampon des délégués du pointeur.

</dd> <dt>

<span id="D3DX10_MESH_DISCARD_ADJACENCY"></span><span id="d3dx10_mesh_discard_adjacency"></span>**D3DX10 de l’écart de la \_ maille \_ \_**
</dt> <dd>

Ignorer la mémoire tampon de contiguïté.

</dd> <dt>

<span id="D3DX10_MESH_DISCARD_DEVICE_BUFFERS"></span><span id="d3dx10_mesh_discard_device_buffers"></span>**\_Tampons de l’appareil d3dx10 Mesh \_ Discard \_ \_**
</dt> <dd>

Ignorez les mémoires tampons validées sur l’appareil (avec [**ID3DX10Mesh :: CommitToDevice**](id3dx10mesh-committodevice.md)).

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX10Mesh. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




