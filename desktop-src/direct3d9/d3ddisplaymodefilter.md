---
description: Spécifie les types de modes d’affichage à exclure.
ms.assetid: 4a03d0f0-dec5-4209-8c99-b58cc13064f5
title: D3DDISPLAYMODEFILTER, structure (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYMODEFILTER
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: f59e2e095f7f0f1c6ee73fc940733e932efaef9af7ec05807ff1b38f35fe5189
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751059"
---
# <a name="d3ddisplaymodefilter-structure"></a>D3DDISPLAYMODEFILTER, structure

Spécifie les types de modes d’affichage à exclure.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  UINT                Size;
  D3DFORMAT           Format;
  D3DSCANLINEORDERING ScanLineOrdering;
} D3DDISPLAYMODEFILTER;
```



## <a name="members"></a>Membres

<dl> <dt>

**Taille**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

La taille de cette structure. Il doit toujours être défini sur sizeof (D3DDISPLAYMODEFILTER).

</dd> <dt>

**Format**
</dt> <dd>

Type : **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Format du mode d’affichage à exclure. Consultez [D3DFORMAT](d3dformat.md).

</dd> <dt>

**ScanLineOrdering**
</dt> <dd>

Type : **[ **D3DSCANLINEORDERING**](./d3dscanlineordering.md)**

</dd> <dd>

Indique si le classement numérisation est entrelacé ou progressif. Consultez [**D3DSCANLINEORDERING**](./d3dscanlineordering.md).

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
