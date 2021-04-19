---
description: Informations sur les propriétés d’un mode d’affichage.
ms.assetid: df9d12b9-7acb-435b-9d54-0b095c871f0e
title: D3DDISPLAYMODEEX, structure (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYMODEEX
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5906b6b23cc83e6d2379f0c5923b08b220285708
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535799"
---
# <a name="d3ddisplaymodeex-structure"></a>D3DDISPLAYMODEEX, structure

Informations sur les propriétés d’un mode d’affichage.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  UINT                Size;
  UINT                Width;
  UINT                Height;
  UINT                RefreshRate;
  D3DFORMAT           Format;
  D3DSCANLINEORDERING ScanLineOrdering;
} D3DDISPLAYMODEEX;
```



## <a name="members"></a>Membres

<dl> <dt>

**Taille**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

La taille de cette structure. Il doit toujours être défini sur sizeof (D3DDISPLAYMODEEX).

</dd> <dt>

**Width**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Largeur du mode d’affichage.

</dd> <dt>

**Height**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Hauteur du mode d’affichage.

</dd> <dt>

**RefreshRate**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Fréquence d’actualisation du mode d’affichage.

</dd> <dt>

**Format**
</dt> <dd>

Type : **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Format du mode d’affichage. Consultez [D3DFORMAT](d3dformat.md).

</dd> <dt>

**ScanLineOrdering**
</dt> <dd>

Type : **[ **D3DSCANLINEORDERING**](./d3dscanlineordering.md)**

</dd> <dd>

Indique si l’ordre de numérisation est progressif ou entrelacé. Consultez [**D3DSCANLINEORDERING**](./d3dscanlineordering.md).

</dd> </dl>

## <a name="remarks"></a>Notes

Cette structure est utilisée dans différentes méthodes pour créer et gérer des appareils Direct3D 9Ex ([**IDirect3DDevice9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex)) et chaînes d’échange ([**IDirect3DSwapChain9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dswapchain9ex)).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
