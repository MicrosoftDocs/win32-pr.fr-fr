---
description: D3DX10_INTERSECT_INFO structure-décrit une intersection de rayons de rayon.
ms.assetid: 21658b74-6f1d-4a16-a8b3-0c7bb6edf899
title: Structure D3DX10_INTERSECT_INFO (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_INTERSECT_INFO
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: d4f660066205a626d6718bf8bd473d54d1d761f9ee499dd0c25a178d9846a0be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753549"
---
# <a name="d3dx10_intersect_info-structure"></a>D3DX10 \_ Intersect ( \_ structure d’informations)

Décrit une intersection de rayons de rayon.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DX10_INTERSECT_INFO {
  UINT  FaceIndex;
  FLOAT U;
  FLOAT V;
  FLOAT Dist;
} D3DX10_INTERSECT_INFO, *LPD3DX10_INTERSECT_INFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**FaceIndex**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Index du triangle qui atteint le rayon.

</dd> <dt>

**U**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordonnée Barycentric dans le triangle où le rayon croise.

</dd> <dt>

**V**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordonnée Barycentric dans le triangle où le rayon croise.

</dd> <dt>

**Dist**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Distance le long du rayon où l’intersection s’est produite.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les coordonnées Barycentric définissent un point à l’intérieur d’un triangle en termes de sommets du triangle. Pour une description plus détaillée des coordonnées Barycentric, consultez [la description des coordonnées Barycentric de MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX10. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
