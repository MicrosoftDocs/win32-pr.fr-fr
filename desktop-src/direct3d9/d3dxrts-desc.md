---
description: Décrit une surface de rendu.
ms.assetid: cffa1555-1fa2-427d-8bcb-da0e61d82152
title: Structure D3DXRTS_DESC (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXRTS_DESC
api_type:
- HeaderDef
api_location:
- d3dx9core.h
ms.openlocfilehash: 838fc7d08eff0889049e7f0c73ae779239934e49049948b926fa956eeac3d40a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607629"
---
# <a name="d3dxrts_desc-structure"></a>D3DXRTS \_ desc, structure

Décrit une surface de rendu.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DXRTS_DESC {
  UINT      Width;
  UINT      Height;
  D3DFORMAT Format;
  BOOL      DepthStencil;
  D3DFORMAT DepthStencilFormat;
} D3DXRTS_DESC, *LPD3DXRTS_DESC;
```



## <a name="members"></a>Membres

<dl> <dt>

**Width**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Largeur de la surface de rendu, en pixels.

</dd> <dt>

**Height**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Hauteur de la surface de rendu, en pixels.

</dd> <dt>

**Format**
</dt> <dd>

Type : **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Membre du type énuméré [D3DFORMAT](d3dformat.md) , décrivant le format de pixel de la surface de rendu.

</dd> <dt>

**DepthStencil**
</dt> <dd>

Type : **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

Si la **valeur est true**, la surface de rendu prend en charge une surface de stencil de profondeur ; dans le cas contraire, ce membre est défini sur **false**.

</dd> <dt>

**DepthStencilFormat**
</dt> <dd>

Type : **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Si DepthStencil a la valeur **true**, ce paramètre est un membre du type énuméré [D3DFORMAT](d3dformat.md) , qui décrit le format de stencil de profondeur de la surface de rendu.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9core. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**ID3DXRenderToSurface::GetDesc**](id3dxrendertosurface--getdesc.md)
</dt> </dl>

 

 
