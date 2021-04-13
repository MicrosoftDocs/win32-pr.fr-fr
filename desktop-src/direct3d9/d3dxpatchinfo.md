---
description: Structure qui contient les attributs d’un filet de correction.
ms.assetid: aaea69c9-2d33-46e8-bc26-95daf65abf50
title: D3DXPATCHINFO, structure (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPATCHINFO
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 8628cc27a0223580aa1f8072750f4c31a176533e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322634"
---
# <a name="d3dxpatchinfo-structure"></a>D3DXPATCHINFO, structure

Structure qui contient les attributs d’un filet de correction.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DXPATCHINFO {
  D3DXPATCHMESHTYPE PatchType;
  D3DDEGREETYPE     Degree;
  D3DBASISTYPE      Basis;
} D3DXPATCHINFO, *LPD3DXPATCHINFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**PatchType**
</dt> <dd>

Type : **[ **D3DXPATCHMESHTYPE**](./d3dxpatchmeshtype.md)**

</dd> <dd>

Type de correctif. Pour plus d’informations sur les types de correctifs, consultez [**D3DXPATCHMESHTYPE**](./d3dxpatchmeshtype.md).

</dd> <dt>

**Degré**
</dt> <dd>

Type : **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**

</dd> <dd>

Degré des courbes utilisées pour construire le correctif. Pour plus d’informations sur les degrés pris en charge, consultez [**D3DDEGREETYPE**](./d3ddegreetype.md).

</dd> <dt>

**basis**
</dt> <dd>

Type : **[ **D3DBASISTYPE**](./d3dbasistype.md)**

</dd> <dd>

Type de courbe utilisé pour construire le correctif. Pour plus d’informations sur les types de base pris en charge, consultez [**D3DBASISTYPE**](./d3dbasistype.md).

</dd> </dl>

## <a name="remarks"></a>Notes

Une maille est un ensemble de faces, chacune d’elles étant décrite par un polygone simple. Les objets peuvent être créés en connectant plusieurs mailles ensemble. Une maille de correctif est construite à partir de patchs. Un patch est un élément de géométrie à quatre faces construit à partir de courbes. Le type de courbe utilisé et l’ordre de la courbe peuvent être variés afin que la surface de la facette corresponde à presque toutes les formes de surface.

Les types de combinaisons de correctifs suivants sont pris en charge :



| Type de correctif | basis       | Degré |
|------------|-------------|--------|
| Rectangle  | Bézier      | 2, 3, 5  |
| Rectangle  | B-spline    | 2, 3, 5  |
| Rectangle  | Catmull-Rom | 3      |
| Triangle   | Bézier      | 2, 3, 5  |
| N-patch    | N/A         | 3      |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**\_Informations D3DRECTPATCH**](d3drectpatch-info.md)
</dt> <dt>

[**\_Informations D3DTRIPATCH**](d3dtripatch-info.md)
</dt> <dt>

[**D3DXCreatePatchMesh**](d3dxcreatepatchmesh.md)
</dt> </dl>

 

 
