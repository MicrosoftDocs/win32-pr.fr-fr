---
description: Décrit un correctif de poids fort triangulaire.
ms.assetid: 3f97120b-3b32-4f95-8614-7b263ff330db
title: Structure D3DTRIPATCH_INFO (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTRIPATCH_INFO
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: c20a846d13cd45bb8a1629fca0e958d3042aacf148c24b0633dd19fb5462bd66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850112"
---
# <a name="d3dtripatch_info-structure"></a>\_Structure d’informations D3DTRIPATCH

Décrit un correctif de poids fort triangulaire.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DTRIPATCH_INFO {
  UINT          StartVertexOffset;
  UINT          NumVertices;
  D3DBASISTYPE  Basis;
  D3DDEGREETYPE Degree;
} D3DTRIPATCH_INFO, *LPD3DTRIPATCH_INFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**StartVertexOffset**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Décalage de début du vertex, en nombre de vertex.

</dd> <dt>

**NumVertices**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre de vertex.

</dd> <dt>

**basis**
</dt> <dd>

Type : **[ **D3DBASISTYPE**](./d3dbasistype.md)**

</dd> <dd>

Membre du type énuméré [**D3DBASISTYPE**](./d3dbasistype.md) , qui définit le type de base pour le correctif de poids fort triangulaire. La seule valeur valide pour ce membre est D3DBASIS \_ Bezier.

</dd> <dt>

**Degré**
</dt> <dd>

Type : **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**

</dd> <dd>

Membre du type énuméré [**D3DDEGREETYPE**](./d3ddegreetype.md) , définissant le type de degré pour le correctif de poids fort triangulaire.



| Valeur                | Nombre de vertex |
|----------------------|--------------------|
| D3DDEGREE \_ cubique     | 10                 |
| D3DDEGREE \_ linéaire    | 3                  |
| D3DDEGREE \_ quadratique | N/A                |
| D3DDEGREE \_ quintaux   | 21                 |



 

Non disponible. Non pris en charge.

</dd> </dl>

## <a name="remarks"></a>Remarques

Par exemple, le diagramme suivant identifie l’ordre des vertex et les numéros de segment pour un correctif de triangle de Bézier cubique. L’ordre des vertex détermine les numéros de segment utilisés par [**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch). Le décalage est le nombre d’octets du premier vertex de patch de triangle dans la mémoire tampon de vertex.

![diagramme d’un correctif de poids fort triangulaire avec neuf vertex](images/hop-tripatch-info.png)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch)
</dt> <dt>

[**D3DXTessellateTriPatch**](d3dxtessellatetripatch.md)
</dt> </dl>

 

 
