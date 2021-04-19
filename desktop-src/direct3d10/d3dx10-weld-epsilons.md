---
description: Spécifie des valeurs de tolérance pour chaque composant de vertex lors de la comparaison des vertex pour déterminer s’ils sont suffisamment semblables pour être soudés ensemble.
ms.assetid: b28a17bd-5d5b-41b3-86d9-327f5497fc94
title: Structure D3DX10_WELD_EPSILONS (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_WELD_EPSILONS
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: c72f63e3ecef1fdb193fcaec9220f9768204d099
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106542169"
---
# <a name="d3dx10_weld_epsilons-structure"></a>Structure des Epsilon de \_ soudure d3dx10 \_

Spécifie des valeurs de tolérance pour chaque composant de vertex lors de la comparaison des vertex pour déterminer s’ils sont suffisamment semblables pour être soudés ensemble.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DX10_WELD_EPSILONS {
  FLOAT Position;
  FLOAT BlendWeights;
  FLOAT Normal;
  FLOAT PSize;
  FLOAT Specular;
  FLOAT Diffuse;
  FLOAT Texcoord[8];
  FLOAT Tangent;
  FLOAT Binormal;
  FLOAT TessFactor;
} D3DX10_WELD_EPSILONS, *LPD3DX10_WELD_EPSILONS;
```



## <a name="members"></a>Membres

<dl> <dt>

**Position**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Position

</dd> <dt>

**BlendWeights**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Poids de fusion

</dd> <dt>

**Normal**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Normal

</dd> <dt>

**PSize**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Valeur de la taille du point

</dd> <dt>

**Spéculaire**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Valeur d’éclairage spéculaire

</dd> <dt>

**Diffus**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Valeur d’éclairage diffus

</dd> <dt>

**Texcoord**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Huit coordonnées de texture

</dd> <dt>

**Tangence**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Tangente

</dd> <dt>

**Binormal**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Binormal

</dd> <dt>

**TessFactor**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Facteur de pavage

</dd> </dl>

## <a name="remarks"></a>Notes

Le type LPD3DXWeldEpsilons est défini en tant que pointeur vers la structure D3DXWeldEpsilons.


```
typedef D3DX_WELD_EPSILONS *LPD3DX_WELD_EPSILONS;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX10. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
