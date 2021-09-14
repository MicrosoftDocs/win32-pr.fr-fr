---
description: Structure des données de maillage.
ms.assetid: 9164b956-95b7-4bc0-bf7e-feed2e3b4a2b
title: D3DXMESHDATA, structure (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESHDATA
api_type:
- HeaderDef
api_location:
- D3dx9anim.h
ms.openlocfilehash: 785284ba1330c957813a099eb6cf1c74521d3c90
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126924552"
---
# <a name="d3dxmeshdata-structure"></a>D3DXMESHDATA, structure

Structure des données de maillage.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DXMESHDATA {
  D3DXMESHDATATYPE Type;
  union {
    LPD3DXMESH      pMesh;
    LPD3DXPATCHMESH pPatchMesh;
  };
} D3DXMESHDATA, *LPD3DXMESHDATA;
```



## <a name="members"></a>Membres

<dl> <dt>

**Type**
</dt> <dd>

Type : **[ **D3DXMESHDATATYPE**](./d3dxmeshdatatype.md)**

</dd> <dd>

Définit le type de données de maillage. Consultez [**D3DXMESHDATATYPE**](./d3dxmeshdatatype.md).

</dd> <dt>

**pMesh**
</dt> <dd>

Type : **[ **LPD3DXMESH**](id3dxmesh.md)**

</dd> <dd>

Pointeur vers une maille. Consultez [**ID3DXMesh**](id3dxmesh.md).

</dd> <dt>

**pPatchMesh**
</dt> <dd>

Type : **LPD3DXPATCHMESH**

</dd> <dd>

Pointeur vers un filet de correction. Consultez [**ID3DXPatchMesh**](id3dxpatchmesh.md).

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXMESHCONTAINER**](d3dxmeshcontainer.md)
</dt> </dl>

 

 
