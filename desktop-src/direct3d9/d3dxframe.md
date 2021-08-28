---
description: Encapsule un frame de transformation dans une hiérarchie d’frame de transformation.
ms.assetid: 838d75c2-41b2-4703-961b-893c34104c55
title: D3DXFRAME, structure (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFRAME
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 33a851f3580045f5483541be155d3e8e85fddb22b530cb3f889253809f0b13aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123235"
---
# <a name="d3dxframe-structure"></a>D3DXFRAME, structure

Encapsule un frame de transformation dans une hiérarchie d’frame de transformation.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DXFRAME {
  LPSTR               Name;
  D3DXMATRIX          TransformationMatrix;
  LPD3DXMESHCONTAINER pMeshContainer;
  D3DXFRAME           *pFrameSibling;
  D3DXFRAME           *pFrameFirstChild;
} D3DXFRAME, *LPD3DXFRAME;
```



## <a name="members"></a>Membres

<dl> <dt>

**Nom**
</dt> <dd>

Type : **LPSTR**

</dd> <dd>

Nom du frame.

</dd> <dt>

**TransformationMatrix**
</dt> <dd>

Type : **[ **D3DXMATRIX**](d3dxmatrix.md)**

</dd> <dd>

Matrice de transformation.

</dd> <dt>

**pMeshContainer**
</dt> <dd>

Type : **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**

</dd> <dd>

Pointeur vers le conteneur de maillage.

</dd> <dt>

**pFrameSibling**
</dt> <dd>

Type : * * * * D3DXFRAME **\***

</dd> <dd>

Pointeur vers un frame frère.

</dd> <dt>

**pFrameFirstChild**
</dt> <dd>

Type : * * * * D3DXFRAME **\***

</dd> <dd>

Pointeur vers un Frame enfant.

</dd> </dl>

## <a name="remarks"></a>Remarques

Une application peut dériver de cette structure pour ajouter d’autres données.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 




