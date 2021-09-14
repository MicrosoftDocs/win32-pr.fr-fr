---
description: Encapsule un objet de maillage dans une hiérarchie de frame de transformation.
ms.assetid: 50e98230-7dc3-468a-92c4-8165e8fe242b
title: D3DXMESHCONTAINER, structure (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESHCONTAINER
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: f57daea26f42d8dd680d0259199b0df77badf510
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126924555"
---
# <a name="d3dxmeshcontainer-structure"></a>D3DXMESHCONTAINER, structure

Encapsule un objet de maillage dans une hiérarchie de frame de transformation.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DXMESHCONTAINER {
  LPSTR                Name;
  D3DXMESHDATA         MeshData;
  LPD3DXMATERIAL       pMaterials;
  LPD3DXEFFECTINSTANCE pEffects;
  DWORD                NumMaterials;
  DWORD                *pAdjacency;
  LPD3DXSKININFO       pSkinInfo;
  D3DXMESHCONTAINER    *pNextMeshContainer;
} D3DXMESHCONTAINER, *LPD3DXMESHCONTAINER;
```



## <a name="members"></a>Membres

<dl> <dt>

**Nom**
</dt> <dd>

Type : **LPSTR**

</dd> <dd>

Nom du maillage.

</dd> <dt>

**MeshData**
</dt> <dd>

Type : **[ **D3DXMESHDATA**](d3dxmeshdata.md)**

</dd> <dd>

Type de données dans la maille. Consultez [**D3DXMESHDATA**](d3dxmeshdata.md).

</dd> <dt>

**pMaterials**
</dt> <dd>

Type : **[ **LPD3DXMATERIAL**](d3dxmaterial.md)**

</dd> <dd>

Tableau de supports de maillage. Consultez [**D3DXMATERIAL**](d3dxmaterial.md).

</dd> <dt>

**pEffects**
</dt> <dd>

Type : **[ **LPD3DXEFFECTINSTANCE**](d3dxeffectinstance.md)**

</dd> <dd>

Pointeur vers un ensemble de paramètres d’effet par défaut. Consultez [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).

</dd> <dt>

**NumMaterials**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre de matériaux dans la maille.

</dd> <dt>

**pAdjacency**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)\***

</dd> <dd>

Pointeur vers un tableau de trois DWORDs par triangle du maillage qui contient les informations d’adjacence.

</dd> <dt>

**pSkinInfo**
</dt> <dd>

Type : **[ **LPD3DXSKININFO**](id3dxskininfo.md)**

</dd> <dd>

Pointeur vers l’interface d’informations d’apparence. Consultez [**ID3DXSkinInfo**](id3dxskininfo.md).

</dd> <dt>

**pNextMeshContainer**
</dt> <dd>

Type : * * * * D3DXMESHCONTAINER **\***

</dd> <dd>

Pointeur vers le conteneur de maillage suivant.

</dd> </dl>

## <a name="remarks"></a>Notes

Une application peut dériver de cette structure pour ajouter d’autres données.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
