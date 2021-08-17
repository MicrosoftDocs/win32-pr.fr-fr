---
description: Spécifie le rectangle utilisé pour encadrer les glyphes sur une surface monochrome.
ms.assetid: ce5d492f-38d1-4e7b-a9c2-68c791c84d0c
title: D3DCOMPOSERECTDESC, structure (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOMPOSERECTDESC
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 8c23868e8759b98898013ea70d8d62768f1e648eb6e5019eb52dd21ba55905b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117733202"
---
# <a name="d3dcomposerectdesc-structure"></a>D3DCOMPOSERECTDESC, structure

Spécifie le rectangle utilisé pour encadrer les glyphes sur une surface monochrome.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _D3DCOMPOSERECTDESC {
  USHORT X;
  USHORT Y;
  USHORT Width;
  USHORT Height;
} D3DCOMPOSERECTDESC;
```



## <a name="members"></a>Membres

<dl> <dt>

**X**
</dt> <dd>

Type : **[ **UShort**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordonnée gauche à laquelle commencer la copie.

</dd> <dt>

**O**
</dt> <dd>

Type : **[ **UShort**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordonnée supérieure à laquelle commencer la copie.

</dd> <dt>

**Width**
</dt> <dd>

Type : **[ **UShort**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre de texels de la coordonnée gauche.

</dd> <dt>

**Height**
</dt> <dd>

Type : **[ **UShort**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre de texels de la coordonnée supérieure.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette structure est utilisée dans les appels à [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) pour encadrer les glyphes sur la surface source. Une mémoire tampon de vertex (voir [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)) remplie avec ces structures est créée pour contenir les emplacements de glyphe. Les membres USHORT sont utilisés pour réduire autant que possible l’encombrement mémoire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
